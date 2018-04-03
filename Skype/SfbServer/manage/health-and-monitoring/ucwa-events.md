---
title: UCWA-Ereignisse in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
description: 'Zusammenfassung: Informationen Sie zu den Unified Communications-Web-API (UCWA) in Skype für Business Server 2015.'
ms.openlocfilehash: cc9b62a4d00e9c4ed4feadfbfecfa4e3f8ca79fa
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="ucwa-events-in-skype-for-business-server-2015"></a>UCWA-Ereignisse in Skype for Business Server 2015
 
**Zusammenfassung:** Erfahren Sie mehr über die Unified Communications-Web-API (UCWA) in Skype für Business Server 2015.
  
Skype für Business Server 2015 verwendet die Unified Communications Web API (UCWA) für eine Reihe von Zwecke, den Zugriff auf Microsoft Exchange für die Kontaktsuche zur Aktualisierung von Anwesenheitsinformationen für mobile Clients.
  
UCWA zeichnet Einträge zum Betriebsverhalten als die Ereignistypen „Information“, „Warnung“ und „Fehler“ auf. In der folgenden Tabelle sind die Ereignisse beschrieben, die von den UCWA-Komponenten geschrieben werden können.
  
|**Ereignis-ID**|**Ereignistyp**|**Zusammenfassung**|**Ursache und Lösung**|
|:-----|:-----|:-----|:-----|
|20001  <br/> |Information  <br/> |UCWA initialisiert  <br/> |-  <br/> -  <br/> |
|20002  <br/> |Fehler  <br/> |Unerwartete Ausnahme während der Initialisierung von UCWA  <br/> |Während der Initialisierung ist ein unerwarteter Fehler aufgetreten.  <br/> Überprüfen Sie die Ausnahmedetails im zugehörigen Ereignisprotokolleintrag, um die mögliche Ursache zu ermitteln.  <br/> |
|20003  <br/> |Fehler  <br/> |In der UCWA ist eine nicht behandelte Ausnahme aufgetreten.  <br/> |Eine nicht behandelte Ausnahme ist aufgetreten.  <br/> Starten Sie den Server neu. Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20004  <br/> |Fehler  <br/> |Kein Zugriff auf Exchange zum Abrufen des HD-Fotos  <br/> |Keine Verbindung mit Exchange verfügbar  <br/> Sicherstellen, dass eine Verbindung mit Exchange verfügbar ist  <br/> |
|20005  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler beim Zugriff auf Exchange zum Abrufen des HD-Fotos ausgeführt  <br/> |-  <br/> |
|20006  <br/> |Fehler  <br/> |Kein Zugriff auf Exchange zum Suchen von Kontakten  <br/> |Keine Verbindung mit Exchange verfügbar  <br/> Sicherstellen, dass eine Verbindung mit Exchange verfügbar ist  <br/> |
|Kategorie "20007"  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler beim Suchen von Kontakten in Exchange ausgeführt  <br/> |-  <br/> |
|20008  <br/> |Warnung  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Anwendung als zulässig abzuschließen  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Anwendung als zulässig abzuschließen  <br/> Clients auf unnötige Abonnements überprüfen  <br/> |
|20009  <br/> |Warnung  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Batch als zulässig abzuschließen  <br/> |Versuchen, mehr Anwesenheitsabonnements pro Batch als zulässig abzuschließen  <br/> Clients auf unnötige Abonnements überprüfen  <br/> |
|20010  <br/> |Fehler  <br/> |In-Band-Daten können nicht abgerufen werden  <br/> |In-Band-Daten können nicht abgerufen werden  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20011  <br/> |Fehler  <br/> |Anwesenheit kann nicht abonniert werden  <br/> |Anwesenheit kann nicht abonniert werden  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20012  <br/> |Fehler  <br/> |Fehler beim Registrieren des Endpunkts  <br/> |Fehler beim Registrieren des Endpunkts  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
|20013  <br/> |Fehler  <br/> |IM MCU ist nicht verfügbar.  <br/> |IM MCU ist nicht verfügbar.  <br/> Prüfen, ob IM MCU ausgeführt wird.  <br/> |
|20014  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit IM MCU ausgeführt  <br/> |-  <br/> |
|20015  <br/> |Fehler  <br/> |AV MCU ist nicht verfügbar.  <br/> |AV MCU ist nicht verfügbar.  <br/> Prüfen, ob AV MCU ausgeführt wird.  <br/> |
|20016  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit AV MCU ausgeführt  <br/> |-  <br/> |
|20017  <br/> |Fehler  <br/> |AS MCU ist nicht verfügbar.  <br/> |AS MCU ist nicht verfügbar.  <br/> Prüfen, ob AS MCU ausgeführt wird.  <br/> |
|20018  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit AS MCU ausgeführt  <br/> |-  <br/> |
|20019  <br/> |Fehler  <br/> |Data MCU ist nicht verfügbar.  <br/> |Data MCU ist nicht verfügbar.  <br/> Prüfen, ob Data MCU ausgeführt wird.  <br/> |
|20020  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit Date MCU ausgeführt  <br/> |-  <br/> |
|20021  <br/> |Fehler  <br/> |Teilnahme an IM MCU nicht möglich  <br/> |Teilnahme an IM MCU nicht möglich  <br/> Prüfen, ob IM MCU ausgeführt wird.  <br/> |
|20022  <br/> |Fehler  <br/> |Teilnahme an AV MCU nicht möglich  <br/> |Teilnahme an AV MCU nicht möglich  <br/> Prüfen, ob AV MCU ausgeführt wird.  <br/> |
|20023  <br/> |Fehler  <br/> |Teilnahme an AS MCU nicht möglich  <br/> |Teilnahme an AS MCU nicht möglich  <br/> Prüfen, ob AS MCU ausgeführt wird.  <br/> |
|20024  <br/> |Fehler  <br/> |Teilnahme an Data MCU nicht möglich  <br/> |Teilnahme an Data MCU nicht möglich  <br/> Prüfen, ob Data MCU ausgeführt wird.  <br/> |
|20025  <br/> |Fehler  <br/> |Kein Zugriff auf Active Directory zum Abrufen des Fotos  <br/> |Die Verbindung mit Active Directory ist nicht verfügbar.  <br/> Stellen Sie sicher, dass die Verbindung mit Active Directory verfügbar ist.  <br/> |
|20026  <br/> |Information  <br/> |Wiederherstellung nach dem Fehler beim Zugriff auf Active Directory zum Abrufen des Fotos ausgeführt  <br/> |-  <br/> |
|20027  <br/> |Warnung  <br/> |Deserialisierung nicht möglich  <br/> |Deserialisierung nicht möglich  <br/> Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.  <br/> |
   
