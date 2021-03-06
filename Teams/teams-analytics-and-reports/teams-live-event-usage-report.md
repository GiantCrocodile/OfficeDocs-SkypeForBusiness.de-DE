---
title: Microsoft Teams Live-Ereignis Verwendungsbericht
author: LanaChin
ms.author: v-lanac
manager: serdars
audience: Admin
ms.topic: article
ms.service: msteams
ms.reviewer: svemu
f1.keywords:
- NOCSH
localization_priority: Normal
search.appverid: MET150
ms.collection:
- M365-collaboration
description: Hier erfahren Sie, wie Sie den Bericht zur Live-Ereignis Verwendung von Teams im Microsoft Teams Admin Center verwenden, um sich einen Überblick über die Aktivitäten von Team Live Events in Ihrer Organisation zu verschaffen.
appliesto:
- Microsoft Teams
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c093464c67fed18a5c5528929f006b7931fd1d9b
ms.sourcegitcommit: bd13aecbb25c14e17d1b64343df6d80c90b2aa45
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "46803957"
---
# <a name="microsoft-teams-live-event-usage-report"></a>Microsoft Teams Live-Ereignis Verwendungsbericht

Der Bericht "Live-Ereignis Verwendung" von Teams im Microsoft Teams Admin Center zeigt die Aktivitätsübersicht für Live Ereignisse in Ihrer Organisation an. Sie können die Nutzungsinformationen, einschließlich Ereignisstatus, Startzeit, Ansichten und Produktionstyp für jedes Ereignis anzeigen. Sie können Einblicke in Nutzungstrends gewinnen und sehen, wer in Ihrer Organisation Live-Events plant, präsentiert und produziert.

## <a name="view-the-live-event-usage-report"></a>Anzeigen des Berichts zur Live-Ereignis Nutzung

1. Klicken Sie in der linken Navigationsleiste des Microsoft Teams admin Centers auf **Analytics & Berichte**  >  **Nutzungsberichte**. Wählen Sie auf der Registerkarte **Berichte anzeigen** unter **Bericht**die Option **Teams Live-Ereignis Nutzung**aus.
2. Wählen Sie unter **Datumsbereich**einen vordefinierten Bereich aus, oder legen Sie einen benutzerdefinierten Bereich fest. Sie können einen Bereich so einstellen, dass Daten bis zu einem Jahr, sechs Monate vor und nach dem aktuellen Datum, angezeigt werden.
3. Optional Unter **Organizer**können Sie auswählen, dass nur Live-Ereignisse angezeigt werden, die von einem bestimmten Benutzer organisiert werden.
4. Klicken Sie auf **Bericht ausführen**.  

    ![Screenshot des Berichts zur Verwendung von Live-Ereignissen in Teams im Team Admin Center mit Beschriftungen](../media/teams-live-event-usage-report-with-callouts.png "Screenshot des Berichts zur Verwendung von Live-Ereignissen in Teams im Team Admin Center mit Beschriftungen")

## <a name="interpret-the-report"></a>Interpretieren des Berichts

|Beschriftung |Beschreibung  |
|--------|-------------|
|**1**   |Der Live-Ereignisbericht "Teams" kann für Trends in den letzten 7 Tagen, 28 Tagen oder einem von Ihnen festgelegten benutzerdefinierten Datumsbereich angezeigt werden. |
|**2**   |Jeder Bericht hat ein Datum, zu dem er generiert wurde. Der Bericht reflektiert nahezu Echtzeitaktivitäten, wenn die Seite aktualisiert wird. |
|**3**   |<ul><li>Die X-Achse im Diagramm stellt den ausgewählten Datumsbereich für den Bericht dar.</li> <li> Die Y-Achse entspricht der Gesamtanzahl der Ansichten.</li> </ul>Zeigen Sie mit der Maus auf den Punkt an einem bestimmten Datum, um die Anzahl der Ansichten für alle Live Ereignisse an diesem Datum anzuzeigen.|
|**4**   |Die Tabelle enthält eine Zusammenfassung der einzelnen Live Ereignisse. <ul><li>**Event** ist der Anzeigename des Live-Ereignisses. Klicken Sie auf den Ereignisnamen, um [Weitere Details](#view-event-details) zum Ereignis abzurufen. </li> <li>Die **Startzeit** bezieht sich auf das Anfangsdatum und die Startzeit des Ereignisses.</li> <li>Der **Ereignis Status** zeigt an, ob das Ereignis stattgefunden hat.  </li><li>**Organizer** ist der Name des Ereignis Organisators.</li> <li>**Referenten** sind die Namen der Veranstaltungs Referenten.</li><li>**Hersteller** sind die Namen der Veranstaltungs Hersteller.</li><li>**Ansichten** ist die Anzahl der eindeutigen Ansichten nach Abschluss des Ereignisses.</li><li>**Aufzeichnung** zeigt an, ob die Aufzeichnungseinstellung aktiviert oder deaktiviert ist.</li><li>**Produktionstyp** zeigt an, ob das Ereignis in Teams oder von einer externen Anwendung oder einem Gerät erzeugt wird.</li></li> </ul>Beachten Sie, dass der Benutzername in der Tabelle als "--" angezeigt wird, wenn ein Benutzerkonto in Azure AD nicht mehr vorhanden ist. <br><br>Um in der Tabelle die gewünschten Informationen anzuzeigen, stellen Sie sicher, dass Sie der Tabelle die entsprechenden Spalten hinzufügen. |
|**5**   |Wählen Sie **Spalten bearbeiten** aus, um Spalten zur Tabelle hinzuzufügen oder daraus zu entfernen.|

## <a name="notes"></a>Hinweise
Es werden bis zu 100-Live Ereignisse angezeigt, die den aktuellen Berichtkriterien entsprechen. Wenn Sie weitere Live Ereignisse anzeigen möchten, wenden Sie Datumsfilter an, um die Listengröße zu verringern.

## <a name="view-event-details"></a>Anzeigen von Ereignisdetails

Auf der Seite Live-Ereignisdetails erhalten Sie eine Zusammenfassung der Details zu einem Live Ereignis und eine Auflistung aller Dateien, einschließlich der Protokolle und Aufzeichnungen, die dem Ereignis zugeordnet sind. Klicken Sie auf einen Dateinamen, um die Datei anzuzeigen oder herunterzuladen.

![Screenshot mit Details zu einem Live Ereignis](../media/teams-live-event-usage-report-event-detail.png)

Wenn Ihre Organisation für [Hive](https://www.hivestreaming.com/partners/integration-partners/microsoft/) ECDN oder [Kollective](https://kollective.com) ECDN aktiviert ist, können Sie zusätzliche Teilnehmer-Analysen abrufen, indem Sie auf den Link Partner Bericht klicken.

## <a name="related-topics"></a>Verwandte Themen

- [Teams – Analyse und Berichterstellung](teams-reporting-reference.md)
- [Was sind Teams-Liveereignisse?](../teams-live-events/what-are-teams-live-events.md)
