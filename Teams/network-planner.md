---
title: Verwenden von Network Planner für Microsoft Teams
author: SerdarSoysal
ms.author: serdars
manager: serdars
ms.date: 06/24/2019
ms.topic: article
ms.service: msteams
ms.reviewer: svemu
audience: admin
description: Administratoren erfahren, wie Sie mithilfe des Netzwerk Planner Netzwerkanforderungen für Microsoft Teams ermitteln können.
localization_priority: Normal
search.appverid: MET150
ms.collection:
- M365-collaboration
- m365initiative-deployteams
f1.keywords:
- CSH
ms.custom:
- ms.teamsadmincenter.networkplanner.overview
- ms.teamsadmincenter.networkplanner.personas
- seo-marvel-apr2020
appliesto:
- Microsoft Teams
ms.openlocfilehash: 14bdc08656cdce18fc25b38ca8d226ac0e70cf27
ms.sourcegitcommit: 57fddb045f4a9df14cc421b1f6a228df91f334de
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "49030621"
---
# <a name="use-the-network-planner-for-microsoft-teams"></a>Verwenden von Network Planner für Microsoft Teams

Network Planner ist ein neues Tool, das im Team Admin Center zur Verfügung steht. Sie finden ihn unter **Planner**  >  **Network Planner**. Mit nur wenigen Schritten kann der Netzwerk Planner Ihnen dabei helfen, die Netzwerkanforderungen für die Verbindung von Microsoft Teams-Benutzern in Ihrer Organisation zu ermitteln und zu organisieren. Wenn Sie Ihre Netzwerkdetails und die Verwendung von Teams angeben, berechnet der Netzwerk Planner Ihre Netzwerkanforderungen für die Bereitstellung von Teams und Cloud-VoIP über die physischen Standorte Ihrer Organisation hinweg.

![Screenshot von Network Planner](media/network-planner.png)

Network Planner bietet Ihnen folgende Möglichkeiten:

- Erstellen Sie Darstellungen Ihrer Organisation mithilfe von Websites und von Microsoft empfohlenen Personas (Office-Mitarbeitern, Remotemitarbeitern und Teams Room System).

    > [!NOTE]
    > Die empfohlenen Personas wurden auf der Grundlage von Daten aus Teams entwickelt, die am besten verwendet werden, sowie typische Verwendungsmuster. Sie können jedoch zusätzlich zu den drei empfohlenen Personas bis zu drei benutzerdefinierte Personas erstellen.

- Generieren von Berichten und Berechnen der Bandbreitenanforderungen für die Verwendung durch Teams.

Um Network Planner verwenden zu können, müssen Sie ein globaler Administrator, Team Dienstadministrator oder Teams-Kommunikations Administrator sein.

## <a name="create-a-custom-persona"></a>Erstellen einer benutzerdefinierten Rolle

Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Rolle zu erstellen:

1. Wechseln Sie im Microsoft Teams Admin Center zum Netzwerk Planner.

2. Klicken Sie auf der Registerkarte **Personas** auf **+ benutzerdefinierte Rolle**. 

3. Fügen Sie im Bereich **neue benutzerdefinierte Rolle** einen Namen und eine Beschreibung für die neue Person hinzu.

4. Wählen Sie die Berechtigungen aus, die diese Person innerhalb der Organisation verwenden soll.

5. Klicken Sie auf **Speichern**.

## <a name="build-your-plan"></a>Erstellen Ihres Plans

Führen Sie die folgenden Schritte aus, um mit dem Erstellen Ihres Netzwerkplans zu beginnen:

1. Wechseln Sie im Microsoft Teams Admin Center zum Netzwerk Planner.

2. Klicken Sie auf der Registerkarte **Netzwerkplan** auf **Netzwerkplan hinzufügen**.

3. Geben Sie einen Namen und eine Beschreibung für Ihren Netzwerkplan ein. Der Netzwerkplan wird in der Liste der verfügbaren Pläne angezeigt.

4. Klicken Sie auf den Plan Namen, um den neuen Plan auszuwählen.

5. Fügen Sie Websites hinzu, um eine Darstellung des Netzwerk Setups Ihrer Organisation zu erstellen.

    Je nach Netzwerk Ihrer Organisation möchten Sie möglicherweise Websites verwenden, um ein Gebäude, einen Office-Standort oder etwas anderes darzustellen. Websites können über ein WAN verbunden sein, um die Freigabe von Internet-und/oder PSTN-Verbindungen zu ermöglichen. Um optimale Ergebnisse zu erzielen, erstellen Sie Websites mit lokalen Verbindungen, bevor Sie Websites erstellen, die eine Remoteverbindung mit dem Internet oder PSTN herstellen.

    So erstellen Sie eine Website:

    1. Fügen Sie einen Namen und eine Beschreibung für Ihre Website hinzu.

    2. Fügen Sie unter **Netzwerkeinstellungen** die Anzahl der Netzwerkbenutzer auf dieser Website hinzu (erforderlich).

    3. Hinzufügen von Netzwerkdetails: WAN-fähig, WAN-Kapazität, Internet-Ausstieg ( **lokal** oder **Remote** ) und PSTN-Ausgang (keine, lokal oder Remote).

      > [!NOTE]
      > Sie müssen WAN-und Internet Kapazitäts Nummern hinzufügen, um bestimmte Bandbreiten Empfehlungen anzuzeigen, wenn Sie einen Bericht generieren.

    4. Klicken Sie auf **Speichern**.

## <a name="create-a-report"></a>Erstellen eines Berichts

Nachdem Sie alle Websites hinzugefügt haben, können Sie einen Bericht wie folgt erstellen.

1. Klicken Sie auf der Registerkarte **Berichte** auf **Bericht starten**.

2. Verteilen Sie für jede Website, die Sie erstellen, die Anzahl der Benutzer auf die verfügbaren Personas. Wenn Sie die Microsoft Recommended Personas verwenden, wird die Nummer automatisch verteilt (80% Office Worker und 20% Remote Worker).

3. Nachdem Sie die Verteilung abgeschlossen haben, klicken Sie auf **Bericht generieren**.

    Der generierte Bericht zeigt die Bandbreitenanforderungen in verschiedenen Ansichten an, sodass Sie die Ausgabe klar verstehen können:
    - Eine Tabelle mit einzelnen Berechnungen zeigt die Bandbreitenanforderungen für die einzelnen zulässigen Aktivitäten an.
    - In einer zusätzlichen Ansicht werden die gesamten Anforderungen an die Bandbreite mit Empfehlungen angezeigt.

4. Klicken Sie auf **Speichern**. Ihr Bericht steht in der Liste Berichte zur späteren Anzeige zur Verfügung.

## <a name="example-scenario"></a>Beispielszenario

Ein Beispiel für die Verwendung des Netzwerk Planner zum Einrichten eines Netzwerkplans und zum Generieren eines Berichts mithilfe dieser Schritte finden Sie unter Herunterladen des Netzwerk Planers [How-To PowerPoint-Deck](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/blob/live/Teams/downloads/network-planner-how-to.pptx?raw=true) (nur Englisch).
