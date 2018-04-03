---
title: Planen der Verwaltung von Skype Room System V2 mit OMS
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 2/13/2018
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 9fd16866-27eb-47a9-b335-2f6bc9044a80
description: " In diesem Artikel werden Planungsüberlegungen für die Verwendung von Operations Management Suite zur Verwaltung von Skype Room System V2-Geräten in Ihrer Skype for Business Server 2015-Implementierung beschrieben."
ms.openlocfilehash: e6409370da3597623526379581081e617f48dd81
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="plan-skype-room-systems-v2-management-with-oms"></a>Planen der Verwaltung von Skype Room System V2 mit OMS
 
  In diesem Artikel werden Planungsüberlegungen für die Verwendung von Operations Management Suite zur Verwaltung von Skype Room System V2-Geräten in Ihrer Skype for Business Server 2015-Implementierung beschrieben.
  
[Vorgänge Management Suite](https://docs.microsoft.com/en-us/azure/operations-management-suite/operations-management-suite-overview) (OMS) ist eine Auflistung von Rights Management Services, die in der Cloud ab dem Anfang entwickelt wurden. Statt bereitstellen und Verwalten von lokalen Ressourcen, werden OMS-Komponenten vollständig in Azure gehostet. Konfiguration ist gering, und Sie können ausgeführt werden und als solches innerhalb weniger Minuten. Einige Arbeit Anpassung können sie bei der Verwaltung von Skype Raum v2 Conferencing-basierte Systeme durch Bereitstellen der Systemintegrität oder Fehler in Echtzeit Benachrichtigungen für einzelne Raum Systeme hilfreich, und es kann potenziell vertikales Skalieren zur Verwaltung von Tausende von Skype Raum Systemen Konferenzräume v2.
  
Dieser Artikel enthält eine Erörterung der Anforderungen, Design-Architektur und Implementierung bewährte Methoden für die Implementierung von OMS-Verwaltung von Skype Raum Systemen v2 Konferenz Geräte und bietet Links zu ausführlichen Artikeln zur Implementierung von OMS Verwaltung für Skype Raum Systemen v2 und kritische Referenzinformationen zur kontinuierlichen Verwaltung OMS Skype Raum Systemen v2 Chatrooms. 
  
## <a name="functional-overview"></a>Funktionsübersicht

![Diagramm der SRS-Verwaltung mit OMS](../../media/3f2ae1b8-61ea-4cd6-afb4-4bd75ccc746a.png)
  
Die Skype Raum Systemen v2 app auf dem Gerät Konsole schreibt Ereignisse in der Windows-Ereignisprotokoll. Wenn ein OMS-Agent installiert wurde, übergibt dieser die Informationen an OMS. 
  
Einmal ordnungsgemäß konfiguriert, OMS analysiert die JSON-Nutzlast eingebettet in den Ereignisdetails Beschreibungen der wird beschrieben, wie jedes Skype Raum Systemen v2 System funktioniert und welche Fehler erkannt werden. 
  
Ein Administrator mit OMS sind finde Benachrichtigungen über Skype Raum v2-basierte Systeme, die offline sind oder app, Diensten oder Hardwarefehler auftritt als auch feststellen, ob ein System muss neu gestartet werden. Jede Systemstatus wird alle fünf Minuten aktualisiert, damit diese Benachrichtigungen nahezu in Echtzeit Updates sind.
  
## <a name="oms-requirements"></a>Anforderungen für OMS

Sie benötigen ein gültiges Abonnement für OMS, um diese Funktion zu verwenden. Finden Sie unter [Erste Schritte mit einem Protokoll Analytics Arbeitsbereich](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-get-started?toc=%2fazure%2foperations-management-suite%2ftoc.json) , um ein Abonnement für Ihre Organisation zu erstellen.
  
Machen Sie sich nach Bedarf mit der Verwendung des OMS-Ansicht-Designers vertraut. Diese Details finden Sie unter [Ansichten in Operations Management Suite (OMS) Management-Lösungen](https://docs.microsoft.com/en-us/azure/operations-management-suite/operations-management-suite-solutions-resources-views) .
  
### <a name="related-tasks"></a>Verwandte Aufgaben

1. Nachdem OMS abonniert haben, erstellen Sie benutzerdefinierte Felder (siehe [Zuordnen von benutzerdefinierten Feldern](../../deploy/deploy-clients/with-oms.md#Custom_fields)) erforderlich, um die Informationen zu analysieren, die von Skype Raum Systemen v2 Konsolen gesendet werden soll. Dazu gehören Grundlegendes zum Schema der JSON in [die Protokolleinträge verstehen](../../manage/skype-room-systems-v2/oms.md#Telemetry)dokumentiert.
    
2. Entwickeln eine Skype Raum Systemen v2 Management-Ansicht in OMS (finden Sie unter [Definieren der SRS v2-Ansichten in OMS](../../deploy/deploy-clients/with-oms.md#Views)) verwenden Sie die zuvor genannten Ansichts-Designer.
    
## <a name="individual-skype-room-systems-v2-console-requirements"></a>Einzelne Skype Raum Systemen v2 Konsole Anforderungen

Jede Skype Raum Systemen v2-Konsole ist eine app auf einem Gerät Fläche 4 im Kioskmodus ausgeführt (normalerweise konfiguriert ist die einzige app handeln, die auf dem Gerät ausgeführt werden können). Wie bei jeder Windows-app schreibt die Skype Raum Systemen v2 app Ereignisse wie beim Starten und Hardware Fehlern im Windows-Ereignisprotokoll. Hinzufügen eines OMS-Agents auf dem Gerät des Skype Raum Systemen v2 ermöglicht diese Ereignisse vom OMS erfasst werden sollen. (Einzelheiten finden Sie unter [mit dem Protokoll Analytics-Dienst in Azure-Computern mit Windows verbinden](https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-windows-agents) .)
  
## <a name="ongoing-management"></a>Laufende Verwaltung

Bei Verwendung von OMS Skype Raum Systemen v2 Konferenz Geräte verwalten, müssen Sie verstehen, die Informationen in den Ereignisprotokollen von OMS verwendet. Finden Sie auf diese Nachrichten Health Einzelheiten in [die Protokolleinträge verstehen](../../manage/skype-room-systems-v2/oms.md#Telemetry) .
  
### <a name="related-tasks"></a>Verwandte Aufgaben

- Verstehen von Skype Raum Systemen v2 und zu deren Behebung (finden Sie im Abschnitt [zu verstehen der Protokolleinträge](../../manage/skype-room-systems-v2/oms.md#Telemetry)) generierte Benachrichtigungen
    
## <a name="see-also"></a>Siehe auch

#### 

[Bereitstellen von Skype Raum v2 systemverwaltung mit OMS](../../deploy/deploy-clients/with-oms.md)
  
[Verwalten von Skype Raum Systemen v2 Geräte mit OMS](../../manage/skype-room-systems-v2/oms.md)
