---
title: Anzeigen von Informationen zu Benutzer-PINs in Skype for Business Server 2015
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 8/17/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: 59e38117-8112-4851-82ac-a746ffa0f89d
description: 'Zusammenfassung: Benutzer der PIN-Informationen in Skype Business Server 2015 anzeigen'
ms.openlocfilehash: 2521c9edba0b16eda6ea799b6b968a8c57bba245
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="view-user-pin-information-in-skype-for-business-server-2015"></a>Anzeigen von Informationen zu Benutzer-PINs in Skype for Business Server 2015
 
**Zusammenfassung:** Benutzer anzeigen PIN-Informationen in Skype Business Server 2015.
  
Um eine Zugriffsnummer für Einwahl Konferenz als authentifizierter Benutzer teilzunehmen, erfordert einen Skype für Benutzer mit Active Directory-Domänendienste (AD DS) Anmeldeinformationen Business Server 2015 eine persönliche Identifikationsnummer (PIN). Sie können einen Benutzer-PIN-Informationen von Skype für Business Server-Systemsteuerung anzeigen.
  
> [!NOTE]
> Sie können Statusinformationen PIN, z. B., ob die PIN-Nummer festgelegt wurde oder wenn die PIN-Nummer der letzten Änderung anzeigen, aber nicht die aktuelle PIN anhand des PIN-Status angezeigt. Wenn ein Benutzer seine PIN verloren gegangen ist, können Sie es zurücksetzen, indem Sie den Verfahren im [eines Benutzers einwahlkonferenzen in Skype für Business Server 2015 PIN festlegen](set-a-user-s-dial-in-conferencing-pin.md)
  
### <a name="to-view-a-users-pin-in-skype-for-business-server-control-panel"></a>Zum Anzeigen von PIN eines Benutzers in Skype Business Server-Systemsteuerung

1. Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen.  
    
3. Klicken Sie in der linken Navigationsleiste auf **Benutzer**.
    
4. Verwenden Sie eine der folgenden Methoden, um nach einem Benutzer zu suchen:
    
   - Geben Sie im Feld **Benutzer suchen** den vollständigen oder teilweisen Anzeigenamen, Vornamen, Nachnamen, SAM-Kontonamen (Security Accounts Manager), die SIP-Adresse oder den Anschluss-URI (Uniform Resource Identifier) des Benutzerkontos ein und klicken Sie dann auf **Suchen**.
    
   - Wenn Sie über eine gespeicherte Abfrage verfügen, klicken Sie auf das Symbol **Abfrage öffnen**, verwenden Sie das Dialogfeld **Öffnen**, um die Abfrage abzurufen (eine USF-Datei), und klicken Sie dann auf **Suchen**.
    
5. (Optional) Geben Sie zusätzliche Suchkriterien ein, um die Ergebnisse einzuschränken:
    
   a. Klicken Sie auf **Filter hinzufügen**.
    
   b. Geben Sie die Benutzereigenschaft ein, indem Sie sie über die Tastatur eintippen oder auf den Pfeil in der Dropdownliste klicken, um die Eigenschaft auszuwählen.
    
   c. Klicken Sie in der Dropdownliste **Gleich** auf den Operator (beispielsweise **Gleich** oder **Ungleich**).
    
   d. Je nachdem, welche Benutzereigenschaft Sie ausgewählt haben, geben Sie nun die Kriterien ein, mit denen Sie die Suchergebnisse filtern möchten, oder treffen eine entsprechende Auswahl in der Dropdownliste.
    
    > [!TIP]
    > Klicken Sie auf **Filter hinzufügen**, um zusätzliche Suchklauseln einzugeben. 
  
   e. Klicken Sie auf **Suchen**.
    
    > [!NOTE]
    > Ist die PIN gesperrt, müssen Sie die Sperre zunächst aufheben, bevor Sie die PIN festlegen können. Klicken Sie zum Aufheben der Sperre auf den Benutzer, dann auf **Aktion** und auf **PIN entsperren**. 
  
6. Klicken Sie auf einen Benutzer in den Suchergebnissen und dann auf **Aktion** und auf **PIN-Status anzeigen**.
    
## <a name="viewing-user-pin-information-by-using-windows-powershell-cmdlets"></a>Anzeigen von PIN-Informationen für Benutzer von mithilfe von Windows PowerShell-cmdlets

Sie können die PIN-Informationen für Benutzer mit dem Cmdlet „Get-CsClientPinInfo“ anzeigen. Dieses Cmdlet kann von der Skype für Business Server-Verwaltungsshell oder von einer remote Windows PowerShell-Sitzung ausgeführt werden. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-view-user-pin-information"></a>So zeigen Sie die PIN-Informationen von Benutzern an

Zum Anzeigen von PIN-Informationen für einen Benutzer geben Sie einen Befehl ähnlich dem folgenden in der Skype für Business Server-Verwaltungsshell, und drücken Sie dann die EINGABETASTE:
    
  ```
  Get-CsClientPinInfo -Identity "Ken Myer"
  ```

Es werden etwa folgende Informationen zurückgegeben:

  ```
  Identity          : sip:kenmyer@litwareinc.com
IsPinSet          : False
IsLockedOut       : False
LastPinChangeTime : 9/25/2012 1:35:03 PM
PinExpirationTime :
  ```

Weitere Informationen finden Sie im Hilfethema zum [Get-CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/get-csconferencedisclaimer?view=skype-ps) -Cmdlet.
  
## <a name="see-also"></a>Siehe auch

#### 

[Einrichten eines Benutzers einwahlkonferenzen PIN in Skype für Business Server 2015](set-a-user-s-dial-in-conferencing-pin.md)
  
[Sperren oder Entsperren einer Benutzer-PIN in Skype für Business Server 2015](lock-or-unlock-a-user-pin.md)
