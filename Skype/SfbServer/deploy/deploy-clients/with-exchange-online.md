---
title: Bereitstellen von Skype Room Systems v2 mit Exchange Online (Hybrid)
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.custom: Strat_SB_Admin
ms.assetid: f3ba85b8-442c-4133-963f-76f1c8a1fff9
description: Lesen Sie dieses Thema bietet Informationen zum Bereitstellen von Skype Raum Systemen v2 mit Exchange Online.
ms.openlocfilehash: 59724ae9b0fc77f16a072e0e08b125407c6e43e3
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="deploy-skype-room-systems-v2-with-exchange-online-hybrid"></a>Bereitstellen von Skype Room Systems v2 mit Exchange Online (Hybrid)
 
Lesen Sie dieses Thema bietet Informationen zum Bereitstellen von Skype Raum Systemen v2 mit Exchange Online.
  
Wenn Ihre Organisation eine Kombination von Diensten, mit einigen an lokalen und online gehostet gehostet hat, wird die Konfiguration abhängen, wo jeden Dienst gehostet wird. In diesem Thema werden für Skype Raum Systemen v2 hybridbereitstellungen mit Exchange online gehostet. Da so viele verschiedene Variationen bei dieser Art von Bereitstellung vorhanden sind, ist nicht möglich, detaillierte Informationen für alle bereitzustellen. Der folgende Prozess wird für viele Konfigurationen verwendet werden. Wenn der Vorgang nicht für die Installation die richtige ist, es wird empfohlen, dass Sie Windows PowerShell verwenden (finden Sie in Anhang: PowerShell) um die gleiche Endergebnis zu erzielen, wie hier und für andere Bereitstellungsoptionen dokumentiert. Sie sollten klicken Sie dann das bereitgestellte Windows PowerShell-Skript verwenden, überprüfen Sie das Skype Raum Systemen v2 Setup. (Siehe Konto Überprüfungsskript).
  
## <a name="deploy-skype-room-systems-v2-with-exchange-online"></a>Bereitstellen von Skype Room Systems v2 mit Exchange Online

Vor der Bereitstellung von Skype Raum Systemen v2 mit Exchange Online, achten Sie darauf, dass Sie die Anforderungen erfüllt sind. Weitere Informationen finden Sie unter [Skype Raum Systemen v2 Requirements](../../plan-your-deployment/clients-and-devices/requirements.md).
  
Zum Bereitstellen von Skype Raum Systemen v2 mit Exchange Online, führen Sie die folgenden Schritte aus. Vergewissern Sie sich, dass Sie über die erforderlichen Berechtigungen zum Ausführen der zugehörigen Cmdlets verfügen. 
  
### <a name="create-an-account-and-set-exchange-properties"></a>Erstellen eines Kontos und Festlegen der Exchange-Eigenschaften

1. Starten Sie eine remote Windows PowerShell-Sitzung auf einem PC und eine Verbindung mit Exchange Online wie folgt:
    
  ```
  Set-ExecutionPolicy Unrestricted
$org='contoso.microsoft.com'
$cred=Get-Credential $admin@$org
$sess= New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/ps1-liveid/ -Credential $cred -Authentication Basic 
-AllowRedirection

  ```

2. Nach dem Einrichten einer Sitzung, werden Sie entweder ein neues Postfach erstellen und als eine RoomMailboxAccount zu aktivieren oder Ändern der Einstellungen für ein vorhandenes Raumpostfach. Dadurch wird das Konto in Skype Raum Systemen v2 zu authentifizieren.
    
   Wenn Sie ein vorhandenes Ressourcenpostfach ändern:
    
   ```
   Set-Mailbox -Identity 'PROJECTRIGEL01' -EnableRoomMailboxAccount $true -RoomMailboxPassword (ConvertTo-SecureString -String <password> -AsPlainText -Force)
   ```

    Wenn Sie eine neue Ressourcenpostfach erstellen:
    
   ```
   New-Mailbox -MicrosoftOnlineServicesID 'PROJECTRIGEL01@contoso.com' -Alias PROJECTRIGEL01 -Name "Project-Rigel-01" -Room -EnableRoomMailboxAccount $true -RoomMailboxPassword (ConvertTo-SecureString -String <password> -AsPlainText -Force)
   ```

3. Um der Besprechung zu optimieren, benötigen Sie die Exchange-Eigenschaften für das Benutzerkonto wie folgt festgelegt:
    
   ```
   Set-CalendarProcessing -Identity 'PROJECTRIGEL01@contoso.com' -AutomateProcessing AutoAccept -AddOrganizerToSubject $false -AllowConflicts $false -DeleteComments $false -DeleteSubject $false -RemovePrivateProperty $false
   Set-CalendarProcessing -Identity 'PROJECTRIGEL01@contoso.com' -AddAdditionalResponse $true -AdditionalResponse "This is a Skype Meeting room!"
   ```

4. Geben Sie das Kennwort für dieses Konto ein. Sie müssen das Kennwort zur Bestätigung erneut eingeben. Stellen Sie sicher, dass als einzige Option das Kontrollkästchen **Kennwort läuft nie ab** aktiviert ist.
    
    > [!NOTE]
    > Auswählen von **Kennwort läuft nie ab** ist eine Voraussetzung für Skype für Business Server 2015 auf Skype Raum Systemen v2. Möglicherweise verhindern Ihre Domänenregeln nicht ablaufende Kennwörter. In diesem Fall müssen Sie eine Ausnahme für jedes Skype Raum Systemen v2-Benutzerkonto zu erstellen.
  
5. Klicken Sie auf **Fertig stellen**, um das Konto zu erstellen.
    
6. Führen Sie nach der Erstellung des Kontos eine Verzeichnissynchronisierung aus. Wechseln Sie nach Abschluss der Synchronisierung zur Benutzerseite, und vergewissern Sie sich, dass die beiden in den vorherigen Schritten erstellten Konten zusammengeführt wurden.
    
7. Zum Anwenden einiger Kontoeinstellungen müssen Sie eine Verbindung mit Azure AD herstellen. Sie können dieses Cmdlet ausführen, um die Verbindung herzustellen.
    
   ```
   Connect-MsolService -Credential $cred
   ```

### <a name="add-an-email-address-for-your-on-premises-domain-account"></a>Hinzufügen einer E-Mail-Adresse für Ihr lokales Domänenkonto

1. In **Active Directory-Benutzer und-Computer AD** -Tool mit der rechten Maustaste auf den Ordner oder die Organisationseinheit, dass die Skype Raum Systeme v2-Konten erstellt werden, klicken Sie auf **neu**, und klicken Sie dann auf **Benutzer**.
    
2. Geben Sie den Anzeigenamen aus dem vorherigen Cmdlet in das Feld **Vollständiger Name** und den Alias in das Feld **Benutzeranmeldename** ein. Klicken Sie auf **Weiter**.
    
### <a name="assign-an-office-365-license"></a>Zuweisen einer Office 365-Lizenz

1. Das Benutzerkonto muss eine gültige Office 365-Lizenz, um sicherzustellen, dass Exchange und Skype für Business Server 2015 funktioniert haben. Wenn Sie die Lizenz haben, müssen Sie einen Verwendungsspeicherort Ihres Benutzerkontos zuweisen – diese Einstellung bestimmt, was Lizenz-SKUs für Ihr Konto zur Verfügung stehen.
    
2. Im nächsten Schritt verwenden Sie Get-MsolAccountSku, um eine Liste der verfügbaren SKUs für Office 365-Mandanten abzurufen.
    
3. Wenn Sie die SKUs aufgelistet haben, können Sie mit dem Cmdlet „Set-MsolUserLicense“ eine Lizenz hinzufügen. In diesem Fall entspricht „$strLicense“ dem angezeigten SKU-Code (zum Beispiel „contoso:STANDARDPACK“).
    
   ```
   Set-MsolUser -UserPrincipalName 'PROJECTRIGEL01@contoso.com' -UsageLocation 'US'
   Get-MsolAccountSku
   Set-MsolUserLicense -UserPrincipalName 'PROJECTRIGEL01@contoso.com' -AddLicenses $strLicense
   ```

### <a name="enable-the-user-account-with-skype-for-business-server-2015"></a>Aktivieren des Benutzerkontos in Skype for Business Server 2015

1. Erstellen Sie eine Windows PowerShell-Remotesitzung von einem PC wie folgt:
    
  ```
  Import-Module LyncOnlineConnector  
$cssess=New-CsOnlineSession -Credential $cred  
Import-PSSession $cssess -AllowClobber

  ```

2. Führen Sie diesen Befehl, um Ihr Skype Raum Systemen v2-Konto für Skype für Business Server 2015 zu aktivieren:
    
   ```
   Enable-CsMeetingRoom -Identity $rm -RegistrarPool'sippoolbl20a04.infra.lync.com' -SipAddressType EmailAddress
   ```

    Wenn Sie nicht genau wissen, welcher Wert für den Parameter RegistrarPool in Ihrer Umgebung verwendet wird, können Sie den Wert aus einer vorhandenen Skype für Business Server 2015 Benutzer mit diesem Befehl abrufen.
    
   ```
   Get-CsOnlineUser -Identity 'alice@contoso.com'| fl *registrarpool*
   ```

### <a name="assign-a-skype-for-business-server-2015-license-to-your-skype-room-systems-v2-account"></a>Zuweisen einer Skype for Business Server 2015-Lizenz zu Ihrem Skype Room Systems v2-Konto

1. Melden Sie sich als mandantenadministrator an, öffnen Sie die administrativen Office 365-Portal, und klicken Sie auf die Admin-app.
    
2. Klicken Sie auf **Benutzer und Gruppen** und dann auf **Benutzer hinzufügen, Kennwörter zurücksetzen und mehr**.
    
3. Klicken Sie auf das Konto Skype Raum Systemen v2, und klicken Sie dann auf das Stiftsymbol, um die Kontoinformationen zu bearbeiten.
    
4. Klicken Sie auf **Lizenzen**.
    
5. Wählen Sie in **Lizenzen zuweisen** abhängig von Ihren Anforderungen für Lizenzen und für Enterprise-VoIP entweder Skype for Business (Plan 2) oder Skype for Business (Plan 3) aus. Sie müssen eine Lizenz planen 3 verwenden, falls Sie Enterprise-VoIP für Ihre Skype Raum Systemen v2 verwenden möchten.
    
6. Klicken Sie auf **Speichern**.
    
Für die Validierung sollten Sie alle Skype für Business-Client verwenden Sie dieses Konto anzumelden sein.
  
## <a name="see-also"></a>Siehe auch

#### 

[Planen von Skype Raum Systemen v2](../../plan-your-deployment/clients-and-devices/skype-room-systems-v2-0.md)
  
[Bereitstellen von Skype Raum Systemen v2](room-systems-v2.md)
  
[Konfigurieren einer Skype Raum Systemen v2-Konsole](console.md)
  
[Verwalten von Skype Raum Systemen v2](../../manage/skype-room-systems-v2/skype-room-systems-v2.md)
