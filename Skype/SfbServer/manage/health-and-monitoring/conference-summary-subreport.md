---
title: Zusammenfassender Konferenz-Unterbericht in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
description: 'Zusammenfassung: Informationen Sie zu den zusammenfassender Konferenz-Unterbericht in Skype für Business Server 2015.'
ms.openlocfilehash: 39c71ebfa5798d861a9b8afd8865486dba033c1d
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="conference-summary-subreport-in-skype-for-business-server-2015"></a>Zusammenfassender Konferenz-Unterbericht in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zu den zusammenfassender Konferenz-Unterbericht in Skype für Business Server 2015.
  
Der zusammenfassende Konferenzunterbericht stellt eine Gesamtübersicht zu gescheiterten Konferenzsitzungen bereit, bei denen Fehler aufgetreten sind. Diese gescheiterten Sitzungen sind weiter nach Sitzungstyp unterteilt: Konferenzzustandsobjekt-Sitzungen und MCU-Sitzungen.
  
## <a name="filters"></a>Filter

Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. In der folgenden Tabelle werden die Filter aufgelistet, die Sie im zusammenfassenden Konferenzunterbericht verwenden können.
  
**Filter im zusammenfassenden Unterbericht der Konferenz**

|**Name**|**Beschreibung**|
|:-----|:-----|
|**Von** <br/> |Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:  <br/> 07.07.2015 13:00  <br/> Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:  <br/> 07.07.2015  <br/> Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):  <br/> 03.07.2015  <br/> Eine Woche läuft immer von Sonntag bis einschließlich Samstag.  <br/> |
|**Bis** <br/> |Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:  <br/> 07.07.2015 13:00  <br/> Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:  <br/> 07.07.2015  <br/> Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):  <br/> 03.07.2015  <br/> Eine Woche läuft immer von Sonntag bis einschließlich Samstag.  <br/> |
|**Pool** <br/> |Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf **[Alle]** klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.<br/> |
   
## <a name="metrics"></a>Metriken

In der folgenden Tabelle sind die Metriken aufgelistet, die im zusammenfassenden Konferenzunterbericht angegeben werden.
  
**Metriken im zusammenfassenden Konferenzunterbericht der Konferenz**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Konferenzen insgesamt** <br/> |Nein  <br/> |Gesamtzahl der Konferenzen, die durchgeführt wurden.  <br/> |
|**Konferenzsitzungen insgesamt** <br/> |Nein  <br/> |Gesamtzahl der Konferenzsitzungen. Eine einzelne Konferenz kann mehrere Sitzungen haben. Beispielsweise kann eine Konferenz sowohl eine Konferenzzustandsobjekt-Sitzung als auch eine MCU-Sitzung umfassen.  <br/> |
|**Sitzungsfehlerrate insgesamt** <br/> |Nein  <br/> |Prozentsatz aller gescheiterten Konferenzen.  <br/> |
|**Konferenzzustandsobjekt-Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der Konferenzzustandsobjekt-Sitzungen.  <br/> |
|**Fehlerrate für Konferenzzustandsobjekt** <br/> |Nein  <br/> |Prozentsatz der gescheiterten Konferenzzustandsobjekt-Sitzungen.  <br/> |
|MCU-Sitzungen  <br/> |Nein  <br/> |Gesamtanzahl der MCU-Sitzungen.  <br/> |
|**MCU-Fehlerrate** <br/> |Nein  <br/> |Prozentsatz der gescheiterten MCU-Sitzungen.  <br/> |
|**MCU-Sitzungen nach Modalität** <br/> |Nein  <br/> |Gesamtanzahl der MCU-Sitzungen, gruppiert nach Modalität (z. B. Chatkonferenz).  <br/> |
|**Fehlerrate nach Modalität** <br/> |Nein  <br/> |Prozentsatz der gescheiterten MCU-Sitzungen, gruppiert nach Modalität (z. B. Chatkonferenz).  <br/> |
   
