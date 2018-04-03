---
title: Konferenzdetailbericht in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 2/13/2018
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
description: 'Zusammenfassung: Informationen Sie zu den detaillierten Konferenzbericht in Skype für Business Server 2015 verwendet.'
ms.openlocfilehash: 4c55b2f339aa3d591f01d73d0f60d8fbc0bb483f
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="conference-detail-report-in-skype-for-business-server-2015"></a>Konferenzdetailbericht in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zu den detaillierten Konferenzbericht in Skype für Business Server 2015 verwendet.
  
Der detaillierte Konferenzbericht enthält ausführliche Informationen zu allen Benutzern, die an einer Konferenz teilgenommen haben. Sie können beispielsweise Informationen wie Datum und Uhrzeit, an dem bzw. zu der ein Benutzer einer Konferenz beigetreten ist und die Konferenz verlassen hat, sowie den Benutzer-Agent des Endpunkts anzeigen, mit dem der Benutzer mit der Konferenz verbunden wurde. Darüber hinaus können Sie Informationen zu der Rolle des Benutzers in den einzelnen Konferenzen (z. B. Referent oder Teilnehmer) anzeigen. Der vielleicht wichtigste Aspekt ist, dass Sie auf einen Blick erkennen können, welche Benutzer der Konferenz erfolgreich beigetreten und sie abgeschlossen haben und welche Benutzer der Konferenz nicht beitreten konnten und sie daher nicht abgeschlossen haben.
  
## <a name="accessing-the-conference-detail-report"></a>Zugreifen auf den detaillierten Konferenzbericht

Auf den detaillierten Konferenzbericht kann über die folgenden Berichte zugegriffen werden:
  
- [Call Admission Control Report in Skype für Business Server 2015](call-admission-control-report.md) (durch Klicken auf die Metrik Detail für eine Konferenz)
    
- [Failure List Report in Skype für Business Server 2015](failure-list-report.md) (durch Klicken auf die Metrik "Konferenz")
    
- Der [Bericht über Benutzeraktivität in Skype für Business Server 2015](user-activity-report.md) (durch Klicken auf die Metrik "Konferenz-URI")
    
Über den detaillierten Konferenzbericht können Sie den [Diagnosebericht in Skype für Business Server 2015](diagnostic-report.md) zugreifen, durch Klicken auf die Metrik Diagnosebericht (Detail).
  
## <a name="filters"></a>Filter

Keine. Der detaillierte Konferenzbericht lässt sich nicht filtern.
  
## <a name="metrics"></a>Metriken

In der folgenden Tabelle werden die Informationen aus dem Abschnitt zu Konferenzinformationen des detaillierten Konferenzberichts aufgeführt.
  
**Konferenzinformationen – Metriken**

|**Name**|**Beschreibung**|
|:-----|:-----|
|**Konferenz-URI** <br/> |Der Konferenz zugewiesener URI. Beispiel:  <br/> SIP:kmyer@litwareinc.com;GRUU;Opaque=App:conf:Focus:ID:drg2y8v4  <br/> |
|**Pool-FQDN** <br/> |Vollqualifizierter Domänenname des Registrierungspools oder Edgeservers in einer Sitzung.  <br/> |
|**Startzeitpunkt** <br/> |Datum und Uhrzeit, an dem bzw. zu der Konferenz begann.  <br/> |
|**Organisator** <br/> |SIP-Adresse des Benutzers, der die Sitzung organisiert hat.  <br/> |
|**Endzeitpunkt** <br/> |Datum und Uhrzeit, an dem bzw. zu der die Konferenz endete.  <br/> |
   
In der folgenden Tabelle werden die Informationen aus dem Abschnitt zur Konferenzteilnahme des detaillierten Konferenzberichts aufgeführt.
  
**Konferenzteilnahme – Metriken**

|**Name**|**Beschreibung**|
|:-----|:-----|
|**User** <br/> |SIP-Adresse des Benutzers, der an der Konferenz teilgenommen hat.  <br/> |
|**Rolle** <br/> |Rolle (z. B. Referent) des Konferenzteilnehmers.  <br/> |
|**Verbindung** <br/> |Netzwerkverbindungen (in der Regel „From Internal“ oder „From External“) des Teilnehmers.  <br/> |
|**Beitrittszeitpunkt** <br/> |Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer der Konferenz beigetreten ist.  <br/> |
|**Beendigungszeitpunkt** <br/> |Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer die Konferenz verlassen hat.  <br/> |
|**Benutzer-Agent** <br/> |Der Bezeichner für die vom Endpunkt des Teilnehmers verwendete Software.  <br/> |
|**Diagnoseberichte** <br/> |Enthält Diagnose- und Problembehandlungsinformationen, einschließlich SIP-Antwortcodes, Diagnoseheader, Zeitpunkt des Konferenzbeitritts und Diagnose-IDs für fehlgeschlagene Sitzungen.  <br/> |
   
In der folgenden Tabelle sind die Informationen in den Abschnitt zu Konferenzmodalitäten des detaillierten Konferenzberichts aufgeführt.
  
**Konferenzmodalitäten – Metriken**

|**Name**|**Beschreibung**|
|:-----|:-----|
|**User** <br/> |SIP-Adresse des Benutzers, der an der Konferenz teilgenommen hat.  <br/> |
|**Beitrittszeitpunkt** <br/> |Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer der Konferenz beigetreten ist.  <br/> |
|**Beendigungszeitpunkt** <br/> |Datum und Uhrzeit, an dem bzw. zu der ein Teilnehmer die Konferenz verlassen hat.  <br/> |
|**Konferenzserver-URI** <br/> |URI für den in der Konferenz verwendeten Konferenzserver.  <br/> |
|**Diagnoseberichte** <br/> |Enthält Diagnose- und Problembehandlungsinformationen, einschließlich SIP-Antwortcodes, Diagnoseheader, Zeitpunkt des Konferenzbeitritts und Diagnose-IDs für fehlgeschlagene Sitzungen.  <br/> |
   
