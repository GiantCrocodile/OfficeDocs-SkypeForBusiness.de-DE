---
title: Überwachen der Speicherkapazitätslimits des Servers in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 1/31/2018
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 1697ea71-6fcf-480d-b4e9-cd79f94d247e
description: 'Zusammenfassung: Informationen Sie zum Überwachen von Server-Speicher-Kapazitätsgrenzen in Skype für Business Server 2015.'
ms.openlocfilehash: df05cdf43a7f09f49760f9671c900d6a9ea992b1
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="monitor-for-server-memory-capacity-limits-in-skype-for-business-server-2015"></a>Überwachen der Speicherkapazitätslimits des Servers in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zum Überwachen von Server-Speicher-Kapazitätsgrenzen in Skype für Business Server 2015.
  
> [!CAUTION]
> Die Informationen in diesem Thema, das auf Capacity Planning verweist bezieht sich nur auf Lync 2010 Mobile-Clients und den Mobilitätsdienst ("MCX"). Kapazitätsplanung für die Unified Communications Web API (UCWA), durch die Lync 2013-Mobile-Clients verwendet, wird von Lync Server 2013, Planungstool bereitgestellt. 
  
Zwei Leistungsindikatoren für Mobilität können Sie zum Bestimmen der Nutzung von aktuellen und unterstützt Sie beim Planen der Kapazität für die Skype für Business Server 2015 Mobility Service ("MCX") als auch um Speicherverwendung UCWA überwachen. Für UCWA ist der Leistungsindikatorkategorie **LS:WEB - UCWA**. Leistungsindikatoren sind für den Mobilitätsdienst ("MCX") unter der Kategorie **LS:WEB - Mobile-Kommunikationsdienst**. Die zu überwachende Leistungsindikatoren sind:
  
- **Anzahl der derzeit aktiven Sitzungen mit aktiven Anwesenheitsabonnements**: Dies ist die aktuelle Anzahl von Endpunkten, die über die UCWA oder den Mobilitätsdienst (Mcx) registriert wurden und aktive Anwesenheitsabonnements besitzen (Anzahl der immer verbundenen mobilen Benutzer).
    
- **Anzahl der derzeit aktiven Sitzungen**: Dies ist die aktuelle Anzahl von Endpunkten, die über UCWA oder den Mobilitätsdienst registriert wurden.
    
Wenn der Unterschied zwischen **Anzahl der derzeit aktiven Sitzungen mit aktiven Anwesenheitsabonnements** und **Anzahl der derzeit aktiven Sitzungen** im Laufe der Zeit gering ist, bedeutet dies, dass die meisten Benutzer ein Mobilgerät verwenden, dass immer verbunden ist, beispielsweise ein Android- oder Nokia-Mobilgerät (nur für Mcx). UCWA immer verbundenen Geräten zählen Apple und Android-Geräte, die mit Lync 2013-Mobile-Clients). Wenn die **Anzahl der derzeit aktiven Sitzungen** sehr viel höher ist als die **Anzahl der derzeit aktiven Sitzungen mit aktiven Anwesenheitsabonnements**, weist dies darauf hin, dass mehr Benutzer ein Hintergrund-Endpunktgerät unter Mcx verwenden, z. B. ein Apple iOS-Gerät oder ein Windows Phone. (Windows Phone ist der einzige Lync 2013-Mobile-Client, der registriert werden, als dies).
  
Sie sollten einen Grenzwert für die Leistungsindikatoren **Anzahl derzeit aktiver Sitzungen mit aktiven Anwesenheitsabonnements** und **Anzahl derzeit aktiver Sitzungen** basierend auf Ihre erwartete Verwendung Capacity planning Ergebnisse und eine fortlaufende Überwachung festlegen. Mobilitätsdienst und anderen Front-End-Server-Leistungsindikatoren. Die festgelegten Beschränkungen sollten das Auswerten der Serverkapazität und das Auslösen von Warnungen bei einer Kapazitätsüberschreitung erlauben.
  
Um die Grenzwerte für die entsprechenden ermitteln möchten, müssen Sie zuerst bestimmen, wie viel Arbeitsspeicher auf dem Front-End-Server für den Mobilitätsdienst verfügbar ist. Überwachen Sie die Leistungsindikatoren, um anhand der folgenden Formel festzustellen, ob zusätzliche Kapazität eingeplant werden muss:
  
Durch die Mcx Mobility Service (MB) verwendeter Arbeitsspeicher insgesamt = 164 + (400 + 134) / 1024 * **Anzahl derzeit aktiver Sitzungen mit aktiven Anwesenheitsabonnements** + 400 / 1024 * ( **Anzahl derzeit aktiver Sitzungen** - **derzeit aktiven Sitzung mit zählen Aktive Anwesenheitsabonnements**)
  
> [!IMPORTANT]
> Kapazitätsrechner für Microsoft Lync Server 2010 ist eine Tabelle, die mit alle Formeln vorausgefüllt ist, mit denen eine Planner, um zu bestimmen, welche die Anforderungen für die Skype für Business Server, einschließlich CPU, Arbeitsspeicher und Festplatte sein soll. Sie können [die Kalkulationstabelle und eines zugeordneten Dokuments herunterladen](https://go.microsoft.com/fwlink/p/?LinkID=212657). 
  
Der Front-End-Server benötigt genügend Arbeitsspeicher, um den Mobilitätsdienst in Situationen Failover zu unterstützen. Sie können den aktuellen verfügbaren Speicher auf dem Front-End-Server mit den **Leistungsindikator Memory\Available** MBytes oder unter Verwendung der Gleichung für den Speicher planen, dass Sie den Mobilitätsdienst verwenden erwarten weiter oben erwähnten überwachen.
  
Wenn die Menge des Arbeitsspeichers zur Verfügung, auf dem Front-End-Server niedriger als 1.500 MB, ist bei der Planung für die erwartete Anzahl von Benutzern für Mobilität, müssen Sie mehr Hardware zur Unterstützung der Mobilitätsdienst hinzufügen. Weitere Informationen finden Sie unter [Monitor Mobilität für die Leistung in Skype für Business Server 2015](monitor-mobility-performance.md) in der Betriebsdokumentation.
  
## <a name="see-also"></a>Siehe auch

#### 

[Überwachen der Leistung in Skype für Business Server 2015 Mobilität](monitor-mobility-performance.md)
