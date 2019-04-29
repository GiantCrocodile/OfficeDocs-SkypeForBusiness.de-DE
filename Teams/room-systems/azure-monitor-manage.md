---
title: Verwalten von Microsoft-Teams Chatrooms Geräte mit Azure Monitor
ms.author: jambirk
author: jambirk
ms.reviewer: davgroom
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: f8109905-3279-475f-a64b-31d37af48bfe
ms.collection: M365-voice
description: In diesem Artikel wird erläutert, wie Microsoft Teams Chatrooms Geräte in Azure Monitor mit integrierten, End-to-End-Weise verwalten.
ms.openlocfilehash: 4606bdde4e47eb2662e73434d1026d47093fb1e1
ms.sourcegitcommit: 79ec789a22acf1686c33a5cc8ba3bd50049f94b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2019
ms.locfileid: "33362807"
---
# <a name="manage-microsoft-teams-rooms-devices-with-azure-monitor"></a>Verwalten von Microsoft-Teams Chatrooms Geräte mit Azure Monitor

In diesem Artikel wird erläutert, wie Microsoft Teams Chatrooms Geräte in Azure Monitor mit integrierten, End-to-End-Weise verwalten.

Sie können konfigurieren, Azure überwachen, um grundlegende Telemetrie bereitzustellen, mit deren Hilfe Sie bei der Verwaltung von Skype meeting Room-Geräte (finden Sie unter [Planen von Microsoft Teams Chatrooms Verwaltung mit Azure Monitor](azure-monitor-plan.md) und [Bereitstellen von Microsoft Teams Chatrooms mit Azure Monitor]((azure-monitor-deploy.md) for details). Der Management-Lösung Laufe der Zeit zusätzliche Daten und Management-Funktionen können Sie um eine ausführlichere Ansicht der Leistung des Geräts zu erstellen.

## <a name="understand-the-log-entries"></a>Verstehen der Protokolleinträge

Die folgenden Sicherheitsereignisse werden alle fünf Minuten, wenn die Microsoft-Teams Raum app die entsprechende Informationen in der Windows-Ereignisprotokoll aufgezeichnet, in das Ereignisprotokoll Beschreibungsfeld eingefügt. Microsoft Agent Monitoring übergibt diese Einträge an Protokoll Analytics in Azure Monitor, wodurch sie in das Dashboard analysiert, die Sie bei der [Verwaltung von Microsoft-Teams-Chatrooms Bereitstellen mit Azure Monitor](azure-monitor-deploy.md)erstellt haben. Mit dem Dashboard können Sie nach einzelnen Protokolleinträgen suchen, um die Ausführung von Aktionen festzulegen (falls erforderlich). 

Die Ereignis-IDs 2000 und 3000 geben an, dass das fragliche Gerät nicht wie erwartet funktioniert. Ereignis-IDs 2001 und 3001 geben an, dass ein Problem gefunden wurde. Für Ereignis-ID 4000 ist möglicherweise eine Aktion erforderlich, wenn diese im Vergleich zu einem von Ihnen festgelegten Punkt oder anderen in Ihrer Organisation bereitgestellten Geräte häufiger angezeigt werden.

Wenn Sie diese Ereignisbeschreibungen verstehen, werden Sie schnell über Probleme informiert und wissen, wo Ihr Ansatz für die weitere Problembehebung sein kann.

| Ereignis&nbsp;ID&nbsp;Ebene|Ereignis&nbsp;Verhalten&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Ereignis&nbsp;Beschreibung&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|:---    |:---   |:---  |
| 2000  <br> Informationen | Dies ist ein Ereignis über einen fehlerfreien Takt. Alle 5 Minuten, Microsoft Teams Chatrooms überprüft, ob es Microsoft-Teams oder Skype für Unternehmen angemeldet ist und Netzwerk- und Verbindungsproblemen Exchange hat. <br> Wenn alle 3 Bedingungen erfüllt werden, wird alle 5 Minuten Ereignis-ID 2000 in das Ereignisprotokoll geschrieben, bis das Gerät offline ist oder mindestens eine der Bedingungen nicht mehr erfüllt wird. | {"Beschreibung": "Heartbeat ist fehlerfrei.", "ResourceState": "Fehlerfrei", "-Operation": "Heartbeat", "OperationResult": "Übergeben", "OS": "Windows 10", "OSVersion": "10.0.14393.693", "Alias": "Alias<span></span>@contoso.com", "DisplayName": "Anzeigename ","AppVersion":"1.0.38.0","IPv4Address":"10.10.10.10","IPv6Address":"IP-Adresse v6"} <br><br> In diesem Beispiel alle Heartbeat-Bedingung erfüllt wurden, und das Gerät Microsoft Teams Chatrooms als fehlerfrei gekennzeichnet wurde. Bei dem Auftreten von Fehlern hätte die App stattdessen Ereignis-ID 2001 aufgezeichnet. |
| 2001  <br> Fehler | Dies ist eine app Error-Ereignis. Alle 5 Minuten, überprüft Microsoft Teams Chatrooms, dass es bei Microsoft-Teams oder Skype für Unternehmen mit Netzwerk- und Verbindungsproblemen Exchange angemeldet ist. Wenn eine oder mehrere Faktoren nicht zutreffen, wird sie schreiben EventID 2001 in das Ereignisprotokoll alle 5 Minuten, bis das Gerät ist offline oder alle Aktionen erneut erfüllt werden können.  | {"Description":"Network status : Healthy. Exchange status : Connected. **Signin status: Unhealthy.** ","ResourceState":"Fehlerhaft","-Operation":"Heartbeat","OperationResult":"Fehler","OS":" Windows 10","OSVersion":"10.0.14393.693","Alias":" ","DisplayName":"Anzeigename","AppVersion":"1.0.38.0","IPv4Address":"10.10.10.10"," IPv6Address":"Ip-Adresse v6"} <br><br>  In diesem Beispiel ermittelt Microsoft Teams Chatrooms, dass die Netzwerkverbindung fehlerfrei und die app wurde mit Exchange verbunden, aber der fett formatierten Teil gibt an, dass die app nicht mit Skype für Unternehmen verbunden ist. Dies könnte ein Problem mit der Serverkonfiguration auf dem Gerät oder Host sein.  <br> <br> Der Netzwerkstatus zeigt entweder „Healthy“ (Fehlerfrei) oder „Unhealthy“ (Fehlerhaft) an. Wenn der Status fehlerhaft ist, Sie müssen möglicherweise ein Problem mit der oder das Gerät entfernt wurde (aber dann würden Sie wahrscheinlich auch Exchange und Microsoft-Teams oder Skype Business Fehler haben).  <br><br> Der Exchange-Status wird als verbunden oder eine der folgenden angezeigt: nicht verbundene, verbinden, AutodiscoveryError (die am häufigsten Fehler), GeneralError oder ServerVersionNotSupported. Wenn der Status verbinden, warten Sie ist, bis die nächste Health-Nachricht gesendet wird, anderen Fehlern finden Sie das Problem in ein Administrator mit Erfahrung in der Exchange-Probleme beheben.  <br><br>  Der Anmeldestatus (zeigt an, dass die App bei Skype for Business angemeldet ist) wird als „Healthy“ bzw. „Unhealthy“ angezeigt. Wenn der Status „Unhealthy“ ist, bemühen Sie einen Techniker, um das Problem zu weiter zu untersuchen. |
| 3000  <br> Informationen | Dieses Ereignis wird überprüft, dass eine Überprüfung der Hardware ausgeführt und fehlerfrei gefunden wurde. Alle 5 Minuten Microsoft Teams Chatrooms Prüfungen, die den Hardwarekomponenten wie am Anfang Raum anzeigen, Mikrofon, Lautsprecher und Kamera konfiguriert sind komplett vernetztes und funktionsfähig. Wenn alle Komponenten fehlerfrei sind, wird Ereignis-ID 3000 in das Ereignisprotokoll geschrieben. Dieses Ereignis wird so lange alle 5 Minuten in das Protokoll geschrieben, bis ein Fehler mit dem verbundenen Gerät auftritt.  <br> | {"Beschreibung": "HardwareCheckEngine ist fehlerfrei.", "ResourceState": "Fehlerfrei", "-Operation": "HardwareCheckEngine", "OperationResult": "Übergeben", "OS": "Windows 10", "OSVersion": "10.0.14393.693", "Alias": "Alias<span></span>@contoso.com", " DisplayName":"Anzeigename","AppVersion":"1.0.38.0","IPv4Address":"10.10.10.10","IPv6Address":"Ip-Adresse v6"}  <br><br> In diesem Beispiel sind bei keiner Hardwareüberprüfung Fehler aufgetreten. Wenn Fehler aufgetreten sind, würde die app-Ereignis-ID 3001 stattdessen aufzeichnen. |
| 3001  <br> Error-Ereignis  | Dies ist eine Hardware Error-Ereignis. Die Microsoft-Teams Chatrooms app verfügt über ein Prozess, der die Integrität der verbundenen Hardwarekomponenten (Vordergrund Raum, Mikrofon, Lautsprecher und Kamera) alle 5 Minuten überprüft. Wenn eine oder mehrere Komponenten fehlerhaft sind, wird es EventID 3001 in das Ereignisprotokoll geschrieben. Dieses Ereignis wird weiterhin geschrieben werden alle 5 Minuten, bis das Problem mit dem Gerät behoben wurde.   | {"Beschreibung": " **Status Front des Raums anzeigen: instabil.** Configured display count is 2. Real display count is 0. **Conference Microphone status : Unhealthy.** Conference Speaker status : Healthy. Default Speaker status : Healthy. Kamera-Status: fehlerfrei. ","ResourceState":"Fehlerhaft","-Operation":"HardwareCheckEngine","OperationResult":"Fehler","OS":"Windows 10","OSVersion":"10.0.14393.1198","Alias":" Alias<span></span>@contoso.com ","DisplayName":"Yosemite Konferenzraum","AppVersion":"2.0.58.0","IPv4Address":"10.10.10.10","IPv6Address":"IPv6Address","IPv4Address2":"10.10.10.10"} <br><br>  Die Hardware-Peripheriegeräte werden entweder als „Healthy“ (Fehlerfrei) oder „Unhealthy“ (Fehlerhaft) angezeigt. <br> In diesem Beispiel werden zwei Vorderseite Raum zeigt konfiguriert, und derzeit keine davon steht. Der Konferenz Mikrofon Status ist fehlerhaft, die möglicherweise einer Reihe von möglichen Ursachen. Da mindestens eine Ressource die Überprüfung nicht bestanden haben, wird die ResourceState als fehlerhaft aufgelistet. Senden Sie einen Techniker weiter untersuchen. |
| 4000  <br> Informationen  <br> | Dies ist ein App-Neustartereignis. Immer, wenn die App neu gestartet wird, wird dieses Ereignis im Windows-Fehlerprotokoll protokolliert.  <br> | {"Beschreibung": "App neu gestartet wird.", "ResourceState": "Fehlerfrei", "-Operation": "Neu starten", "OperationResult": "Übergeben", "OS": "Windows 10", "OSVersion": "10.0.14393.693", "Alias": "Alias<span></span>@domain.com", "DisplayName": "Anzeigename", " AppVersion":"1.0.38.0","IPv4Address":"10.10.10.10","IPv6Address":"Ip-Adresse v6"} <br><br> Die app kann aus verschiedenen Gründen neu starten. Vergleichen Sie die Neustartfrequenz der Geräte im selben Gebäude und in anderen Gebäuden und berücksichtigen Sie dabei Probleme wie Stromzufuhrschwankungen und Stromausfälle, da diese Hinweise auf mögliche Infrastrukturprobleme geben können.|

## <a name="see-also"></a>Siehe auch
 

[Planen der Verwaltung von Microsoft-Teams Chatrooms mit Azure Monitor](azure-monitor-plan.md)

[Bereitstellen von Microsoft-Teams Chatrooms Management mit Azure Monitor](azure-monitor-deploy.md)