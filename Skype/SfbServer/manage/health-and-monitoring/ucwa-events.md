---
title: UCWA-Ereignisse in Skype for Business Server
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
description: 'Zusammenfassung: erfahren Sie mehr über die Unified Communications Web API (UCWA) in Skype for Business Server.'
ms.openlocfilehash: db6aee15564fe9fca05c33ec5a6dd37988195956
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41817624"
---
# <a name="ucwa-events-in-skype-for-business-server"></a>UCWA-Ereignisse in Skype for Business Server
 
**Zusammenfassung:** Erfahren Sie mehr über die Unified Communications Web API (UCWA) in Skype for Business Server.
  
Skype for Business Server verwendet die Unified Communications Web-API (UCWA) für eine Reihe von Zwecken, vom Zugriff auf Microsoft Exchange für Kontakt suchen bis zur Aktualisierung der Anwesenheitsinformationen für mobile Clients.
  
UCWA zeichnet Einträge zum Betriebsverhalten als die Ereignistypen „Information“, „Warnung“ und „Fehler“ auf. In der folgenden Tabelle sind die Ereignisse beschrieben, die von den UCWA-Komponenten geschrieben werden können.
  
|**Ereigniskennung**|**Ereignistyp**|**Zusammenfassung**|**Ursache und Lösung**|
|:-----|:-----|:-----|:-----|
|20001  <br/> |Information  <br/> |UCWA initialisiert  <br/> |Nicht zutreffend  <br/> Nicht zutreffend  <br/> |
|20002  <br/> |Fehler  <br/> |Unerwartete Ausnahme während der Initialisierung von UCWA  <br/> |Während der Initialisierung ist ein unerwarteter Fehler aufgetreten.  <br/> Überprüfen Sie die Ausnahmedetails im zugehörigen Ereignisprotokolleintrag, um die mögliche Ursache zu ermitteln.  <br/> |
|20003  <br/> |Fehler  <br/> |In der UCWA ist eine nicht behandelte Ausnahme aufgetreten.  <br/> |Eine nicht behandelte Ausnahme ist aufgetreten.  <br/> Starten Sie den Server neu. Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20004  <br/> |Fehler  <br/> |Kein Zugriff auf Exchange zum Abrufen des HD-Fotos  <br/> |Keine Verbindung mit Exchange verfügbar  <br/> Sicherstellen, dass eine Verbindung mit Exchange verfügbar ist  <br/> |
|20005  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler beim Zugriff auf Exchange zum Abrufen des HD-Fotos ausgeführt  <br/> |Nicht zutreffend  <br/> |
|20006  <br/> |Fehler  <br/> |Kein Zugriff auf Exchange zum Suchen von Kontakten  <br/> |Keine Verbindung mit Exchange verfügbar  <br/> Sicherstellen, dass eine Verbindung mit Exchange verfügbar ist  <br/> |
|20007  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler beim Suchen von Kontakten in Exchange ausgeführt  <br/> |Nicht zutreffend  <br/> |
|20008  <br/> |Warnung  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Anwendung als zulässig abzuschließen  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Anwendung als zulässig abzuschließen  <br/> Clients auf unnötige Abonnements überprüfen  <br/> |
|20009  <br/> |Warnung  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Batch als zulässig abzuschließen  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Batch als zulässig abzuschließen  <br/> Clients auf unnötige Abonnements überprüfen  <br/> |
|20010  <br/> |Fehler  <br/> |In-Band-Daten können nicht abgerufen werden  <br/> |In-Band-Daten können nicht abgerufen werden  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20011  <br/> |Fehler  <br/> |Anwesenheit kann nicht abonniert werden  <br/> |Anwesenheit kann nicht abonniert werden  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20012  <br/> |Fehler  <br/> |Fehler beim Registrieren des Endpunkts  <br/> |Fehler beim Registrieren des Endpunkts  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20013  <br/> |Fehler  <br/> |IM MCU ist nicht verfügbar.  <br/> |IM MCU ist nicht verfügbar.  <br/> Prüfen, ob IM MCU ausgeführt wird.  <br/> |
|20014  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit IM MCU ausgeführt  <br/> |Nicht zutreffend  <br/> |
|20015  <br/> |Fehler  <br/> |AV MCU ist nicht verfügbar.  <br/> |AV MCU ist nicht verfügbar.  <br/> Prüfen, ob AV MCU ausgeführt wird.  <br/> |
|20016  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit AV MCU ausgeführt  <br/> |Nicht zutreffend  <br/> |
|20017  <br/> |Fehler  <br/> |AS MCU ist nicht verfügbar.  <br/> |AS MCU ist nicht verfügbar.  <br/> Prüfen, ob AS MCU ausgeführt wird.  <br/> |
|20018  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit AS MCU ausgeführt  <br/> |-  <br/> |
|20019  <br/> |Fehler  <br/> |Data MCU ist nicht verfügbar.  <br/> |Data MCU ist nicht verfügbar.  <br/> Prüfen, ob Data MCU ausgeführt wird.  <br/> |
|20020  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit Date MCU ausgeführt  <br/> |Nicht zutreffend  <br/> |
|20021  <br/> |Fehler  <br/> |Teilnahme an IM MCU nicht möglich  <br/> |Teilnahme an IM MCU nicht möglich  <br/> Prüfen, ob IM MCU ausgeführt wird.  <br/> |
|20022  <br/> |Fehler  <br/> |Teilnahme an AV MCU nicht möglich  <br/> |Teilnahme an AV MCU nicht möglich  <br/> Prüfen, ob AV MCU ausgeführt wird.  <br/> |
|20023  <br/> |Fehler  <br/> |Teilnahme an AS MCU nicht möglich  <br/> |Teilnahme an AS MCU nicht möglich  <br/> Prüfen, ob AS MCU ausgeführt wird.  <br/> |
|20024  <br/> |Fehler  <br/> |Teilnahme an Data MCU nicht möglich  <br/> |Teilnahme an Data MCU nicht möglich  <br/> Prüfen, ob Data MCU ausgeführt wird.  <br/> |
|20025  <br/> |Fehler  <br/> |Kein Zugriff auf Active Directory zum Abrufen des Fotos  <br/> |Die Verbindung mit Active Directory ist nicht verfügbar.  <br/> Stellen Sie sicher, dass die Verbindung mit Active Directory verfügbar ist.  <br/> |
|20026  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler beim Zugriff auf Active Directory zum Abrufen des Fotos ausgeführt  <br/> |-  <br/> |
|20027  <br/> |Warnung  <br/> |Deserialisierung nicht möglich  <br/> |Deserialisierung nicht möglich  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
   

