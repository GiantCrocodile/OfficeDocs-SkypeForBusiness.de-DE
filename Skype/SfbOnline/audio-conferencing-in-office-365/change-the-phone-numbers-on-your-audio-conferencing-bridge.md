---
title: "Ändern Sie die Telefonnummern für die Audiokonferenz-Brücke"
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.date: 01/22/2018
ms.topic: article
ms.assetid: 6403f6d1-c05a-44ab-a6e0-558000e246f4
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
ms.collection: Adm_Skype4B_Online
ms.audience: Admin
appliesto:
- Skype for Business
- Microsoft Teams
localization_priority: Normal
f1keywords: None
ms.custom:
- Strat_SB_PSTN
- Audio Conferencing
description: "Wenn Sie Lizenzen für Audiokonferenzen erwerben, hostet Microsoft Ihre Audiokonferenzbrücke für Ihre Organisation. Die Audiokonferenzbrücke gibt Einwahlnummern von verschiedenen Standorten aus, damit die Besprechungsorganisatoren und die Teilnehmer über ein Telefon an Skype for Business- oder Microsoft Teams-Besprechungen teilnehmen können."
ms.openlocfilehash: 21603ebc5ea710598a1af70a66fe4388e206cea9
ms.sourcegitcommit: 94e32f776364b0aaefe2d2d72062ec1c249eaef3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2018
---
# <a name="change-the-phone-numbers-on-your-audio-conferencing-bridge"></a>Ändern Sie die Telefonnummern für die Audiokonferenz-Brücke

Wenn Sie Lizenzen für **Audiokonferenzen** erwerben, hostet Microsoft Ihre *Audiokonferenzbrücke*  für Ihre Organisation. Die Audiokonferenzbrücke gibt Einwahlnummern von verschiedenen Standorten aus, damit die Besprechungsorganisatoren und die Teilnehmer über ein Telefon an Skype for Business- oder Microsoft Teams-Besprechungen teilnehmen können.
  
Neben die Telefonnummern, die Konferenzbrücke bereits zugewiesen, Sie können [zusätzliche Service Zahlen abrufen](../what-is-phone-system-in-office-365/getting-service-phone-numbers.md) (gebührenpflichtige und gebührenfreie Nummern für die Audiokonferenz verwendet) aus anderen Speicherorten und weisen Sie anschließend, damit Sie können zu Live Meeting-Brücke, Erweitern Sie Abdeckung für Ihre Benutzer.
  
> [!NOTE]
> Um eine Rufnummer für ein Konferenzbrücke zuweisen/aufheben können, muss die Rufnummer eine Zahl "*Dienst*". Sie können den Typ der Zahl ist, navigieren Sie zur **VoIP**finden Sie unter > **Telefonnummern** und suchen Sie in der Spalte **' Zahl '** . Office 365 Communications haben muss zuerst, damit Benutzer, die eine gebührenfreie Telefonnummer-Brücke einwählen festgelegt werden. 
  
## <a name="steps-when-you-are-assigning-a-new-service-phone-number-to-your-conference-bridge"></a>Schritte zum Zuweisen einer neuen Servicetelefonnummer zu Ihrer Konferenzbrücke

### <a name="step-1---assign-the-new-phone-number-to-your-audio-conferencing-bridge"></a>Schritt 1 - Zuweisen der neuen Telefonnummer zu Ihrer Audiokonferenzbrücke

1. Melden Sie sich bei Office 365 mit Ihrem Geschäftskonto an.
    
2. Navigieren Sie zu **Office 365 Admin Center** > **Admin Center** > **Skype for Business** > **VoIP** > **Telefonnummern**.
    
3. Wählen Sie die Telefonnummer aus der Liste aus, und klicken Sie im Aktionsbereich auf **Zuweisen**.
    
4. Klicken Sie auf der Seite **Zuweisen** auf **Speichern**.
    
    Für Ihre Konferenzbrücke kann nur eine gebührenpflichtige Servicenummer als Standardnummer festgelegt werden. **Gebührenfreie Servicenummern können nicht als Standardnummer für Ihre Konferenzbrücke festgelegt werden**. Wenn Sie eine gebührenpflichtige Servicenummer zuweisen und diese als neue Standardnummer für Ihre Audiokonferenzbrücke festlegen möchten, müssen Sie die Option **Diese Nummer als Standardnummer verwenden** auswählen.
    
    > [!NOTE]
    > Nachdem eine neue Telefonnummer zugewiesen wurde, ändert sich die Standardnummer für vorhandene Benutzer nicht, selbst wenn die Nummer als neue Standardnummer festgelegt wurde. Legen Sie die standardmäßige gebührenpflichtige oder eine gebührenfreie Telefonnummer, die hinzugefügt wird, um Organisator der Besprechung eingeladen werden, finden Sie unter [Einrichten des Telefons, Zahlen auf enthalten lädt](set-the-phone-numbers-included-on-invites.md). 
  
### <a name="step-2---change-the-default-phone-numbers-that-are-included-in-the-meeting-invites-of-users-optional"></a>Schritt 2 - Ändern der Standardrufnummern, die in den Besprechungseinladungen von Benutzern enthalten sind (optional)

Bei den Standardtelefonnummern für Benutzer handelt es sich um die Nummern, die in ihren Besprechungseinladungen enthalten sind, wenn sie eine Besprechung planen. Weitere Informationen finden Sie unter [Einrichten des Telefons, Zahlen auf enthalten lädt](set-the-phone-numbers-included-on-invites.md).
  
1. Melden Sie sich bei Office 365 mit Ihrem Firmen- oder Schulkonto an.
    
2. Go to the **Office 365 admin center** > **Admin centers** > **Skype for Business** > **Audio conferencing** > **Users** and select the users in the list.
    
3. Klicken Sie im Aktionsbereich auf **Bearbeiten**.
    
4. Wählen Sie unter **Gebührenpflichtige Standardnummer** oder **Gebührenfreie Standardnummer** die Nummer in der Liste aus, und klicken Sie auf **Speichern**.
    
Nach dem Speichern der Änderungen sind die neuen Standardtelefonnummern in den Besprechungseinladungen der Organisatoren enthalten, wenn diese zum nächsten Mal eine neue Besprechung planen.
  
### <a name="step-3---update-existing-meeting-invites-of-users-using-the-meeting-migration-service-optional"></a>Schritt 3 - Aktualisieren vorhandener Besprechungseinladungen von Benutzern mit Meeting Migration Service (optional)

Für die nächsten beiden Schritte müssen Sie Windows PowerShell zu starten.
  
Mit Meeting Migration Service können Sie optional Besprechungseinladungen aktualisieren, die bereits vor der Änderung der Standardtelefonnummern an Benutzer in Ihrer Organisation gesendet wurden. Weitere Informationen finden Sie unter [Einrichten des Meeting Migration Service (MMS)](setting-up-the-meeting-migration-service-mms.md).
  
- Führen Sie Meeting Migration Service (MMS) für die Benutzer aus, deren Standardtelefonnummern in Schritt 2 geändert wurden. Führen Sie dazu den folgenden Befehl aus:
    
```
    Start-CsExMeetingMigration user@contoso.com

```

- Sie können auch den Status der Besprechungsmigration anzeigen. Alle Besprechungen werden neu geplant, sobald keine Vorgänge mit dem Status  *Ausstehend*  oder *In Bearbeitung*  mehr vorhanden sind.
    
```
    Get-CsMeetingMigrationStatus -SummaryOnly
```

## <a name="steps-when-you-are-unassigning-a-service-phone-number-for-a-conferencing-bridge"></a>Schritte zum Aufheben der Zuweisung einer Servicetelefonnummer für eine Konferenzbrücke


Wenn Sie die Zuweisung einer Telefonnummer zu einer Konferenzbrücke aufheben, können die Benutzer nicht mehr über diese Telefonnummer an Besprechungen teilnehmen. Aufgrund der Telefonnummernänderung ist es wichtig, alle Benutzer zu aktualisieren, die eine Telefonnummer als Standardnummer haben können (falls vorhanden). Außerdem müssen Sie die vorhandenen Besprechungseinladungen dieser Benutzer aktualisieren, bevor die Zuweisung der Telefonnummer zur Audiokonferenzbrücke aufgehoben wird. 
  
Wenn die Rufnummer ohne Aktualisierung der Benutzer und ihrer Besprechungen entfernt wird, enthalten die vorhandenen Besprechungseinladungen dieser Benutzer möglicherweise eine Rufnummer, die für die Teilnahme an Besprechungen nicht mehr funktioniert.
  
Für die ersten drei Schritte müssen Sie Windows PowerShell zu starten. Um herauszufinden, wie Sie dies tun, klicken Sie auf [möchten Sie wissen, wie Sie mit Windows PowerShell verwalten?](change-the-phone-numbers-on-your-audio-conferencing-bridge.md#bkPowerShell)
  
### <a name="step-1---update-users-that-have-the-phone-number-to-be-unassigned-as-one-of-their-default-numbers"></a>Schritt 1 - Aktualisieren von Benutzern, für die die Rufnummer, deren Zuweisung aufgehoben werden soll, als Standardnummer festgelegt ist

Ersetzen Sie die gebührenpflichtige oder gebührenfreie Standardnummer für alle Benutzer, für die die Nummer, deren Zuweisung aufgehoben werden soll, als Standardnummer festgelegt ist. Starten Sie den Prozess zum Neuplanen der Besprechungen dieser Benutzer. Führen Sie dazu den folgenden Befehl aus:
  
```
Set-CsOnlineDialInConferencingUserDefaultNumber -FromNumber <Number to be removed> -ToNumber <Number to be set as new default> -NumberType <"Toll" or "Toll-Free"> -RescheduleMeetings
```
 > [!IMPORTANT] 
 >Sie können auch die Standard gebührenpflichtige oder gebührenfreie Anzahl von Benutzern in der Skype für Business Administrationscenter ändern. Allerdings werden nicht dies automatisch ihre Besprechungen neu planen. 
 
 Weitere Informationen finden Sie unter [Einrichten des Telefons, die Zahlen enthalten auf invites](set-the-phone-numbers-included-on-invites.md).

  > [!NOTE]
  > Je nach Größe Ihrer Organisation kann es eine Weile dauern, bis dieser Vorgang abgeschlossen ist. 
  
### <a name="step-2---view-meeting-migration-status-using-windows-powershell"></a>Schritt 2 - Anzeigen des Status der Besprechungsmigration mit Windows PowerShell

Alle Besprechungen werden neu geplant werden, nachdem es keine Vorgänge im Zustand *ausstehenden* oder *In Bearbeitung sind* .
  
```
Get-CsMeetingMigrationStatus -SummaryOnly
```

Weitere Informationen zu Meeting Migration Service finden Sie unter [Einrichten des Meeting Migration Service (MMS)](setting-up-the-meeting-migration-service-mms.md).
  
### <a name="step-3---unassign-the-old-phone-number-from-the-audio-conferencing-bridge"></a>Schritt 3 - Aufheben der Zuweisung der alten Telefonnummer zur Audiokonferenzbrücke

1. Melden Sie sich bei Office 365 mit Ihrem Firmen- oder Schulkonto an.
    
2. Navigieren Sie zu **Office 365 Admin Center** > **Admin Center** > **Skype for Business** > **VoIP** > **Telefonnummern**.
    
3. Wählen Sie die Telefonnummer aus der Liste aus, und klicken Sie im Aktionsbereich auf **Zuweisung aufheben**.
    
4. Klicken Sie im Bestätigungsfenster auf **Ja**.
    
  > [!IMPORTANT]
  > Nachdem die Zuweisung einer Telefonnummer zu einer Audiokonferenzbrücke aufgehoben wurde, ist die Telefonnummer nicht mehr für die Teilnahme der Benutzer an neuen oder bestehenden Besprechungen verfügbar. 
  
## <a name="want-to-know-how-to-manage-with-windows-powershell"></a>Möchten Sie wissen, wie Sie die Verwaltung mit Windows PowerShell organisieren?
<a name="bkPowerShell"> </a>

### <a name="to-verify-that-windows-powershell-is-ready-to-go"></a>So überprüfen Sie, ob Windows PowerShell bereit ist

 **Überprüfen, ob Windows PowerShell 3.0 oder höher ausgeführt wird**
  
1. To verify that you are running version 3.0 or higher: **Start Menu** > **Windows PowerShell**.
    
2. Überprüfen Sie die Version, indem Sie im Fenster _Windows PowerShell_ die Zeichenfolge **Get-Host** eingeben.
    
3. Wenn Sie nicht über Version 3.0 oder eine höhere Version verfügen, müssen Sie Updates für Windows PowerShell herunterladen und installieren. Informationen zum Herunterladen von Windows PowerShell und zum Aktualisieren auf Version 4.0 finden Sie unter [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/?LinkId=716845). Starten Sie Ihren Computer neu, wenn Sie dazu aufgefordert werden.
    
4. Sie müssen auch das Windows PowerShell-Modul für Skype for Business Online installieren, mit dem Sie eine Windows PowerShell-Remotesitzung erstellen können, die eine Verbindung mit Skype for Business Online herstellt. Dieses Modul, das nur auf 64-Bit-Computern unterstützt wird, kann aus dem Microsoft Download Center unter [Windows PowerShell-Modul für Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=294688) heruntergeladen werden. Starten Sie Ihren Computer neu, wenn Sie dazu aufgefordert werden.
    
Weitere Informationen finden Sie unter [Verbinden mit allen Office 365-Diensten in einem einzigen Windows PowerShell-Fenster](https://technet.microsoft.com/EN-US/library/dn568015.aspx).
  
### <a name="to-start-windows-powershell"></a>So starten Sie Windows PowerShell

 **Starten einer Windows PowerShell-Sitzung**
  
1. From the **Start Menu** > **Windows PowerShell**.
    
2. Stellen Sie im Fenster **Windows PowerShell** eine Verbindung mit Ihrer Office 365-Organisation her, indem Sie Folgendes ausführen:
    
    > [!NOTE]
    > Sie müssen den Befehl **Import-Module** nur bei der ersten Verwendung des Windows PowerShell-Moduls für Skype for Business Online ausführen.
  
> 
  ```
    Import-Module "C:\\Program Files\\Common Files\\Skype for Business Online\\Modules\\SkypeOnlineConnector\\SkypeOnlineConnector.psd1"
    $credential = Get-Credential
    $session = New-CsOnlineSession -Credential $credential
    Import-PSSession $session
  ```

Wenn Sie weitere Informationen zu Windows PowerShell starten möchten, finden Sie unter [Connect auf alle Office 365-Dienste in einem einzelnen Windows PowerShell-Fenster](https://technet.microsoft.com/EN-US/library/dn568015.aspx) oder [Herstellen einer Verbindung mit Skype für Business Online mithilfe von Windows PowerShell](https://technet.microsoft.com/en-us/library/dn362795%28v=ocs.15%29.aspx).
  
### <a name="save-time-or-automate"></a>Zeit sparen oder Automatisieren des Vorgangs

Um Zeit zu sparen bzw. den Vorgang zu automatisieren, können Sie das Cmdlet [Set-CsOnlineDialInConferencingUser](http://go.microsoft.com/fwlink/?LinkId=617688) oder **Set-CsOnlineDialInConferencingUserDefaultNumber** nutzen.
  
- Mit dem Cmdlet [Set-CsOnlineDialInConferencingUser](http://go.microsoft.com/fwlink/?LinkId=617688) können Sie die gebührenpflichtige oder gebührenfreie Standardnummer für spezifische Benutzer ändern.
    
  - Führen Sie Folgendes aus, um die gebührenfreie Standardnummer für einen Benutzer zu ändern:
    
  ```
  Set-CsOnlineDialinConferencingUser -Identity amos.marble@Contoso.com -TollFreeServiceNumber   80045551234
  ```

- Ändern Sie mit dem Cmdlet **Set-CsOnlineDialInConferencingUserDefaultNumber** die gebührenpflichtige oder gebührenfreie Nummer für Benutzer auf Basis ihrer ursprünglichen Standardnummer oder ihres Standorts.
    
    > [!NOTE]
    > Die BridgeID finden Sie mithilfe von **Get-CsOnlineDialInConferencingBridge**.
  
  - So ändern Sie die gebührenpflichtige Standardnummer für alle Benutzer bis auf einen in 8005551234:
    
  ```
  Set-CsOnlineDialInConferencingUserDefaultNumber -FromNumber $null -ToNumber 8005551234 -NumberType TollFree -BridgeId <Bridge Id>  
  ```

  - Führen Sie Folgendes aus, um die gebührenfreie Standardnummer aller Benutzer mit der gebührenfreien Standardnummer 8005551234 in 8005551239 zu ändern und die Besprechungen der Benutzer automatisch neu zu planen:
    
  ```
  Set-CsOnlineDialInConferencingUserDefaultNumber -FromNumber 8005551234 -ToNumber 8005551239 NumberType TollFree -BridgeId <Bridge Id> -RescheduleMeetings
  ```

  - Führen Sie Folgendes aus, um die gebührenfreie Standardnummer aller Benutzer in den USA in 8005551234 zu ändern und ihre Besprechungen automatisch neu zu planen:
    
  ```
  Set-CsOnlineDialInConferencingUserDefaultNumber -Country US -ToNumber 8005551234 -NumberType TollFree -BridgeId <Bridge Id> -RescheduleMeetings
  ```

    > [!NOTE]
    > Der oben verwendete Standort muss mit den im Office 365 Admin Center festgelegten Kontaktinformationen der jeweiligen Benutzer übereinstimmen. 
  
## <a name="about-windows-powershell"></a>Informationen zu Windows PowerShell

In Bezug auf Windows PowerShell geht es um das Verwalten von Benutzern und darum, was Benutzer tun dürfen und was nicht. Mit Windows PowerShell können Sie Office 365 und Skype for Business Online zentral verwalten. Dies kann Ihre tägliche Arbeit vereinfachen, wenn Sie mehrere Aufgaben ausführen müssen. Informationen zu den ersten Schritten mit Windows PowerShell finden Sie unter den folgenden Themen:
    
  - [Einführung in Windows PowerShell und Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525039)
    
  - [Warum Sie Office 365 PowerShell verwenden müssen](https://go.microsoft.com/fwlink/?LinkId=525041)
    
Windows PowerShell verfügt im Vergleich zur ausschließlichen Verwendung des Office 365 Admin Centers über viele Vorteile in puncto Geschwindigkeit, Einfachheit und Produktivität, beispielsweise wenn Sie Einstellungsänderungen für viele Benutzer gleichzeitig vornehmen. Informationen zu diesen Vorteilen finden Sie unter den folgenden Themen:
    
  - [Beste Möglichkeiten zum Verwalten von Office 365 mit der Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=525142)
    
  - [Verwenden von Windows PowerShell zum Verwalten von Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525453)
    
  - [Verwenden von Windows PowerShell für die Durchführung gängiger Verwaltungsaufgaben von Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525038)

## <a name="related-topics"></a>See Also
[Ändern der Einstellungen für eine Audiokonferenzbrücke](change-the-settings-for-an-audio-conferencing-bridge.md)
  