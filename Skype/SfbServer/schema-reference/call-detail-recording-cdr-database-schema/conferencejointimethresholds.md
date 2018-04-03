---
title: ConferenceJoinTimeThresholds-Tabelle in Skype für Business Server 2015
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
description: 'Die Tabelle conferencejointimethresholds enthält die klassifizierungsgrenzen, die von der Konferenz beitreten Zeit Summary Report verwendet. Die Zusammenfassung der Konferenzbeitrittszeit enthält eine Zusammenfassung den Betrag Zeitaufwand für Benutzer erfolgreich eine Konferenz beitreten; Diese Zeitwerte werden sowohl als durchschnittlich und in einem der folgenden Kategorien gemeldet:'
ms.openlocfilehash: 3646337c9e9f20ac0b1dabfdd5504ce83dfa5c40
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="conferencejointimethresholds-table-in-skype-for-business-server-2015"></a>ConferenceJoinTimeThresholds-Tabelle in Skype für Business Server 2015
 
Die Tabelle conferencejointimethresholds enthält die klassifizierungsgrenzen, die von der Konferenz beitreten Zeit Summary Report verwendet. Die Zusammenfassung der Konferenzbeitrittszeit enthält eine Zusammenfassung den Betrag Zeitaufwand für Benutzer erfolgreich eine Konferenz beitreten; Diese Zeitwerte werden sowohl als durchschnittlich und in einem der folgenden Kategorien gemeldet:
  
- Weniger als 2 Sekunden.
    
- Zwischen 2 Sekunden und 5 Sekunden.
    
- Zwischen 5 und 10 Sekunden.
    
- Mehr als 10 Sekunden.
    
Die Tabelle conferencejointimethresholds enthält die klassifizierungswerte 2 Sekunden, 5 Sekunden und 10 Sekunden.
  
Diese Tabelle wurde in Microsoft Lync Server 2013 eingeführt.
  
|**Spalte**|**Datentyp**|**Schlüssel/Index**|**Details**|
|:-----|:-----|:-----|:-----|
|**ThresholdId** <br/> |int  <br/> |Primary  <br/> |Eindeutiger Bezeichner für die Klassifikation.  <br/> |
|**ThresholdValue** <br/> |int  <br/> || Die Obergrenze für die Klassifikation. Zulässige Werte: <br/>  2 <br/>  5 <br/>  10 <br/> |
   
