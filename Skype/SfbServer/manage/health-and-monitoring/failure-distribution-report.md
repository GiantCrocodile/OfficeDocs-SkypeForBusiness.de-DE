---
title: Bericht über Fehlerverteilung in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
description: 'Zusammenfassung: Informationen Sie zu den Bericht über Fehlerverteilung in Skype für Business Server 2015.'
ms.openlocfilehash: 002f8e9b72ded0d5793b775e445cd57f20f35af5
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="failure-distribution-report-in-skype-for-business-server-2015"></a>Bericht über Fehlerverteilung in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zu den Bericht über Fehlerverteilung in Skype für Business Server 2015.
  
Der Bericht über Fehlerverteilung ordnet Sitzungen, bei denen ein Fehler aufgetreten ist, in folgende Kategorien ein:
  
- Häufigste Diagnosegründe
    
- Häufigste Modalitäten
    
- Häufigste Pools
    
- Häufigste Quellen
    
- Häufigste Komponenten
    
- Häufigste Absenderbenutzer
    
- Häufigste Empfängerbenutzer
    
- Häufigste Absenderbenutzer-Agenten
    
Anhand dieser Kategorien können Sie genau bestimmen, wo ein Problem aufgetreten ist und in einigen Fällen auch die Ursache feststellen. Angenommen, an einem Tag sind bei 242 Audio- und Videositzungen Fehler aufgetreten. Wenn Sie sich den Bericht über Fehlerverteilung ansehen, stellen Sie möglicherweise fest, dass 237 dieser gescheiterten Sitzungen im Dublin-Pool aufgetreten sind. Dies gibt Ihnen einen guten Ausgangspunkt zum Einkreisen der Ursache und Diagnostizieren dieser Fehler. Wenn Sie in der Kategorie **Häufigste Pools** auf den Dublin-Pool klicken, sehen Sie einen Bericht über Fehlerverteilung nur für diesen Pool. Sie können dann mit der Analyse des Dublin-Pools beginnen, um herauszufinden, warum es so viele Schwierigkeiten gab.
  
## <a name="viewing-the-failure-distribution-report"></a>Anzeigen des Berichts über Fehlerverteilung

Sie können auf den Bericht über Fehlerverteilung von einem der folgenden Berichte zugreifen, indem Sie entweder auf die Metrik **Anzahl der erwarteten Fehler** oder **Anzahl der unerwarteten Fehler** klicken:
  
- [Bericht über häufigste Fehler in Skype für Business Server 2015](top-failures-report.md)
    
- [Diagnosebericht Konferenz in Skype für Business Server 2015](conference-diagnostic-report.md)
    
- [Diagnosebericht über Peer-zu-Peer-Aktivität in Skype für Business Server 2015](peer-to-peer-activity-diagnostic-report.md)
    
Der Bericht über Fehlerverteilung können Sie eine der folgenden Metriken [Failure List Report in Skype für Business Server 2015](failure-list-report.md)anzeigen klicken:
  
- Wichtigste Diagnosegründe (Sitzungen)
    
- Wichtigste Modalitäten (Sitzungen)
    
- Wichtigste Pools (Sitzungen)
    
- Wichtigste Quellen (Sitzungen)
    
- Wichtigste Komponenten (Sitzungen)
    
- Wichtigste Absenderbenutzer (Sitzungen)
    
- Wichtigste Empfängerbenutzer (Sitzungen)
    
- Wichtigste Absenderbenutzer-Agenten (Sitzungen)
    
## <a name="using-the-failure-distribution-report"></a>Verwenden des Berichts über Fehlerverteilung

Je nach Ihrer Monitorgröße und Bildschirmauflösung werden einige Daten im Bericht über Fehlerverteilung möglicherweise abgeschnitten, wenn Sie auf dem Bildschirm angezeigt werden. Dies ist insbesondere bei Agent-Benutzern der Fall, die sehr lange Bezeichnungen haben können. Auf dem Bildschirm wird ein Benutzer-Agent mit dem Namen „UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)“ z. B. nur teilweise angezeigt: 
  
UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...
  
Sie können aber die gesamte Bezeichnung anzeigen, indem Sie die Maus über den gekürzten Wert halten.
  
Eine interessante Metrik, nach der Sie im Bericht über Fehlerverteilung filtern können, ist die Diagnose-ID. Wenn Sie dieselbe Diagnose-ID auch in anderen Berichten sehen, können Sie nach dieser ID im Bericht über Fehlerverteilung filtern. Sie erhalten dann einen sehr detaillierten Einblick darüber, wo genau und wie oft diese ID in einer gescheiterten Sitzung gemeldet wurde.
  
## <a name="filters"></a>Filter

Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Mit dem Bericht über Fehlerverteilung können Sie beispielsweise nach Kriterien wie dem Aktivitätstyp (Peer-to-Peer-Sitzung oder Konferenzsitzung) oder nach der Diagnose-ID der jeweiligen fehlgeschlagenen Sitzung filtern.
  
In der folgenden Tabelle sind die Filter aufgeführt, die Sie im Bericht über Fehlerverteilung verwenden können.
  
**Fehler bei Filter im Bericht**

|**Name**|**Beschreibung**|
|:-----|:-----|
|**Von** <br/> |Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:  <br/> 07.07.2015 13:00  <br/> Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:  <br/> 07.07.2015  <br/> Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):  <br/> 03.07.2015  <br/> Eine Woche läuft immer von Sonntag bis einschließlich Samstag.  <br/> |
|**Bis** <br/> |Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:  <br/> 07.07.2015 13:00  <br/> Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:  <br/> 07.07.2015  <br/> Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):  <br/> 03.07.2015  <br/> Eine Woche läuft immer von Sonntag bis einschließlich Samstag.  <br/> |
|**Pool** <br/> |Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf **[Alle]** klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.<br/> |
|**Aktivitätstyp** <br/> | Aktivitätstyp, nach dem gefiltert wird. Wählen Sie eine der folgenden Optionen aus: <br/>  [Alle] <br/>  Peer-to-Peer <br/>  Konferenz <br/> |
|**Sitzungskategorie** <br/> | Gibt an, ob die betreffende Aktivität erfolgreich war oder nicht. Wählen Sie eine der folgenden Optionen aus: <br/>  [Alle] <br/>  Erfolg <br/>  Erwarteter Fehler <br/>  Unerwarteter Fehler <br/>  Ein „erwarteter Fehler“ ist ein Fehler, der zu erwarten ist. Hat beispielsweise ein Benutzer seinen Status auf „Nicht stören“ gesetzt, ist zu erwarten, dass alle Anrufe an diesen Benutzer fehlschlagen. Ein „unerwarteter Fehler“ ist ein Fehler, der in einem ansonsten scheinbar fehlerfreien System auftritt. Beispielsweise sollte ein Anruf nicht abgebrochen werden, während der Anrufer sich in der Warteschleife befindet. In diesem Fall würde der Fehler als „unerwartet“ gekennzeichnet. <br/> |
|**Diagnose-ID** <br/> |Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt. Diagnostics-Header sind optional (SIP-Sitzungen ohne diese Header sind möglich) und Diagnose-IDs werden nur für Sitzungen berichtet, bei denen Probleme aufgetreten sind.  <br/> |
   
## <a name="metrics-for-top-diagnostic-reasons"></a>Metriken für die wichtigsten Diagnosegründe

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf der am häufigsten berichteten Diagnose-ID.
  
**Metriken für die wichtigsten Diagnosegründe**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf Diagnose-IDs. Die Diagnose-ID ist eine eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt.  <br/> |
|**Häufigste Diagnosegründe** <br/> |Nein  <br/> |In einer Sitzung generierte Diagnose-ID.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen, für die die angegebene Diagnose-ID generiert wurde.  <br/> |
   
## <a name="metrics-for-top-modalities"></a>Metriken für die wichtigsten Modalitäten

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Sitzungsmodalitäten, bei denen die meisten Fehler auftraten.
  
**Metriken für die wichtigsten Modalitäten**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung basierend auf der gescheiterten Sitzung und auf dem Sitzungstyp (z. B. Audio-/Video-Konferenz oder Peer-to-Peer-Dateiübertragungssitzung).  <br/> |
|**Häufigste Modalitäten** <br/> |Nein  <br/> |Sitzungstyp  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen mit der angegebenen Modalität.  <br/> |
   
## <a name="metrics-for-top-pools"></a>Metriken für die wichtigsten Pools

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Pools, bei denen die meisten Fehler auftraten.
  
**Metriken für die wichtigsten Pools**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem Registrar-Pool oder Edge-Server, auf dem die Sitzung abgehalten wurde.  <br/> |
|**Häufigste Pools** <br/> |Nein  <br/> |Name des Registrar-Pools oder Edgeservers.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen pro Registrar-Pool oder Edge-Server.  <br/> |
   
## <a name="metrics-for-top-sources"></a>Metriken für die wichtigsten Quellen

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Computern, bei denen die meisten Fehler auftraten.
  
**Metriken für die wichtigsten Quellen**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen pro Computer.  <br/> |
|**Häufigste Quellen** <br/> |Nein  <br/> |Name des Computers, auf dem die Sitzung fehlgeschlagen ist.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen pro Computer.  <br/> |
   
## <a name="metrics-for-top-components"></a>Metriken für die wichtigsten Komponenten

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Komponenten, bei denen die meisten Fehler auftraten.
  
**Metriken für die wichtigsten Komponenten**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf Komponente (z. B. ExumRouting, Gruppenchat oder MediationServer).  <br/> |
|**Häufigste Komponenten** <br/> |Nein  <br/> |Name der für die fehlgeschlagene Sitzung verwendeten Komponente.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen pro Komponente.  <br/> |
   
## <a name="metrics-for-top-from-users"></a>Metriken für die wichtigsten Absenderbenutzer

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Benutzern, bei denen beim Versuch, jemanden anzurufen, die meisten Fehler auftraten (als Absenderbenutzer bezeichnet).
  
**Metriken für die wichtigsten von Benutzern**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem Benutzer, der zur Teilnahme an der Sitzung eingeladen wurde.  <br/> |
|**Häufigste Absenderbenutzer** <br/> |Nein  <br/> |SIP-Adresse des Benutzers, der zur Teilnahme an der Sitzung eingeladen wurde.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen pro Benutzer.  <br/> |
   
## <a name="metrics-for-top-to-users"></a>Metriken für die wichtigsten Empfängerbenutzer

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Benutzern, bei denen die meisten Fehler auftraten, wenn sie von einem anderen Benutzer angerufen wurden (als Empfängerbenutzer bezeichnet).
  
|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem Benutzer, der die Sitzung initiiert hat.  <br/> |
|**Häufigste Empfängerbenutzer** <br/> |Nein  <br/> |SIP-Adresse des Benutzers, der die Sitzung initiiert hat.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen pro Benutzer.  <br/> |
   
## <a name="metrics-for-top-user-agents"></a>Metriken für die wichtigsten Benutzer-Agenten

In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf der Endpunktsoftware, bei der die meisten Fehler auftraten.
  
**Metriken für die wichtigsten Benutzer-Agents**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Rang** <br/> |Nein  <br/> |Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem in der Sitzung verwendeten Benutzer-Agent (Software), z. B. RTCC/4.0.0.0 Inbound Routing/4.0.0.0.  <br/> |
|**Wichtigste Benutzer-Agenten** <br/> |Nein  <br/> |Name des in der fehlgeschlagenen Sitzung verwendeten Benutzer-Agent.  <br/> |
|**Sitzungen** <br/> |Nein  <br/> |Gesamtanzahl der fehlgeschlagenen Sitzungen pro Benutzer-Agent.  <br/> |
   
