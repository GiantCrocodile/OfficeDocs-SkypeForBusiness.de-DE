---
title: 'Patienten-App für Teams-Administratoren '
author: jambirk
ms.author: jambirk
manager: serdars
audience: ITPro
ms.topic: article
ms.service: msteams
search.appverid: MET150
localization_priority: Normal
MS.collection:
- M365-collaboration
- Teams_ITAdmin_Healthcare
appliesto: Microsoft Teams
ms.reviewer: anach
description: Patienten-App für Teams-Administratoren
ms.openlocfilehash: 85f0d382de11b9259c6839aa8d0e556ad2512f5a
ms.sourcegitcommit: 2064c94eae82a5453674d38f0b28dcd6dc5c370e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "37885499"
---
# <a name="patients-app-overview"></a>Übersicht der Patienten-App

Die patients-Anwendung ist eine Microsoft Teams Store-App, die für alle Teams-Benutzer verfügbar ist. Die APP ermöglicht es Patienten Teams aus klinischen Arbeitern (wie Krankenschwestern, Ärzten, Sozialarbeitern), Listen von Patienten für Szenarien, die von runden und interdisziplinären Teambesprechungen bis hin zur allgemeinen Patientenüberwachung reichen, zu kuratiert und zu überprüfen.   

Die APP hat zwei Modi: 

- Der EMR-verbundene Modus, der über FHIR eine Verbindung mit EMRs herstellt. Die EMR-App für den verbundenen Modus bleibt in der privaten Vorschau und interessierte Kunden oder Administratoren können den Zugriff auf die APP anfordern, indem Sie Microsoft eine e-Mail unter teamsforhealthcare@Service.Microsoft.com mit Informationen zu Ihrem Office 365-Mandanten ablegen. 
- Der manuelle Modus, in dem Betreuerteams die Patienteninformationen manuell hinzufügen/einbringen können. Die Anwendung ist im Teams-App-Store verfügbar, damit Endbenutzer standardmäßig heruntergeladen werden und in der öffentlichen Vorschau angezeigt werden. Die APP kann mithilfe von [App-Setup Richtlinien in Microsoft Teams](../../teams-app-setup-policies.md) auf bestimmte Benutzer Abschnitte beschränkt werden.



## <a name="usage-example"></a>Verwendungsbeispiel

Während der runden Sitzungen bei jeder Schicht in medizinischen Stationen versammeln sich Kliniker an der Krankenstation, um über die neuesten Updates über den Fortschritt bei Patienten in der Gemeinde zu diskutieren.  Sie betonen die wichtigsten wichtigen Metriken (nicht unbedingt medizinisch oder ausdrücklich auf die medizinischen Unterlagen der Patienten) und stellen sicher, dass der Patient auf dem richtigen Gleitweg zur Entladung ist, basierend auf seiner Diagnose. Um diese Patienten umrunden zu können, richtet die Krankenschwester die Patienten-app in einem Team ein, in dem alle Ärzte hinzugefügt werden und Patienten zu einer Patientenliste hinzugefügt werden. Während der Runde greifen die Krankenschwestern und die anderen Betreuer für den Patienten auf die Microsoft Teams und die Patienten-App auf Ihren mobilen Geräten zu und aktualisieren relevante Patienteninformationen auf Ihrem Gerät, und alle anderen Personen im Betreuerteam können diese Updates und Notizen sehen und bleiben Sie synchron. Zweimal am Tag, am Anfang und am Ende einer Schicht, haben Sie auch mehrere displicinary-Teambesprechungen, um über die Patientenliste zu wechseln und die Patienten-APP zu verwenden, um sich selbst zu beerdigen und Informationen über jeden Patienten über die Patienten-App auf einem größeren Bildschirm zu teilen. Oft können sich bestimmte Kliniker auch Remote in diese Teams einwählen und dennoch Teil der Diskussion sein. 

## <a name="configure-patients-app"></a>Konfigurieren der Patienten-App

Informationen dazu, wie Sie Ihre Umgebung auf die Verwendung der EMR-Modus-Patienten-App vorbereiten, finden Sie unter [integrieren elektronischer Gesundheitsdatensätze in Microsoft Teams](patients-app.md). Außerdem müssen Sie [in Microsoft Teams die Richtlinien für die APP-Einrichtung verwalten](../../teams-app-setup-policies.md) anzeigen, um die Patienten-App für Ihre Organisation zu aktivieren.

<!-- For information on how your end users can access and install the Patients App to a team that they own or manage, you will need to see [End user documentation for the Patients App]() -->

<!-- add link out to client doc, doesn't seem to be available yet, Grant is finalizing -->

## <a name="frequently-asked-questions-faq"></a>Häufig gestellte Fragen (FAQ)

**Wo werden die Daten der Patienten-APP gespeichert?**

Alle von Endbenutzern in die Patienten-App eingegebenen Daten, einschließlich des Spalten-/Feld Schemas, der tatsächlichen Daten, die in die Liste und Listenelemente eingegeben wurden (also Patienten), werden in der sicheren und kompatiblen Exchange Online-Infrastruktur gespeichert. Alle Daten werden in dem Gruppenpostfach gespeichert, das dem Team zugeordnet ist. Diese Architektur ermöglicht der Patienten-APP die einfache Erfüllung von Daten Wohnsitz, staatlicher Cloud-Unterstützung (in der Zukunft) sowie andere Compliance-und Informationsschutz Features wie eDiscovery-Unterstützung. Die Patienten-APP arbeitet in einem Teambereich. Sie müssen eine Instanz der APP pro Team installieren.

<!-- add link to eDiscovery article for the Patients app, Mark Johnson will finalize soon -->

**Wo kann ich die Patienten-App abrufen?**

Wenn die patients-App für Ihre Organisation von Ihrem Administrator aktiviert ist, kann jeder Endbenutzer zum Teams-App-Store wechseln und die Patienten-APP einem Team hinzufügen, in dem Sie Mitglied sind. Weitere Informationen finden Sie unter [Verwalten von App-Setup Richtlinien in Microsoft Teams](../../teams-app-setup-policies.md).

**Kann ich in einem Team mehrere Instanzen der Patienten-APP haben, denn so funktioniert meine Station/Einheit?**

Derzeit können Sie nur eine Instanz der Patienten-App für ein bestimmtes Team und nur im Kanal "Allgemein" installieren. In der App können jedoch mehrere Listen erstellt werden, um Szenarien mit mehreren Kanälen oder Isolierung/Separation zu beheben. Standardmäßig können alle Mitglieder des Teams auf die Registerkarte "Patienten" im Kanal "Allgemein" zugreifen. 

**Kann ich alle Daten aus der Patienten-App exportieren?**
Nicht im Moment, aber diese Funktion wird in Kürze verfügbar sein. 

**Da diese APP Phi beherbergt, gibt es Audits, um unbefugten Zugriff zu verhindern oder Vorschriften zu erfüllen?**

Ja, das gibt es. Jede einzelne Benutzeroberflächen Aktion, die von einem Microsoft Teams-Benutzer in der Patienten-app ausgeführt wird, wird überwacht und im Security and Compliance Center zur Verfügung gestellt. Die Details werden im Artikel [hier](patients-audit.md) erläutert.


## <a name="related-topics"></a>Verwandte Themen

[Integration von elektronischen Datensätzen aus dem Gesundheitswesen in Microsoft Teams](patients-app.md)