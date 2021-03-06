---
title: Migration zu Skype for Business Server 2019
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: ITPro
ms.topic: quickstart
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
description: Die Themen in diesem Abschnitt führen Sie durch den Migrationsprozess zu Skype for Business Server 2019.
ms.openlocfilehash: 860fce550de33ed726bbbe723c8c7677ff09fc1c
ms.sourcegitcommit: 62946d7515ccaa7a622d44b736e9e919a2e102d0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2020
ms.locfileid: "44752617"
---
# <a name="migration-to-skype-for-business-server-2019"></a>Migration zu Skype for Business Server 2019

Die Themen in diesem Abschnitt führen Sie durch den Migrationsprozess zu Skype for Business Server 2019. In diesem Artikel wird das Migrieren von lync Server 2013 oder Skype for Business Server 2015 zu Skype for Business Server 2019 behandelt.

> [!IMPORTANT]
> Im gesamten Inhalt verwenden wir den Begriff *Legacy* , um auf die Legacy lync Server 2013 oder Skype for Business Server 2015 zu referenzieren, die Sie zu Skype for Business Server 2019 migrieren.
  
> [!IMPORTANT]
> In diesem Leitfaden werden die Schritte beschrieben, die im Allgemeinen zur Ausführung der einzelnen Migrationsphasen erforderlich sind. Es werden nicht alle möglichen Vorversionen der Bereitstellungstopologie oder jedes mögliche Migrationsszenario behandelt. Daher müssen Sie möglicherweise nicht alle beschriebenen Schritte ausführen, oder Sie müssen abhängig von Ihrer Bereitstellung möglicherweise zusätzliche Schritte ausführen. Dieses Handbuch enthält auch Beispiele für Überprüfungsschritte. Anhand dieser Überprüfungsschritte können Sie verstehen, worauf Sie achten müssen, um sicherzustellen, dass jede Phase beim Fortschreiten der Migration erfolgreich abgeschlossen wird. Passen Sie diese Überprüfungsschritte an den jeweiligen Migrationsprozess an. 
  
Dieses Handbuch enthält Informationen, die speziell auf die Aktualisierung Ihrer vorhandenen Bereitstellung eingehen. Die Änderung Ihrer vorhandenen Topologie wird darin nicht behandelt. In diesem Handbuch wird nicht die Implementierung neuer Funktionen behandelt. Wenn ein ausführliches Verfahren an anderer Stelle dokumentiert wird, werden Sie in diesem Leitfaden zum Artikel oder Artikel Abschnitt geleitet. 
  
In diesem Artikel werden die in der folgenden Liste angegebenen Begriffe definiert.
  
**Migration:** Verschieben der Produktionsbereitstellung von lync Server 2013 oder Skype for Business Server 2015 auf Skype for Business Server 2019.
    
**Koexistenz:** Die temporäre Umgebung, die während der Migration vorhanden ist, wenn einige Funktionen zu Skype for Business Server 2019 migriert wurden und andere Funktionen weiterhin in einer früheren Version verfügbar sind.
    
**Interoperabilität:** Die Möglichkeit, dass Ihre Bereitstellung während des Zeitraums der Koexistenz erfolgreich ausgeführt werden kann.

**Legacy:** Das System, von dem Sie die Migration fortfahren, das entweder lync Server 2013 oder Skype for Business Server 2015 ist.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Vorbereiten der Migration](before-you-begin-the-migration.md)
    
- [Phase 1: Planen der Migration](phase-1-plan-your-migration.md)
    
- [Phase 2: Vorbereitung der Migration](phase-2-prepare-for-migration.md)
    
- [Phase 3: Bereitstellen des Pilotpools](phase-3-deploy-pilot-pool.md)
    
- [Phase 4: verlagern von Testbenutzern in den Pilot Pool](phase-4-move-test-users-to-the-pilot-pool.md)
    
- [Phase 5: Hinzufügen von Edgeservern zum Pilotpool](phase-5-add-edge-server-to-pilot-pool.md)
    
- [Phase 6: Migration von der Pilotbereitstellung zur Produktionsbereitstellung](phase-6-move-from-pilot-deployment-into-production.md)
    
- [Phase 7: Aufgaben nach der Migration abschließen](phase-7-complete-post-migration-tasks.md)
    
- [Phase 8: Außerbetriebsetzen der Legacypools](phase-8-decommission-legacy-pools.md)
    

