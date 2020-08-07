---
title: Grenzwerte und Spezifikationen für Microsoft Teams
author: SerdarSoysal
ms.author: serdars
manager: serdars
ms.topic: reference
ms.service: msteams
audience: admin
ms.reviewer: ''
description: In diesem Artikel werden die Grenzwerte, Spezifikationen und anderen Anforderungen für Microsoft Teams beschrieben.
localization_priority: Priority
f1.keywords:
- NOCSH
ms.collection:
- M365-collaboration
- SPO_Content
search.appverid: MET150
appliesto:
- Microsoft Teams
ms.custom: seo-marvel-apr2020
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 236b11242c4f7f609fb5eab0bd772884f9452336
ms.sourcegitcommit: 43d66693f6f08d4dcade0095bf613240031fec56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "46583654"
---
# <a name="limits-and-specifications-for-microsoft-teams"></a>Grenzwerte und Spezifikationen für Microsoft Teams

In diesem Artikel werden einige der Grenzwerte, Spezifikationen und anderen Anforderungen für Teams beschrieben.

## <a name="teams-and-channels"></a>Teams und Kanäle

|Feature    | Obergrenze |
|-----------|---------------|
|Anzahl der Teams, die ein Benutzer erstellen kann | Grenzwert von 250 Objekten&sup1;         |
|Anzahl von Teams, in denen ein Benutzer Mitglied sein kann|1.000|
|Anzahl der Mitglieder in einem Team | 10.000       |
|Anzahl von Besitzern pro Team | 100   |
|Anzahl organisationsweiter Teams, die in einem Mandanten zulässig sind | 5     |
|Anzahl der Mitglieder in einem [organisationsweiten Team](create-an-org-wide-team.md) | 5.000       |
|Anzahl der Teams, die ein globaler Administrator erstellen kann        |  500.000   |
|Anzahl von Teams, die eine Microsoft 365- oder Office 365-Organisation haben kann    | 500.000&sup2;     |
|Anzahl der Kanäle pro Team    | 200 (einschließlich gelöschter Kanäle)&sup3;         |
|Anzahl der privaten Kanäle pro Team    |30|
|Anzahl der Mitglieder in einem privaten Kanal    |250|
|Größe eines Beitrags in einer Kanalunterhaltung | Ca. 28 KB pro Beitrag<sup>4</sup> |

<sup>1</sup> Jedes Verzeichnisobjekt in Azure Active Directory zählt. Globale Administratoren und Apps, die Microsoft Graph mit [Anwendungsberechtigungen](https://docs.microsoft.com/graph/permissions-reference) aufrufen, sind von diesem Grenzwert ausgeschlossen.

<sup>2</sup> Diese Beschränkung umfasst archivierte Teams.

<sup>3</sup> Gelöschte Kanäle können innerhalb von 30 Tagen wiederhergestellt werden. Während dieser 30 Tage wird ein gelöschter Kanal weiterhin in das 200-Kanallimit pro Team eingerechnet. Nach 30 Tagen wird ein gelöschter Kanal und dessen Inhalte endgültig gelöscht, und der Kanal wird nicht mehr in das 200-Kanallimit pro Team eingerechnet.

<sup>4</sup> 28 KB ist ein ungefährer Grenzwert, da er die Nachricht selbst (Text, Bildlinks usw.), @Erwähnungen, die Anzahl der Connectors und Reaktionen umfasst.

## <a name="messaging"></a>Messaging

### <a name="chat"></a>Chat

Benutzer, die an Gesprächen teilnehmen, die Teil der Chat-Liste in Microsoft Teams sind, müssen ein Exchange Online-Postfach (cloudbasiert) für einen Administrator haben, um Unterhaltungen im Chat zu durchsuchen. Der Grund hierfür ist, dass Unterhaltungen, die Teil der Chat-Liste sind, in den cloudbasierten Postfächern der Chat-Teilnehmer gespeichert werden. Wenn ein Chat-Teilnehmer nicht über ein Exchange Online-Postfach verfügt, kann der Administrator Chat-Unterhaltungen nicht durchsuchen oder sperren. Beispielsweise können in einer Exchange-Hybridbereitstellung Benutzer mit lokalen Postfächern an Unterhaltungen teilnehmen, die Teil der Chat-Liste in Microsoft Teams sind. Der Inhalt dieser Unterhaltungen ist in diesem Fall jedoch nicht durchsuchbar und kann nicht gesperrt werden, da die Benutzer keine cloudbasierten Postfächer haben. (Weitere Informationen finden Sie unter [Interaktion von Exchange und Microsoft Teams](exchange-teams-interact.md).)

Der Microsoft Teams-Chat funktioniert in einem Microsoft Exchange-Backend, sodass Grenzwerte für das Exchange-Messaging auf die Chat-Funktion in Microsoft Teams angewendet werden.

|Feature  | Obergrenze  |
|---------|---------|
|Anzahl der Personen in einem privaten Chat<sup>1</sup>  | 250<br><br>**Hinweis:** Für Teams for Government (GCC, GCC High, DoD) ist der Grenzwert immer noch 100. Wir werden diesen Artikel aktualisieren, sobald die Cloud-Grenze der Behörden von 100 auf 250 erhöht wird.    |
|Anzahl von Personen in einem Video- oder Audioanruf aus dem Chat | 20 |
|Anzahl der Dateianlagen <sup>2</sup>  |10     |
|Größe des Chats | Ca. 28 KB pro Beitrag<sup>3</sup> |

<sup>1</sup> Wenn mehr als 20 Personen an einem Chat teilnehmen, werden die folgenden Chat-Funktionen deaktiviert: automatische Outlook-Antworten und Teams-Statusmeldungen; Eingabeindikator; Video- und Telefonanrufe; Freigabe; Lesebestätigungen. Die Schaltfläche „Übermittlungsoptionen festlegen“ (!) wird ebenfalls entfernt, wenn private Gruppenchats mehr als 20 Mitglieder umfassen.

<sup>2</sup> Falls die Anzahl der Anlagen dieses Limit überschreitet, wird eine Fehlermeldung angezeigt.

<sup>3</sup> 28 KB ist ein ungefährer Grenzwert, da er die Nachricht selbst (Text, Bildlinks usw.), @Erwähnungen und Reaktionen umfasst.

### <a name="emailing-a-channel"></a>Senden von E-Mails an einen Kanal

 Wenn Benutzer eine E-Mail an einen Kanal in Microsoft Teams senden möchten, verwenden sie dazu die E-Mail-Adresse des Kanals. Wenn eine E-Mail Teil eines Kanals ist, kann jeder darauf antworten, um eine Unterhaltung zu beginnen. Hier einige geltende Grenzwerte zum Senden von E-Mails an einen Kanal:

|Funktion  | Obergrenze  |
|---------|---------|
|Nachrichtengröße<sup>1<sup> | 24 KB |
|Anzahl der Dateianlagen <sup>2</sup>  |20     |
|Größe der einzelnen Dateianlagen | Kleiner als 10 MB |
|Anzahl von Inlinebildern<sup>2</sup> |50   |

<sup>1</sup> Wenn die Nachricht dieses Limit überschreitet, wird eine Vorschaunachricht generiert und der Benutzer wird aufgefordert, die Original-E-Mail über den bereitgestellten Link herunterzuladen und anzusehen.

<sup>2</sup> Falls die Anzahl der Anlagen oder Bilder dieses Limit überschreitet, wird eine Fehlermeldung angezeigt.

Weitere Informationen finden Sie unter [Exchange Online-Begrenzungen](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits).

> [!NOTE]
> Die Beschränkungen für Nachrichtengröße, Dateianlagen und Inline-Bilder sind für alle Microsoft 365- und Office 365-Lizenzen identisch.

## <a name="channel-names"></a>Kanalnamen

Kanalnamen dürfen keine der folgenden Zeichen oder Worte enthalten.

|||
|---------|---------|
|Zeichen     | ~ # % & * { } + / \ : < > ? &#124; ' " , .        |
|Zeichen in diesen Bereichen:    | 0 bis 1F<br>80 bis 9F        |
|Words     | Formulare, CON, CONIN$, CONOUT$, PRN, AUX, NUL, COM1 to COM9, LPT1 to LPT9, desktop.ini,  &#95;vti&#95;|

Kanalnamen dürfen auch nicht mit einem Unterstrich (_) oder Punkt (.) beginnen oder mit einem Punkt (.) enden.

## <a name="meetings-and-calls"></a>Besprechungen und Anrufe

|Feature     | Obergrenze |
|------------|---------------|
|Anzahl von Personen in einer Besprechung (können chatten und sich einwählen)  |300. Bei **„Nur anzeigen“** können bis zu 20.000 Teilnehmer an einer Besprechung teilnehmen, bei der der Organisator über eine Lizenz für die Advanced Communications-Add-on-SKU verfügt.<sup>1</sup> [!INCLUDE [template](includes/preview-feature.md)] <br><br>**Hinweis:** In Teams for Government (GCC, GCC High, DoD) ist der Grenzwert immer noch 250. Wir aktualisieren diesen Artikel, sobald die Cloud-Grenze für Behörden von 250 auf 300 erhöht wird und Besprechungs-Überlauf unterstützt.   |
|Anzahl von Personen in einer Besprechung (können chatten und sich einwählen)  | 300 |
|Anzahl von Personen in einem Video- oder Audioanruf aus dem Chat | 20 |
|Maximale Größe von PowerPoint-Dateien | 2GB|
|Teams hält [Besprechungsaufzeichnungen](cloud-recording.md), die nicht in Microsoft Stream hochgeladen werden, verfügbar für den lokalen Download | 20 Tage |

<sup>1</sup> „Nur anzeigen“ ist standardmäßig aktiviert. Sie können mithilfe von PowerShell den Besprechungs-Überlauf deaktivieren. 
```powershell
Set-CsTeamsMeetingPolicy -Identity Global -StreamingAttendeeMode Disabled
Set-CsTeamsMeetingPolicy -Identity Global -StreamingAttendeeMode Enabled
```
„Nur-anzeigen“-Teilnehmer können nicht an einer Besprechung teilnehmen, wenn es in der Besprechung keine mehr Anzeigekapazität gibt oder wenn der Teilnehmer keine Berechtigung zum Umgehen der Lobby hat, basierend auf den Richtlinien oder Optionen für die Lobby. „Nur anzeigen“-Teilnehmer können keine nativen PPT-Freigabe Dateien sehen.

### <a name="meeting-expiration"></a>Ablauf der Besprechung

|Besprechungstyp  |Besprechung läuft nach diesem Zeitraum ab  |Jedes Mal, wenn Sie eine Besprechung starten oder aktualisieren, verlängert sich der Ablaufzeitpunkt um die entsprechende Zeit  |
|---------|---------|---------|
|Besprechung beginnen     |Startzeitpunkt + 8 Stunden         |Nicht zutreffend         |
|Regulär ohne Endzeitpunkt     |Startzeitpunkt + 60 Tage         | 60 Tage        |
|Regulär mit Endzeitpunkt     |Endzeitpunkt + 60 Tage         |60 Tage         |
|Wiederkehrend ohne Endzeitpunkt     |Startzeitpunkt + 60 Tage         |60 Tage         |
|Wiederkehrend mit Endzeitpunkt     |Endzeitpunkt des letzten Vorkommens + 60 Tage         |60 Tage         |

> [!NOTE]
> Microsoft Teams-Besprechungen haben ein Zeitlimit von 24 Stunden.

## <a name="teams-live-events"></a>Teams-Liveereignisse

|Funktion     | Obergrenze |
|------------|---------------|
|Zielgruppengröße | 10.000 Teilnehmer |
|Dauer des Ereignisses | 4 Stunden |
|Gleichzeitige Liveereignisse in einer Microsoft 365- oder Office 365-Organisation<sup>1</sup> | 15 |

<sup>1</sup> Sie können beliebig viele Live-Ereignisse planen, aber Sie können nur jeweils 15 ausführen. Sobald der Produzent einem Live-Ereignis beitritt, wird es als ausgeführt betrachtet. Der Produzent, der versucht, am 16. Live-Ereignis teilzunehmen, erhält eine Fehlermeldung.

Weitere Informationen zu Liveereignissen und eine Gegenüberstellung von Team-Liveereignissen und Skype-Livekonferenzen finden Sie unter [Teams-Liveereignisse und Skype-Livekonferenzen](teams-live-events/plan-for-teams-live-events.md#teams-live-events-and-skype-meeting-broadcast).

> [!IMPORTANT]
> **Das Limit für Microsoft 365 Live-Ereignisse wird erhöht**
>
> Damit Kunden den sich schnell ändernden Kommunikationsbedürfnissen gerecht werden können, wird das Limit für Microsoft 365 Live-Ereignisse vorübergehend bis zum 1. Oktober 2020 für Live-Ereignisse in Teams erhöht. Die nachstehenden Erhöhungen werden bereitgestellt:
>
> - Teilnehmerlimit: Ereignisse können bis zu 20 000 Teilnehmer unterstützen
> - Gleichzeitige Ereignisse: 50 Ereignisse können über einen Mandanten gleichzeitig gehostet werden
> - Ereignisdauer: die Ereignisdauer wurde auf 16 Stunden pro Sendung erhöht

## <a name="presence-in-outlook"></a>Anwesenheit in Outlook

Die Anwesenheit in Teams wird in Outlook ab der Outlook 2013-Desktop-App und höher unterstützt. Wenn Sie mehr über die Anwesenheit in Teams wissen möchten, lesen Sie [Anwesenheit von Benutzern in Teams](presence-admins.md).

## <a name="storage"></a>Speicher

Jedes Team in Microsoft Teams verfügt über eine Teamsite in SharePoint Online, und jeder Kanal in einem Team erhält einen Ordner innerhalb der Dokumentbibliothek der Standardteamsite. In einer Unterhaltung freigegebene Dateien werden automatisch zur Dokumentbibliothek hinzugefügt, und in SharePoint festgelegte Berechtigungen und Dateisicherheitsoptionen werden automatisch in Teams übernommen.

> [!NOTE]
> Jeder [private Kanal](https://docs.microsoft.com/microsoftteams/private-channels) hat seine eigene SharePoint-Websitesammlung.

Wenn Sie SharePoint Online nicht in Ihrem Mandanten aktiviert haben, können Microsoft Teams-Benutzer nicht immer Dateien in Teams freigeben. Benutzer im privaten Chat können Dateien auch nicht freigeben, weil OneDrive for Business (mit der SharePoint-Lizenz verknüpft) für diese Funktionalität erforderlich ist.

Beim Speichern der Dateien in der SharePoint Online-Dokumentbibliothek und OneDrive for Business werden alle auf der Mandantenebene konfigurierten Complianceregeln eingehalten. (Weitere Informationen finden Sie unter [Interaktion von SharePoint Online und OneDrive for Business mit Microsoft Teams](sharepoint-onedrive-interact.md).)

Da Teams in einem SharePoint Online-Backend für die Dateifreigabe ausgeführt wird, gelten die SharePoint-Einschränkungen für den Bereich „Dateien“ innerhalb eines Teams. Hier die entsprechenden Speichergrenzwerte für SharePoint Online:

|Feature                 |Microsoft 365 Business Basic  |Microsoft 365 Business Standard   |Office 365 Enterprise E1  |Office 365 Enterprise E3  |Office 365 Enterprise E5  |Office 365 Enterprise F1  |
|------------------------|---------|---------|---------|---------|---------|---------|
|Speicher                 |1 TB pro Organisation plus 10 GB pro erworbener Lizenz  |1 TB pro Organisation plus 10 GB pro erworbener Lizenz  |1 TB pro Organisation plus 10 GB pro erworbener Lizenz   |1 TB pro Organisation plus 10 GB pro erworbener Lizenz |1 TB pro Organisation plus 10 GB pro erworbener Lizenz  |1 TB pro Organisation           |
|Speicher für Teams-Dateien |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |
|Maximale Größe für Dateiuploads (pro Datei)    |15 GB    |15 GB    |15 GB    |15 GB    |15 GB    |15 GB    |

Kanäle werden durch Ordner innerhalb der SharePoint Online-Websitesammlung, die für das Team erstellt wurde, gesichert. Deshalb teilen sich Dateiregisterkarten in Kanälen die Speicherlimits des Teams, zu dem sie gehören.

Weitere Informationen finden Sie unter [SharePoint Online-Beschränkungen](https://support.office.com/article/SharePoint-Online-limits-8f34ff47-b749-408b-abc0-b605e1f6d498).

## <a name="tags"></a>Tags

|Feature  |Obergrenze  |
|---------|---------|
|Anzahl der Tags pro Team    | 100        |
|Anzahl der vorgeschlagenen Standardtags pro Team    | 25        |
|Anzahl der Teammitglieder, die einem Tag zugeordnet werden    |100         |
|Die Anzahl der Tags, die einem Benutzer zugewiesen werden.    |25         |

## <a name="contacts"></a>Kontakte

Microsoft Teams verwendet die folgenden Kontakte:

- Kontakte in der Active Directory Ihrer Organisation
- Kontakte, die dem Outlook-Standardordner des Benutzers hinzugefügt wurden

Microsoft Teams-Benutzer können mit jeder Person in der Active Directory Ihrer Organisation kommunizieren, und sie können jede Person in der Active Directory Ihrer Organisation als Kontakt bzw. zu ihren Kontaktlisten hinzufügen, indem sie zu **Chat** > **Kontakte** beziehungsweise zu **Anrufe** > **Kontakte** gehen.

Microsoft Teams-Benutzer können außerdem eine Person, die sich nicht in der Active Directory Ihrer Organisation befindet, unter **Anrufe** > **Kontakte** als Kontakt hinzufügen.

## <a name="browsers"></a>Browser

[!INCLUDE [browser-support](includes/browser-support.md)]

## <a name="operating-systems"></a>Betriebssysteme

Informationen zu den Betriebssystemanforderungen finden Sie unter [Beziehen von Clients für Microsoft Teams](get-clients.md).