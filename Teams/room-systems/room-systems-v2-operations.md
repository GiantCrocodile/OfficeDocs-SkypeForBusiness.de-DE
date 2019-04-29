---
title: Microsoft-Teams Chatrooms Wartung und Betrieb
ms.author: jambirk
author: jambirk
ms.reviewer: davgroom
manager: serdars
ms.date: 5/10/2018
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
ms.collection: M365-voice
localization_priority: Normal
description: Lesen Sie in diesem Thema, um Informationen zur Verwaltung von der Microsoft-Teams Chatrooms, die nächste Generation von Skype Raum Systemen zu erfahren.
ms.openlocfilehash: efaf2a1bae7980855501b826d6a2ee902f0f56b2
ms.sourcegitcommit: 79ec789a22acf1686c33a5cc8ba3bd50049f94b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2019
ms.locfileid: "33362854"
---
# <a name="microsoft-teams-rooms-maintenance-and-operations"></a>Microsoft-Teams Chatrooms Wartung und Betrieb 
 
Lesen Sie in diesem Thema, um Informationen zur Verwaltung von der Microsoft-Teams Chatrooms, die nächste Generation von Skype Raum Systemen zu erfahren.
  
Microsoft-Teams Chatrooms ist Microsofts neueste konferenzlösung entwickelt, um Ihre Besprechungsraum in ein rich-collaborative Erlebnis umgewandelt. Benutzer werden die vertraute Microsoft-Teams, genießen oder Skype für Business-Schnittstelle und IT-Administratoren wird eine auf einfache Weise bereitgestellte und verwaltete Windows 10 Skype Besprechung app zu schätzen wissen. Microsoft-Teams Chatrooms ist darauf ausgelegt, vorhandene Ausrüstung, wie LCD-Bereiche zur Erleichterung der Installation auf die Microsoft-Teams oder Skype für Unternehmen in Ihrem Besprechungsraum bringen verwenden können.
  
Zusätzliche Konfiguration ist Remoteverwaltung möglich mit Microsoft Azure Monitor gemäß [Planen Microsoft Teams Chatrooms Management mit Azure Monitor](azure-monitor-plan.md), [Microsoft-Teams-Chatrooms bereitstellen Management mit Azure Monitor](azure-monitor-deploy.md), [Verwalten Microsoft-Teams Chatrooms Geräte mit Azure Monitor](azure-monitor-deploy.md). Sie können auch [verwalten Microsoft Teams Chatrooms Konsole Einstellungen Remote mit einer XML-Konfigurationsdatei](xml-config-file.md), einschließlich eines Designs benutzerdefinierte anzeigen. 
  
## <a name="collecting-logs-on-microsoft-teams-rooms"></a>Erfassen von Protokollen auf Microsoft Teams Räume
<a name="Logs"> </a>

Um die Protokolle gespeichert werden, müssen Sie das Protokoll Auflistung Skript aufrufen, das mit der Microsoft-Teams Chatrooms app verwendet werden soll. Starten Sie im Administratormodus eine Eingabeaufforderung mit erhöhten Rechten, und geben Sie den folgenden Befehl:
  
```
powershell -ExecutionPolicy unrestricted c:\rigel\x64\scripts\provisioning\ScriptLaunch.ps1 CollectSrsV2Logs.ps1
```

Die Protokolle werden als ZIP-Datei in c:\rigel ausgegeben werden.
  
## <a name="front-of-room-display-settings"></a>Anzeigeeinstellungen vorne im Raum
<a name="Display"> </a>

Konfigurieren Sie den Bildschirm vorne im Raum für den Modus „Erweitert“. Dadurch wird die Konsole sicherstellen, dass, die Benutzeroberfläche auf, die anzeigen nicht dupliziert werden, wenn Sie die Anzeige schalten.
  
> [!NOTE]
> Ein Consumer-TV, der als eine Anzeige vorne im Raum verwendet wird, muss das Feature „Consumer Electronics Control (CEC)“ von HDMI unterstützen/aktivieren, sodass ein automatischer Wechsel zu einer aktiven Videoquelle aus dem Standbymodus möglich ist. Dieses Feature wird nicht auf allen TVs unterstützt. 
  
## <a name="microsoft-teams-rooms-reset-factory-restore"></a>Microsoft-Teams, Räume zurücksetzen (Factory wiederherstellen)
<a name="Reset"> </a>

Wenn Microsoft Teams Chatrooms auch nicht ausgeführt wird, möglicherweise ausführen Herstellerstandard zurücksetzen helfen. Dies ist möglich, in der app Einstellungen auf der Registerkarte **Wiederherstellen** unter **diesem PC zurücksetzen**, wählen Sie **Erste Schritte**, und klicken Sie dann **Alles entfernen**. Führen Sie die verbleibenden aufforderungen, um das Gerät zurückzusetzen.
  
> [!NOTE]
> Es ist ein bekanntes Problem, in dem die Microsoft-Teams Räume werden kann nicht mehr verwendet werden, wenn die Option **Meine Dateien - Apps entfernt und Einstellungen, beibehalten werden sollen, jedoch bleibt Ihre persönlichen Dateien** während des Aktivierungsvorgangs zurücksetzen ausgewählt ist. Führen Sie _nicht_ verwenden Sie diese Option.
  
## <a name="supported-remote-options"></a>Unterstützte Remoteoptionen
<a name="RemoteOptions"> </a>

In der folgenden Tabelle sind die möglichen Remotevorgänge und die Methoden zusammengefasst, die Sie für diese Vorgänge verwenden können.
  

|**Arbeitsgruppe **|**Nicht Mitglied einer Domäne**|**Mitglied einer Domäne**|
|:-----|:-----|:-----|
|Neustart  <br/> |Remotedesktop  <br/> Remote-Powershell  <br/> |Remotedesktop (Weitere Konfiguration erforderlich)  <br/> Remote-Powershell (Weitere Konfiguration erforderlich)  <br/> SCCM  <br/> |
|Betriebssystemupdate  <br/> |Windows Update  <br/> |Windows Update  <br/> WSUS  <br/> |
|App-Update  <br/> |Windows Store  <br/> |Windows Store  <br/> SCCM  <br/> |
|Skype-Kontokonfiguration  <br/> |Zurzeit nicht unterstützt  <br/> |Zurzeit nicht unterstützt  <br/> |
|Zugriff auf Protokolle  <br/> |Zurzeit nicht unterstützt  <br/> |Zurzeit nicht unterstützt  <br/> |
   
## <a name="configuring-group-policy-for-microsoft-teams-rooms"></a>Konfigurieren von Gruppenrichtlinien für Microsoft-Teams, Räume
<a name="GroupPolicy"> </a>

In diesem Abschnitt werden die Systemeinstellungen, von denen Microsoft Teams Chatrooms abhängt, ordnungsgemäß behandelt. Wenn Microsoft Teams Chatrooms mit einer Domäne verknüpft wird, stellen Sie sicher, dass Ihre Gruppenrichtlinien die Einstellungen in der folgenden Tabelle außer Kraft setzen nicht.
  

|**Einstellung**|**Ermöglicht**|
|:-----|:-----|
|HKLM\Software\Microsoft\Windows NT\CurrentVersion\Winlogon automatische Anmeldung = (REG_SZ) 1  <br/> |Microsoft-Teams Chatrooms starten aktiviert  <br/> |
|Strom-Management -\> AC, deaktivieren Sie auf Bildschirm nach 10 Minuten  <br/> Strom-Management -\> auf AC, setzen Sie nie System in den Energiesparmodus  <br/> |Microsoft-Teams Chatrooms angefügte zeigt deaktivieren und Reaktivieren von automatisch aktiviert  <br/> |
|net accounts /maxpwage:unlimited  <br/> Oder entsprechende Möglichkeit zum Deaktivieren des Kennwortablaufs für das lokale Konto. Wird dies nicht ausgeführt, kann bei der Anmeldung des Skype-Kontos aufgrund eines abgelaufenen Kennworts ein Fehler auftreten. Beachten Sie, dass sich dies auf alle lokalen Konten auf dem Computer auswirkt, sodass bei Nichtfestlegung dieser Einstellung auch das Administratorkonto ablaufen kann.  <br/> |Ermöglicht die ständige Anmeldung des Skype-Kontos  <br/> |
   
Übertragen von Dateien mithilfe von Gruppenrichtlinien wird unter [Konfigurieren einer Dateielement](https://technet.microsoft.com/library/cc772536%28v=ws.11%29.aspx)erläutert.
  
## <a name="remote-management-using-powershell"></a>Remoteverwaltung mit PowerShell
<a name="RemotePS"> </a>

Sie können die folgenden Verwaltungsvorgänge Remote mithilfe von PowerShell ausführen (siehe Tabelle unten für Skriptbeispiele):
  
- Abrufen von angeschlossenen Geräten
    
- Abrufen des App-Status
    
- Abrufen von Systeminformationen
    
- Neustart des Systems
    
- Abrufen von Protokollen
    
- Übertragen von Dateien (einer Domäne gehörenden Microsoft Teams Chatrooms erforderlich)
    
> [!NOTE]
> Diese Funktion ist standardmäßig deaktiviert. Sie müssen zum Ausführen der folgenden Vorgänge remote-PowerShell für Ihre Umgebung auf dem System Microsoft Teams Räume zu aktivieren. Finden Sie in der Dokumentation auf **[Enable-psremoting sieht](https://technet.microsoft.com/library/hh849694.aspx)** für Informationen zur Verwendung von remote-PowerShell aktivieren.
  
Sie können Remote-PowerShell beispielsweise wie folgt aktivieren:
  
1. Melden Sie sich als Administrator auf einem Gerät mit Microsoft-Teams Chatrooms.
    
2. Öffnen Sie eine PowerShell-Eingabeaufforderung mit erhöhten Rechten.
    
3. Geben Sie den folgenden Befehl ein: Enable-PSRemoting -force
    
So führen Sie einen Verwaltungsvorgang durch:
  
1. Melden Sie sich an einem Computer mit den Anmeldeinformationen des Kontos, die Berechtigung zum Ausführen von PowerShell-Befehlen auf einem Gerät mit Microsoft-Teams Chatrooms.
    
2. Öffnen Sie eine reguläre PowerShell-Eingabeaufforderung auf dem PC.
    
3. Kopieren Sie den Befehlstext aus der folgenden Tabelle, und fügen Sie ihn an der Eingabeaufforderung ein.
    
4. Ersetzen Sie `<Device fqdn>` Felder mit den Werten des FQDN für Ihre Umgebung geeignet.
    
5. Ersetzen Sie * \<Pfad\> * mit den Dateinamen und den lokalen Pfad der master SkypeSettings.xml-Konfigurationsdatei (oder Bild Design).
    
Abzurufenden angeschlossene Geräte
  
```
invoke-command {Write-Host "VIDEO DEVICES:" 
gwmi -Class Win32_PnPEntity | where {$_.PNPClass -eq "Image"} | Format-Table Name,Status,Present; Write-Host "AUDIO DEVICES:" 
gwmi -Class Win32_PnPEntity | where {$_.PNPClass -eq "Media"} | Format-Table Name,Status,Present; Write-Host "DISPLAY DEVICES:" 
gwmi -Class Win32_PnPEntity | where {$_.PNPClass -eq "Monitor"} | Format-Table Name,Status,Present} -ComputerName <Device fqdn>
```

Abrufen des App-Status
  
```
invoke-command { $package = get-appxpackage -User Skype -Name Microsoft.SkypeRoomSystem; if ($package -eq $null) {Write-host "SkypeRoomSystems not installed."} else {write-host "SkypeRoomSystem Version : " $package.Version}; $process = Get-Process -Name "Microsoft.SkypeRoomSystem" -ErrorAction SilentlyContinue; if ($process -eq $null) {write-host "App not running."} else {$process | format-list StartTime,Responding}}  -ComputerName <Device fqdn>
```

Abrufen von Systeminformationen
  
```
invoke-command {gwmi -Class Win32_ComputerSystem | Format-List PartOfDomain,Domain,Workgroup,Manufacturer,Model
gwmi -Class Win32_Bios | Format-List SerialNumber,SMBIOSBIOSVersion} -ComputerName <Device fqdn>
```

Neustart des Systems
  
```
invoke-command { Shutdown /r /t 0 } -ComputerName <Device fqdn>
```

Abrufen von Protokollen
  
```
$targetDevice = "<Device fqdn> "
$logFile = invoke-command {$output = Powershell.exe -ExecutionPolicy Bypass -File C:\Rigel\x64\Scripts\Provisioning\ScriptLaunch.ps1 CollectSrsV2Logs.ps1
Get-ChildItem -Path C:\Rigel\*.zip | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1} -ComputerName $targetDevice
$session = new-pssession -ComputerName $targetDevice
Copy-Item -Path $logFile.FullName -Destination .\ -FromSession $session; invoke-command {remove-item -force C:\Rigel\*.zip} -ComputerName $targetDevice
```

Drücken Sie eine XML-Konfigurationsdatei (oder Grafik Design)
  
```
$movefile = "<path>";
$targetDevice = "\\<Device fqdn> \Users\Skype\AppData\Local\Packages\Microsoft.SkypeRoomSystem_8wekyb3d8bbwe\LocalState\SkypeSettings.xml"; 
Copy-Item $movefile $targetDevice 
```

## <a name="software-updates"></a>Softwareupdates
<a name="SWupdate"> </a>

Standardmäßig versucht Microsoft Teams Räume zum Verbinden mit den Windows Store zum Abrufen der neuesten Version von Microsoft-Teams Chatrooms Software, damit das Gerät regulären Internetzugriff erforderlich ist. Kontaktaufnahme mit Microsoft Support-Probleme, werden Sie sicher, dass das Gerät Microsoft Teams Chatrooms mit der neuesten Version der app geladen wird.
  
Standardmäßig Microsoft Teams Chatrooms stellt eine Verbindung mit Windows Update Betriebssystem abgerufen und USB-Peripheriegeräte Firmwareupdates und installiert diese außerhalb der Geschäftszeiten konfiguriert. Sie können Geschäftszeiten konfigurieren, indem Sie sich beim Administratorkonto anmelden und die Einstellungen-App ausführen.
  
Wenn Sie Updates manuell verwalten möchten, und nicht im normale Verfahren für eine [Microsoft Store for Business](https://businessstore.microsoft.com/store) zu [verteilen offline-apps](https://docs.microsoft.com/microsoft-store/distribute-offline-apps)haben, können Sie die entsprechende APPX Datei und Abhängigkeiten in [Deployment Kit](https://go.microsoft.com/fwlink/?linkid=851168) (aus abrufen. die Anweisungen zum [Konfigurieren einer Microsoft-Teams Chatrooms Konsole](console.md)) mit SCCM verwendet werden kann. Die Deployment Kit-Version Positionen davor befindet hinter der Store-Version, damit es immer den neuesten Build möglicherweise nicht übereinstimmt.
  
### <a name="to-update-using-powershell"></a>Aktualisieren von Powershell

1. Extrahieren Sie das Paket aus der Installation die [MSI-Datei](https://go.microsoft.com/fwlink/?linkid=851168) zu einer Freigabe das Gerät, die zugreifen kann.
    
2. Führen Sie das folgende Skript für die Microsoft-Teams Chatrooms Geräte, ändern \<freigeben\> freigeben als Antwort auf das Gerät:
    
```
Add-AppxPackage -Update -ForceApplicationShutdown -Path '\\<share>\$oem$\$1\Rigel\x64\Ship\AppPackages\*\*.appx' -DependencyPath (Get-ChildItem '\\<share>\$oem$\$1\Rigel\x64\Ship\AppPackages\*\Dependencies\x64\*.appx' | Foreach-Object {$_.FullName})
```

## <a name="admin-mode-and-device-management"></a>Administratormodus und Geräteverwaltung
<a name="AdminMode"> </a>

Einige Managementfunktionen, wie die manuelle Installation eines privaten Zertifizierungsstellenzertifikats erfordern das Vorhandensein des Surface Pro Geräts im Admin-Modus. 
  
### <a name="switching-to-admin-mode-and-back-when-the-microsoft-teams-rooms-app-is-running"></a>Wechsel in Administratormodus und zurück, wenn die Microsoft-Teams Chatrooms app ausgeführt wird

1. Alle laufenden Anrufe Auflegen, und klicken Sie auf der Startseite zurück.
    
2. Wählen Sie das Zahnradsymbol und rufen Sie das Menü (Optionen sind **Einstellungen**, **Eingabehilfen**und **Gerät neu starten** ).
    
3. Wählen Sie **Einstellungen** aus.
    
4. Geben Sie das Administratorkennwort ein. Der Setupbildschirm wird angezeigt.
    
    > [!NOTE]
    > Wenn das Gerät in die Domäne eingebundener nicht ist, wird das lokale Administratorkonto (Benutzername "Admin") in der Standardeinstellung verwendet werden. Das Standard-Kennwort für dieses Konto ist 'Sfb', aber es wird empfohlen, dass Ihre Organisation dies für aus Sicherheitsgründen so bald wie möglich zu ändern. Wenn der Computer Mitglied einer Domäne ist, können Sie sich mit einem Domänenkonto entsprechend berechtigten anmelden. 
  
5. Wählen Sie **Windows-Einstellungen** in der linken Spalte aus.
    
6. Wählen Sie **Zu Administratoranmeldung wechseln** aus.
    
7. Geben Sie das Administratorkennwort ein. Daraufhin wird die App ordnungsgemäß abgemeldet, und Sie gelangen zum Windows-Anmeldebildschirm. 
    
8. Melden Sie sich mit Ihren Administratoranmeldeinformationen beim Desktop an. Sie müssen die erforderlichen Berechtigungen zum Verwalten des Geräts.
    
9. Führen Sie die notwendigen Administratoraufgaben aus.
    
10. Melden Sie sich bei Ihrem Administratorkonto ab.
    
11. Zurück zu Microsoft-Teams Räumen durch Auswählen des Benutzer Konto-Symbols auf der linken Seite des Bildschirms und anschließend **Skype**.
    
    Wenn der Benutzer **Skype** nicht aufgeführt ist, möglicherweise müssen Sie wählen Sie **Benutzer** aus, und geben **. \skype** als den Benutzernamen und das anmelden.
    
Die Konsole ist nun wieder in den normalen Betrieb-Modus. Das folgende Verfahren benötigen Sie eine Tastatur auf das Gerät anfügen, falls noch nicht angefügt wurde. 
  
### <a name="switching-to-admin-mode-and-back-when-the-microsoft-teams-rooms-app-crashes"></a>Wechsel in Administratormodus und zurück, wenn die Anwendung Microsoft-Teams Räume zum Absturz

1. Drücken Sie fünf Mal schnell hintereinander die WINDOWS-TASTE. Daraufhin gelangen Sie zum Windows-Anmeldebildschirm. 
    
2. Melden Sie sich mit Ihren Administratoranmeldeinformationen beim Desktop an.
    
    > [!NOTE]
    > Diese Methode nicht melden Sie sich den Skype-Benutzer oder die app ordnungsgemäß beendet, aber verwenden Sie es, wenn die app wurde nicht mehr reagiert und die andere Methode war nicht verfügbar. 
  
3. Führen Sie die notwendigen Administratoraufgaben aus.
    
4. Starten Sie den Computer, wenn Sie fertig sind.
    
   Die Konsole wird neu gestartet, in den normalen Betrieb-Modus, die Microsoft-Teams Chatrooms app ausgeführt. Sie können die Tastatur entfernen, wenn es angefügt wurde, damit Sie dieses Verfahren ausführen können.
   ## <a name="troubleshooting-tips"></a>Tipps zur Problembehandlung
   <a name="TS"> </a>

- Besprechungsanfragen möglicherweise nicht angezeigt, wenn über Domänengrenzen hinweg (beispielsweise zwischen zwei Unternehmen) gesendet. In solchen Fällen sollten die IT-Administratoren, ob externe Benutzer zum Planen einer Besprechung zugelassen entscheiden.
    
- Microsoft-Teams Chatrooms unterstützt keine Exchange AutoDiscover leitet über Exchange 2010.
    
- Im Allgemeinen ist es ratsam für IT-Administratoren, die alle audioendpunkte deaktivieren, die er nicht verwenden möchten.
    
- Falls ein Spiegelbild in der Raumvorschau angezeigt wird, kann der IT-Administrator dies korrigieren, indem die Stromversorgung der Kamera angestellt wird oder die Bildausrichtung mit der Fernsteuerung der Kamera gekippt wird.
    
- Es ist bekannt, dass der Zugang zum Konsolentouchscreen verloren gehen kann. In solchen Fällen wird durch einen Neustart des Systems Microsoft Teams Chatrooms manchmal das Problem behoben.
    
- Beim Verbinden eines PCs mit der Konsole über verkabelte Erfassung kann ein Verlust der lokalen Audiodaten auftreten. Das Problem mit der Wiedergabe der lokalen Audiodaten kann in diesem Fall durch einen Neustart des PCs gelöst werden.
    