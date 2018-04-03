---
title: Konfigurieren von VoIP-Richtlinien, PSTN-Verwendungsdatensätzen und VoIP-Routen in Skype for Business 2015
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Admin
ms.assetid: 1e5a15f9-6f42-4dc6-baaa-24daf54afc4d
description: 'Zusammenfassung: Informationen Sie zum Konfigurieren von VoIP-Richtlinien, PSTN-verwendungsdatensätzen und VoIP-Routen in Skype für Business Server 2015.'
ms.openlocfilehash: d238703b98ebe532b2370456212760620c30ebf4
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="configure-voice-policies-pstn-usage-records-and-voice-routes-in-skype-for-business-2015"></a>Konfigurieren von VoIP-Richtlinien, PSTN-Verwendungsdatensätzen und VoIP-Routen in Skype for Business 2015
 
**Zusammenfassung:** Informationen Sie zum Konfigurieren von VoIP-Richtlinien, PSTN-verwendungsdatensätzen und VoIP-Routen in Skype für Business Server 2015.
  
VoIP-Richtlinien, PSTN-Verwendungsdatensätze und VoIP-Routen stehen in enger Beziehung zueinander. Zur Konfiguration von VoIP-Richtlinien wird eine Reihe von Anruffunktionen ausgewählt. Anschließend wird die Richtlinie einem Satz von PSTN-Verwendungsdatensätzen zugewiesen, in denen die Rechte für die Benutzer oder Gruppen festgelegt sind, denen die VoIP-Richtlinie zugewiesen wird. Auch VoIP-Routen werden PSTN-Verwendungsdatensätze zugewiesen, um Routen und die für ihre Verwendung autorisierten Benutzer einander zuzuordnen. Benutzer können also nur Anrufe über Routen tätigen, für die sie passende PSTN-Verwendungsdatensätze besitzen.
  
Der empfohlene Workflow für eine neue Enterprise-VoIP-Bereitstellung besteht darin, zunächst eine VoIP-Richtlinie mit den geeigneten PSTN-Verwendungsdatensätzen zu konfigurieren und anschließend den einzelnen PSTN-Verwendungsdatensätzen die entsprechenden Routen zuzuordnen. 
  
> [!NOTE]
> Sie können auch VoIP-Richtlinien *Benutzerebene* erstellen und diese für einzelne Benutzer oder Gruppen zuweisen.
  
Die einzelnen Schritte zur Durchführung dieser Aufgaben finden Sie in den Verfahren in diesem Abschnitt.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen oder Ändern einer VoIP-Richtlinie und Konfigurieren von PSTN-Verwendungseinträge in Skype für Business 2015](voice-policy-and-pstn-usage-records.md)
    
- [Konfigurieren des Wechsels der Voicemail in Skype für Business 2015](configure-voice-mail-escape.md)
    
- [Anzeigen von PSTN-Verwendungseinträge in Skype für Business 2015](view-pstn-usage-records.md)
    
- [Erstellen oder Ändern einer VoIP-Route in Skype für Business 2015](create-or-modify-a-voice-route.md)
    
- [Exportieren oder Importieren einer VoIP-routenkonfigurationsdatei in Skype für Business 2015](voice-route-configuration-import-export.md)
    
- [Veröffentlichen von ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md)
    
