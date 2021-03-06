---
title: Ändern der Einstellungen für eine Audiokonferenzbrücke
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.topic: article
ms.assetid: 783fad3f-b77c-422b-b91f-7c8b0af324fb
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
- M365-voice
- M365-collaboration
audience: Admin
appliesto:
- Skype for Business
- Microsoft Teams
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Audio Conferencing
- ms.teamsadmincenter.audioconferencing.bridgesettings
- seo-marvel-mar2020
description: Ändern Sie die Einstellungen für die Audiokonferenz-Bridge, einschließlich ein-und Ausstiegs Benachrichtigungen, Wiedergeben von Namen oder Telefonnummern, Töne, und fordern Sie Anrufer auf, Ihren Namen aufzuzeichnen.
ms.openlocfilehash: acebe42e8dbc5707238975c34ce97961c1493d91
ms.sourcegitcommit: 1807ea5509f8efa6abba8462bce2f3646117e8bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2020
ms.locfileid: "44690911"
---
# <a name="change-the-settings-for-an-audio-conferencing-bridge"></a>Ändern der Einstellungen für eine Audiokonferenzbrücke

Wenn Sie Audiokonferenzen in Microsoft 365 oder Office 365 einrichten, erhalten Sie Telefonnummern für Ihre Benutzer von der sogenannten Audiokonferenz-Brücke. Eine Konferenzbrücke kann eine oder mehrere Telefonnummern umfassen. Diese Telefonnummern werden verwendet, wenn Anrufer sich in eine Besprechung einwählen. Die Telefonnummer ist am Ende der Skype for Business- oder Microsoft Teams-Besprechungseinladung zu finden.
  
Die Konferenzbrücke nimmt den Anruf an und gibt Sprachanweisungen einer automatischen Telefonzentrale aus. Je nach Ihren Einstellungen kann sie dann Benachrichtigungen wiedergeben, Anrufer auffordern, ihren Namen aufzuzeichnen, und die PIN-Einstellungen steuern. Besprechungsorganisatoren erhalten PINs, damit sie eine Besprechung starten können, wenn sie keine Skype for Business- oder Microsoft Teams-App verwenden.

  > [!IMPORTANT]
  > Der Besprechungsorganisator benötigt nur dann eine PIN, wenn die Besprechung nicht bereits von einem Benutzer einer Skype for Business- oder Microsoft Teams-App gestartet wurde. Wenn sich alle Teilnehmer in die Besprechung einwählen, benötigt der Besprechungsorganisator die PIN zum Starten der Besprechung. 

> [!NOTE]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

## <a name="an-icon-showing-the-microsoft-teams-logo-using-the-microsoft-teams-admin-center"></a>![Symbol, das das Microsoft Teams-Logo zeigt](media/teams-logo-30x30.png) Verwenden des Microsoft Teams Admin Centers

1. Wechseln Sie in der linken Navigationsleiste zu **Besprechungen**  >  **Konferenz Brücken**. 

2. Klicken Sie oben auf der Seite **Konferenz Brücken** auf **Brücken Einstellungen**. 

3. Wählen Sie im Bereich **Bridge Settings** die folgenden Optionen aus: 
   - **Besprechungs-und Exit-Benachrichtigungen** Wenn Sie diese Option deaktivieren, werden Benutzer, die der Besprechung bereits beigetreten sind, nicht benachrichtigt, wenn jemand die Besprechung eingibt oder verlässt.
    
     Wenn Sie Besprechungs- **und Beendigungs Benachrichtigungen**aktivieren, können Sie die folgenden Optionen auswählen:
    
   - **Names or phone numbers** (Namen oder Telefonnummern): Wenn sich Benutzer in eine Besprechung einwählen und teilnehmen, wird ihre Telefonnummer wiedergegeben.
    
   - **Tones** (Töne): Wenn sich Benutzer in eine Besprechung einwählen und teilnehmen, wird ein Ton wiedergegeben.
      
   - **Bitten Sie die Anrufer, Ihren Namen aufzuzeichnen, bevor Sie der Besprechung beitreten** . Wenn Sie diese Option deaktivieren, werden Anrufer nicht aufgefordert, Ihren Namen aufzuzeichnen, bevor Sie an einer Besprechung teilnehmen.

4. Wenn Sie die PIN-Länge für Besprechungen festlegen möchten, wählen Sie die Anzahl der Ziffern für die PIN in der Liste **PIN-Länge** aus.

5. Wenn Sie angeben möchten, ob e-Mails an Ihre Benutzer gesendet werden sollen, aktivieren oder deaktivieren Sie **automatisch e-Mails an Benutzer senden, wenn sich Ihre Audiokonferenz-Konfiguration ändert**.
    Weitere Informationen finden Sie unter [e-Mails, die automatisch an Benutzer gesendet werden, wenn sich Ihre audiokonferenzeinstellungen in Microsoft Teams ändern](emails-sent-to-users-when-their-settings-change-in-teams.md) oder [e-Mails an Benutzer gesendet werden, wenn sich Ihre Einstellungen in Skype for Business Online ändern](/SkypeForBusiness/audio-conferencing-in-office-365/emails-sent-to-users-when-their-settings-change) .
 
6. Klicken Sie auf **Speichern**. 


## <a name="an-icon-showing-the-skype-for-business-logo--using-the-skype-for-business-admin-center"></a>![Ein Symbol mit dem Skype for Business-Logo](media/sfb-logo-30x30.png)  Verwenden des Skype for Business Admin Center

 **Festlegen des Besprechungsverhaltens, wenn Anrufer an einer Besprechung teilnehmen**
    
1. Wechseln Sie im **Skype for Business Admin Center**in der linken Navigationsleiste zu **Audiokonferenz-**  >  **Einstellungen von Microsoft Bridge**.
    
2. Wählen Sie auf der Seite **Einstellungen von Microsoft Bridge** unter **Besprechungsteilnahme** Folgendes aus:
    
   - **Benachrichtigungen beim Betreten oder Verlassen einer Besprechung aktivieren**: Diese Option ist standardmäßig aktiviert. Wenn Sie das Kontrollkästchen deaktivieren, werden Benutzer, die bereits an der Besprechung teilnehmen, nicht benachrichtigt, wenn ein Teilnehmer der Besprechung beitritt oder diese verlässt.
    
   - Bei Auswahl von **Benachrichtigungen beim Betreten oder Verlassen einer Besprechung aktivieren** können Sie diese Optionen in der Liste **Entry/exit announcement type** (Typ der Benachrichtigung bei Zu- oder Abgang) auswählen:
    
   - **Names or phone numbers** (Namen oder Telefonnummern): Wenn sich Benutzer in eine Besprechung einwählen und teilnehmen, wird ihre Telefonnummer wiedergegeben.
    
   - **Tones** (Töne): Wenn sich Benutzer in eine Besprechung einwählen und teilnehmen, wird ein Ton wiedergegeben.
  
   - **Anrufer zur Aufnahme ihres Namens auffordern, bevor sie an der Besprechung teilnehmen**: Diese Option ist standardmäßig aktiviert. Wenn Sie das Kontrollkästchen deaktivieren, werden Anrufer nicht aufgefordert, ihren Namen aufzuzeichnen, bevor sie an der Besprechung teilnehmen.
    
3. Nachdem Sie die Änderungen vorgenommen haben, klicken Sie auf **Speichern**.
    
**Festlegen der Länge der PIN für Besprechungen**
  
1. Mit Ihrem Firmen-oder Schulkonto anmelden
    
2. Navigieren Sie zum **Microsoft 365 Admin Center** > **Skype for Business**.
    
3. Wechseln Sie im **Skype for Business Admin Center**in der linken Navigationsleiste zu **Audiokonferenz-**  >  **Einstellungen für Microsoft Bridge**.
    
4. Geben Sie auf der Seite **Einstellungen von Microsoft Bridge** unter **Sicherheit** in der Liste **PIN-Länge** die gewünschte Anzahl der Ziffern für die PIN ein, und klicken Sie dann auf **Speichern**.
    
    > [!IMPORTANT]
    > Die PIN muss aus 4 bis 12 Ziffern bestehen. 
  
**Auswählen, ob E-Mails an Ihre Benutzer gesendet werden sollen**
  
1. Mit Ihrem Firmen-oder Schulkonto anmelden
    
2. Navigieren Sie zum **Microsoft 365 Admin Center** > **Skype for Business**.
    
3. Wechseln Sie im **Skype for Business Admin Center**in der linken Navigationsleiste zu **Audiokonferenz-**  >  **Einstellungen für Microsoft Bridge**.
    
4. Aktivieren oder deaktivieren Sie auf der Seite **Einstellungen von Microsoft Bridge** **automatisch e-Mails an Benutzer senden, wenn sich Ihre Einwahlinformationen ändern**, und klicken Sie dann auf **Speichern**.
    
    Weitere Informationen finden Sie unter [e-Mails, die automatisch an Benutzer gesendet werden, wenn sich Ihre audiokonferenzeinstellungen in Microsoft Teams ändern](emails-sent-to-users-when-their-settings-change-in-teams.md) oder [e-Mails an Benutzer gesendet werden, wenn sich Ihre Einstellungen in Skype for Business Online ändern](/SkypeForBusiness/audio-conferencing-in-office-365/emails-sent-to-users-when-their-settings-change) .
    
## <a name="want-to-know-how-to-manage-with-windows-powershell"></a>Möchten Sie wissen, wie Sie die Verwaltung mit Windows PowerShell organisieren?

- Um Zeit zu sparen bzw. den Vorgang zu automatisieren, können Sie das Cmdlet [Set-CsDialinConferencingBridge](https://go.microsoft.com/fwlink/?LinkId=617686) nutzen.
    
- Bei Windows PowerShell dreht sich alles um das Verwalten von Benutzern und Funktionen, die Benutzer verwenden oder nicht verwenden können. Mit Windows PowerShell können Sie Microsoft 365 oder Office 365 mit einem zentralen Verwaltungspunkt verwalten, der Ihre tägliche Arbeit vereinfachen kann, wenn mehrere Aufgaben ausgeführt werden müssen. Informieren Sie sich in den folgenden Themen über die Verwendung von Windows PowerShell:
    
  - [Warum Sie Office 365 PowerShell verwenden müssen](https://go.microsoft.com/fwlink/?LinkId=525041)
    
  - [Beste Möglichkeiten zum Verwalten von Microsoft 365 oder Office 365 mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=525142)
    
- Windows PowerShell bietet zahlreiche Vorteile bei der Geschwindigkeit, Einfachheit und Produktivität, wenn Sie nur das Microsoft 365 Admin Center verwenden, beispielsweise wenn Sie für viele Benutzer gleichzeitig Einstellungsänderungen vornehmen. Informationen zu diesen Vorteilen finden Sie unter den folgenden Themen: 
    
  - [Einführung in Windows PowerShell und Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525039)
    
  - [Verwenden von Windows PowerShell zum Verwalten von Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525453)
    
  - [Verwenden von Windows PowerShell für die Durchführung gängiger Verwaltungsaufgaben von Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525038)
    
    > [!NOTE]
    > Mithilfe des Windows PowerShell-Moduls für Skype for Business Online können Sie eine Windows PowerShell-Remotesitzung erstellen, bei der eine Verbindung mit Skype for Business Online hergestellt wird. Dieses Modul, das nur von 64-Bit-Computern unterstützt wird, kann im Microsoft Download Center unter [Windows PowerShell-Modul für Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=294688) heruntergeladen werden.
  
## <a name="related-topics"></a>Verwandte Themen

[Einrichten von Audiokonferenzen für Microsoft Teams](set-up-audio-conferencing-in-teams.md)

[Einrichten von Audiokonferenzen für Skype for Business Online](/skypeforbusiness/audio-conferencing-in-office-365/set-up-audio-conferencing)
