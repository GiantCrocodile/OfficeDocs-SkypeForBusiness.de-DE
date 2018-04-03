---
title: Aktivieren der Aufzeichnung von Kommunikationsdatensätzen in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 3b28e432-596f-45a5-a070-577d6fa748d9
description: 'Zusammenfassung: Erfahren Sie, wie die Aufzeichnung von kommunikationsdatensätzen (CDR) Datensätze in Skype für Business Server 2015 zu aktivieren.'
ms.openlocfilehash: 3fe33f3cfde310b3674c125b7eb8ab1bf04f7c03
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="enable-call-detail-recording-in-skype-for-business-server-2015"></a>Aktivieren der Aufzeichnung von Kommunikationsdatensätzen in Skype for Business Server 2015
 
**Zusammenfassung:** Erfahren Sie, wie die Aufzeichnung von kommunikationsdatensätzen (CDR) Datensätze in Skype für Business Server 2015 zu aktivieren.
  
Bei der Aufzeichnung von Kommunikationsdatensätzen werden Nutzungs- und Diagnoseinformationen über Peer-to-Peer-Aktivitäten aufgezeichnet, z. B. Chat, VoIP-Anrufe (Voice over Internet Protocol), Anwendungsfreigabe, Dateiübertragung und Besprechungen. Anhand der Nutzungsdaten kann die Rendite berechnet werden und die Diagnosedaten können zur Problembehandlung bei Peer-to-Peer-Aktivitäten und Besprechungen eingesetzt werden. 
  
Verwenden Sie das folgende Verfahren, um die Aufzeichnung von Kommunikationsdatensätzen (KDS) in der gesamten Organisation oder für jeden Standort in Ihrer Organisation zu aktivieren.
  
> [!NOTE]
> Zur Aktivierung von KDS müssen Sie die Überwachung und eine Überwachungsdatenbank konfigurieren. Weitere Informationen hierzu finden Sie unter [Deploying Monitoring](http://technet.microsoft.com/library/117f4a3e-0670-4388-a553-b9854921145f.aspx). 
  
### <a name="to-enable-cdr-with-skype-for-business-server-control-panel"></a>So aktivieren Sie KDS mit Skype für Business Server-Systemsteuerung

1.  Von einem Benutzerkonto, das Mitglied der Gruppe RTCUniversalServerAdmins (oder gleichwertige Benutzerrechte verfügt), oder der CsServerAdministrator oder CsAdministrator-Rolle, melden Sie sich an einem beliebigen Computer, die im Netzwerk ist in der Bereitstellung von Skype für Business Server zugeordnet ist 2015.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen. 
    
3. Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **Aufzeichnung von Kommunikationsdatensätzen**. 
    
4. Klicken Sie auf der Seite **Aufzeichnung von Kommunikationsdatensätzen** in der Tabelle auf den geeigneten Standort, klicken Sie auf **Aktion** und anschließend auf **KDS aktivieren**.
    
    > [!NOTE]
    > KDS ist standardmäßig aktiviert. 
  
## <a name="enabling-cdr-by-using-windows-powershell-cmdlets"></a>Aktivieren KDS mithilfe von Windows PowerShell-cmdlets

Sie können KDS aktivieren, mithilfe von Windows PowerShell und das **Set-CsCdrConfiguration** -Cmdlet. Sie können dieses Cmdlet entweder von der Skype für Business Server-Verwaltungsshell oder aus einer Remotesitzung von Windows PowerShell ausführen. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-enable-cdr-for-a-single-location"></a>So aktivieren Sie KDS für einen einzelnen Standort

 Sie können KDS aktivieren, indem Sie den Parameter „EnableCDR“ auf „True“ ($True) setzen.
    
  ```
  Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $True
  ```

### <a name="to-disable-cdr-for-a-single-location"></a>So deaktivieren Sie KDS für einen einzelnen Standort

 Sie können KDS deaktivieren, indem Sie den Parameter „EnableCDR“ auf „False“ ($False) setzen. Durch die Deaktivierung von KDS wird die Überwachung nicht deinstalliert, sondern die Sammlung und Speicherung von KDS-Daten angehalten.
    
  ```
  Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False
  ```

### <a name="to-use-a-single-command-to-enable-cdr-in-multiple-locations"></a>So verwenden Sie einen einzelnen Befehl zum Aktivieren von KDS an mehreren Standorten

 Mit diesem Befehl wird KDS für alle derzeit in der Organisation verwendeten KDS-Einstellungen aktiviert.
    
  ```
  Get-CsCdrConfiguration | Set-CsCdrConfiguration "site:Redmond" -EnableCDR $True
  ```

Weitere Informationen finden Sie im Hilfethema zum [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/set-cscdrconfiguration?view=skype-ps) -Cmdlet.
  
## <a name="see-also"></a>Siehe auch

[Planen der Überwachung](http://technet.microsoft.com/library/26cead5a-183c-42f1-a4b0-0e8d61c6159d.aspx)
  
[Bereitstellen des Monitoring](http://technet.microsoft.com/library/117f4a3e-0670-4388-a553-b9854921145f.aspx)