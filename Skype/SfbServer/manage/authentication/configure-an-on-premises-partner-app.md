---
title: Konfigurieren einer lokalen Partneranwendung für Skype for Business Server 2015
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 8/17/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: 696f2b26-e5d0-42b5-9785-a26c2ce25bb7
description: 'Zusammenfassung: Konfigurieren einer lokalen partneranwendung für Skype für Business Server 2015.'
ms.openlocfilehash: 4a31d97f7a4c2f717084c72cbc349c4f495597ea
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="configure-an-on-premises-partner-application-for-skype-for-business-server-2015"></a>Konfigurieren einer lokalen Partneranwendung für Skype for Business Server 2015
 
**Zusammenfassung:** Konfigurieren einer lokalen partneranwendung für Skype für Business Server 2015.
  
Nachdem Sie das Zertifikat OAuthTokenIssuer zugewiesen haben, müssen Sie klicken Sie dann Ihre Skype für partneranwendungen Business Server 2015 konfigurieren. (Die Prozedur, die erläutert werden konfiguriert sowohl Microsoft Exchange Server 2013 und SharePoint als partneranwendungen, der optional ist). Um einer lokalen partneranwendung zu konfigurieren, müssen Sie starten durch Kopieren des folgenden Windows PowerShell-Skripts und den Code in Editor (oder einem anderen Texteditor) einfügen:
  
```
if ((Get-CsPartnerApplication -ErrorAction SilentlyContinue) -ne $Null)
   {
       Remove-CsPartnerApplication app
   }

$exch = Get-CsPartnerApplication microsoft.exchange -ErrorAction SilentlyContinue
        
if ($exch -eq $null)
   {
      New-CsPartnerApplication -Identity microsoft.exchange -MetadataUrl https://atl-exchange-001.litwareinc.com/autodiscover/metadata/json/1 -ApplicationTrustLevel Full 
    }
else
    {
       if ($exch.ApplicationIdentifier -ne "00000002-0000-0ff1-ce00-000000000000")
          {
             Remove-CsPartnerApplication microsoft.exchange
New-CsPartnerApplication -Identity microsoft.exchange -MetadataUrl https://atl-exchange-001.litwareinc.com/autodiscover/metadata/json/1 -ApplicationTrustLevel Full 
           }
        else
           {
             Set-CsPartnerApplication -Identity microsoft.exchange -ApplicationTrustLevel Full 
           }
     }

$shp = Get-CsPartnerApplication microsoft.sharepoint -ErrorAction SilentlyContinue
        
if ($shp -eq $null)
   {
      New-CsPartnerApplication -Identity microsoft.sharepoint -MetadataUrl http://atl-sharepoint-001.litwareinc.com/jsonmetadata.ashx -ApplicationTrustLevel Full 
    }
else
    {
       if ($shp.ApplicationIdentifier -ne "00000003-0000-0ff1-ce00-000000000000")
          {
             Remove-CsPartnerApplication microsoft.sharepoint
  
             New-CsPartnerApplication -Identity microsoft.sharepoint -MetadataUrl https://atl-sharepoint-001.litwareinc.com/_layouts/15/metadata/json/1 -ApplicationTrustLevel Full 
           }
        else
           {
             Set-CsPartnerApplication -Identity microsoft.sharepoint -ApplicationTrustLevel Full 
            }
   }

Set-CsOAuthConfiguration -ServiceName 00000004-0000-0ff1-ce00-000000000000

```

Nach dem Kopieren des Codes, speichern Sie das Skript mithilfe einer. Erweiterung der ps1 (beispielsweise C:\Scripts\ServerToServerAuth.ps1). Beachten Sie, dass Sie, bevor Sie dieses Skript ausführen, müssen Sie die Metadaten-URLs ersetzen https://atl-exchange-001.litwareinc.com/autodiscover/metadata/json/1 und http://atl-sharepoint-001.litwareinc.com/_layouts/15/metadata/json/1 mit den Metadaten-URLs, die jeweils von der Exchange 2013 und SharePoint Server verwendet. Finden Sie in der Produktdokumentation für Exchange 2013 und SharePoint Informationen auf, wie Sie Metadaten-URL für das betreffende Produkt identifizieren können.
  
In der letzten Zeile des Skripts werden Sie bemerken, dass das Cmdlet „Set-CsOAuthConfiguration“ mit der folgenden Syntax aufgerufen wird:
  
```
Set-CsOAuthConfiguration -ServiceName 00000004-0000-0ff1-ce00-000000000000
```

Da beim Aufrufen von „Set-CsOAuthConfiguration“ der Parameter „Realm“ nicht verwendet wurde, wird als Bereich automatisch der vollqualifizierte Domänenname (FQDN) Ihrer Organisation festgelegt (z. B. litwareinc.com). Wenn der Bereichsname anders als Ihr Organisationsname lautet, sollten Sie den Bereichsnamen wie folgt mit angeben:
  
```
Set-CsOAuthConfiguration -ServiceName 00000004-0000-0ff1-ce00-000000000000 -Realm "contoso.com"
```

Nach dem Ändern dieser Änderungen können Sie anschließend führen Sie das Skript und Konfigurieren von Exchange 2013 und SharePoint als partneranwendungen, durch die Skriptdatei aus innerhalb der Skype für Business Server-Verwaltungsshell ausführen. Beispiel:
  
```
C:\Scripts\ServerToServerAuth.ps1
```

Beachten Sie, dass Sie dieses Skript ausführen können, selbst wenn Sie keinen sowohl Exchange 2013 und SharePoint Server installiert:, keine Probleme tritt auf, wenn Sie, sagen, SharePoint Server als partneranwendung konfigurieren, auch wenn Sie keine SharePoint Server installiert.
  
Bei Ausführung des Skripts würden Sie dann eine Fehlermeldung erhalten, die wie folgt aussieht:
  
```
New-CsPartnerApplication : Cannot bind parameter 'MetadataUrl' to the target. Exception setting "MetadataUrl": "The metadata document could not be downloaded from the URL in the MetadataUrl parameter or downloaded data is not a valid metadata document."
```

Diese Fehlermeldung hat meist zwei Bedeutungen: 1.) Eine der im Skript angegebenen URLs ist ungültig (d. h. eine Ihrer Metadaten-URLs ist tatsächlich keine Metadaten-URL) oder 2.) eine der Metadaten-URLs konnte nicht kontaktiert werden. In diesem Fall sollten Sie überprüfen, ob die URLs korrekt geschrieben sind und auf sie zugegriffen werden kann, und das Skript danach erneut ausführen.
  
Nach dem Erstellen der partneranwendung für Skype für Business Server 2015 müssen Sie Skype für Business Server werden als partneranwendung für Exchange 2013 konfigurieren. Sie können durch Ausführen des Skripts konfigurieren EnterprisePartnerApplication.ps1 partneranwendungen für Exchange 2013 konfigurieren. müssen Sie nur die Metadaten-URL für Skype für Business Server angeben und anzugeben, dass Skype für Business Server die neue partneranwendung ist. 
  
Zum Konfigurieren von Skype für Business Server als partneranwendung für Exchange, öffnen Sie die Exchange-Verwaltungsshell, und führen Sie einen Befehl wie den folgenden
  
```
"c:\Program Files\Microsoft\Exchange Server\V15\Scripts\Configure-EnterprisePartnerApplication.ps1" -AuthMetadataUrl "https://SkypePro.contoso.com/metadata/json/1" -ApplicationType "Lync"
```

