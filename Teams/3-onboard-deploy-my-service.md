---
title: Bereitstellen von Microsoft-Teams, Cloud VoIP-Dienst
author: rmw2890
ms.author: MyAdvisor
manager: lehewe
ms.date: 03/13/2018
ms.topic: article
ms.service: msteams
ms.reviewer: rowille
description: Laden Sie die Website-Aktivierung Playbook zur Planung der Einführung Teams und beschleunigen und zur Optimierung Benutzerakzeptanz, Wahrnehmung der Qualität und Kundenzufriedenheit.
MS.collection: Strat_MT_TeamsAdmin
appliesto:
- Microsoft Teams
ms.openlocfilehash: 3ddccd9c52e25ae9d0069119641aa7e8a8077d56
ms.sourcegitcommit: b985035b91ebd7ceff8d50e9e0fa9aa6ff971f3a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2018
---
# <a name="deploy-my-service"></a>Stellen Sie meine Dienst

## <a name="site-enablement-playbook-for-microsoft-teams-voice-workloads"></a>Website-Aktivierung (Playbook) für Microsoft-Teams, VoIP-Arbeitslasten

Verwenden Sie diese Playbook mit deren Hilfe Ihre Organisation erfolgreich planen und Ausführen von der Einführung von Microsoft-Teams, VoIP-Funktionen für einzelne Website-Website.

Einschließlich aller erforderlichen Aktivitäten, empfohlen Zeitachsen und Links zu entsprechenden Anweisungen für jede Aktivität behandelt dieses Playbook End-to-End-Anleitungen zum Sicherstellen einer erfolgreichen Teams VoIP-bereitstellungs für eine bestimmte Website, Konzentration auf Faktoren, die eine wichtige Rolle spielen für den Benutzer.

Anhand der Aktivitäten in dieser Playbook kann Ihre Organisation:

-   Effektiv planen und nahezubringen Teams planen.

-   Beschleunigen Sie und Optimieren Sie der Benutzerakzeptanz.

-   Reduzieren von Support-Anforderungen und steigern Benutzerzufriedenheit.

> [!NOTE]
> In diesem Artikel und die zugehörigen Playbook werden nicht für die direkte Verwendung beschreiben alle technischen Konfigurationsschritte erforderlich für die Aktivierung von Diensten oder an einen bestimmten Standort Wählton bereitstellen. Stattdessen Schwerpunktthemen Aktivitäten und Aufgaben auf einfache Weise integrierte Benutzern empfohlen und lassen, beginnt, Teams VoIP Arbeitslasten über einen schnellen und reibungslosen Übergang mit einer hohen Akzeptanz Support-Anforderungen zu minimieren. Technische Anleitungen für Teams VoIP Ihrer Umgebung am besten konfigurieren finden Sie unter Onboarding Prüflisten für [Teams VoIP Arbeitslasten konfigurieren](https://docs.microsoft.com/MicrosoftTeams/onboarding-checklist-configure-cloud-voice-workloads-in-Microsoft-Teams), [Teams Kernfunktionen](https://docs.microsoft.com/MicrosoftTeams/onboarding-checklist-configure-microsoft-teams-core-capabilities), [Netzwerke für Teams](https://docs.microsoft.com/MicrosoftTeams/onboarding-checklist-configure-networking)und [Aktivieren von Office 365 ](https://docs.microsoft.com/MicrosoftTeams/onboarding-checklist-enable-office-365).

<!--ENDOFSECTION-->

## <a name="playbook-focus-areas"></a>Schwerpunkte (Playbook)

Der Schwerpunkt der Playbook ist die Faktoren behandeln, die beeinflussen des Benutzers Wahrnehmung der einer Teams VoIP-Bereitstellung. Aktivitäten und Aufgaben sind in die folgenden Fokus Bereiche unterteilt:

-   Überprüfung der Service-Bereitschaft

-   Benutzer-Aktivierung

-   Endpunkte

-   Verwendung und Qualität

-   Übernahme

Die [Website Aktivierung Playbook für VoIP (Playbook)](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/blob/live/Teams/downloads/site-enablement-playbook-for-voice-(playbook).xlsx?raw=true) ist eine Microsoft Excel-Arbeitsmappe. Jeden dieser Bereiche fünf Fokus ist ein separates Blatt in der Arbeitsmappe, und jeder Bereitstellungsaufgabe und die Aktivitäten auf eine der folgenden Arbeitsblätter gruppiert wird.

![Screenshot des der (Playbook)] (media/deploy-my-service-image1.png "Screenshot des der (Playbook)")

> [!NOTE]
> Sie erstellen eine separate Instanz von der Playbook für jeden Standort für nahezubringen Teams im Bereich.

<!--ENDOFSECTION-->

## <a name="how-to-use-the-playbook"></a>So verwenden Sie die (Playbook)

Unabhängig von der Größe und Komplexität des Speicherorts, jede Website aktivieren,, Ihre Aufgaben und Aktivitäten planen erfordert früh genug – sowie deren Ausführung in optimaler Reihenfolge – vor, während und nach der Einführung der tatsächlichen Service. Es wird empfohlen, dass Sie beim Planen und Ausführen Ihrer eigenen Weg zu Microsoft-Teams, VoIP diese Schritte ausführen.

1.  Laden Sie die [Website-Aktivierung Playbook für VoIP (Playbook)](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/blob/live/Teams/downloads/site-enablement-playbook-for-voice-(playbook).xlsx?raw=true) für Microsoft-Teams, VoIP.

2.  Erstellen Sie eine separate Kopie der Playbook für jeden Standort.

3.  Ersetzen Sie auf der Registerkarte für das Blatt mit dem Namen **Playbook für {SiteName-Code}** **{SiteName-Code}** mit der relevante Websitename und/oder Vorwahl.

4.  Geben Sie die **Websitename, Vorwahl**und **Starttermin geplant**, wie im folgenden beschrieben. Dies ist ein wichtiger Schritt, da die empfohlenen Stichtagen für jede Aktivität in der Playbook angepasst.

    ![Beispiel mit Namen von New York-Vorwahl NY01, und geplanten Startdatum für 20-Mrz-18 des Standorts] (media/deploy-my-service-image2.png "Beispiel mit Namen von New York-Vorwahl NY01, und geplanten Startdatum für 20-Mrz-18 des Standorts")

5.  Überprüfen Sie jede Aktivität, Aktionen Sie erforderlich, und aktualisieren Sie den Status aus, wie Sie die Zeitachse durchlaufen. Status wird wie unten beschrieben grafisch dargestellt:
    <ul>
    <li>![Grünes Häkchen](media/deploy-my-service-image3.png) **Ja oder nicht zutreffend (Grün):** die Aktivität abgeschlossen wurde, oder es gilt nicht für diese Website und keine weitere Aktion erforderlich ist.</li>
    <li>![Gelbes Ausrufezeichen](media/deploy-my-service-image4.png) **die Aktivität nicht vollständig ausgeführt noch (gelb):** die Aktivität noch nicht noch abgeschlossen und müssen auf Ja oder Nein aus, dessen Zeitplan aktualisiert werden.</li>
    <li>![Rote X](media/deploy-my-service-image5.png) **keine (Rot):** die Aktivität kann aufgrund eines Problems nicht abgeschlossen werden und muss für die Project Status Besprechung durchgeführt werden.</li></ul>

6.  Der Status wird in jedem Abschnitt zusammengefasst und die Abschnittsüberschrift mit einem der folgenden Statusindikatoren formatiert ist. **Wöchentliche Status** wird auch automatisch aktualisiert.

![Screenshot des weekly Status - Rollups in die (Playbook)] (media/deploy-my-service-image6.png "Screenshot des weekly Status - Rollups in die (Playbook)")

> [!TIP]
> Wiederholen Sie die obigen Schritte für alle Speicherorte, die Ihnen.


> [!IMPORTANT]
> Einige Schritte möglicherweise nicht für alle Standorte und Websites gelten. Wenn eine bestimmte Aktivität nicht für eine Website relevant ist, müssen Sie für diese Aktivität **nicht zutreffend** auswählen. Alle Zeilen in der Playbook **nicht löschen** . In diesem Fall die Status-Rollup-Formeln, funktionieren nicht.<br/><br/>
Achten Sie auf, die die voraussichtliche mehr Zeit als Sie, wie etwa Zahl Portieren geplant und Beschaffungsaktivitäten. Diese Aktivitäten können sich negativ auf die Website Bereitstellung Zeitachse auswirken. Müssen Sie überprüfen und aktualisieren die Liste der Aktivitäten und der zugehörige Zeitplan wöchentlich, und präsentieren sie bei [Lenkungsausschuss Besprechungen](https://docs.microsoft.com/MicrosoftTeams/envision-steering-committee-complete-guide) , um sicherzustellen, dass die Beteiligten den Status von jedem Standort und alle möglichen Abweichung aus der Planung der Bereitstellung kennen.


<table>
<tr><td>![](media/audio_conferencing_image7.png) <br/>Entscheidungspunkte</td><td><ul><li>Entscheiden Sie, ob die Website-Aktivierung (Playbook) für Ihre Bereitstellung erforderlich ist.</li><li>Legen Sie fest, wer ist verantwortlich für das Anpassen von Website-Aktivierung (Playbook) für Microsoft-Teams für jeden Standort, den Sie bereitstellen müssen.</li></ul></td></tr>
<tr><td>![](media/audio_conferencing_image9.png)<br/>Nächste Schritte</td><td><ul><li>Laden Sie die Website-Aktivierung (Playbook).</li><li>Passen Sie die Website-Aktivierung Playbook für die erste Website.</li><li>Wiederholen Sie nach Bedarf für weitere Standorte.</li></ul></td></tr>
</table>

<!--ENDOFSECTION-->