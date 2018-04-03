---
title: Edgeserver-Szenarien in Skype for Business Server 2015
ms.author: heidip
author: microsoftheidi
ms.date: 8/18/2015
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Hybrid
ms.assetid: 7b9c211b-deb0-479d-b184-973f08b96d07
description: 'Zusammenfassung: Lesen Sie diese Szenarien, die Ihnen bei der Planung Ihrer Edge-Server-Topologie in Skype für Business Server 2015 erleichtern.'
ms.openlocfilehash: 30bce96e1764a608bf7bc8daeec3d918b9e5912c
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="edge-server-scenarios-in-skype-for-business-server-2015"></a>Edgeserver-Szenarien in Skype for Business Server 2015
 
**Zusammenfassung:** Lesen Sie diese Szenarien, die Ihnen bei der Planung Ihrer Edge-Server-Topologie in Skype für Business Server 2015 erleichtern.
  
Wir haben einige Szenarien Diagramme zur Unterstützung beim visualisieren und entscheiden, auf welche Skype für Business Server Edge-Server-Topologie, die Sie implementieren möchten. Sobald Sie einen geeigneten Kandidaten ausgewählt haben, können Sie sich über die Umgebungsanforderungen informieren, die Sie erfüllen müssen. Da das Folgende auf alle Szenarien zutrifft, erwähnen wir es zuerst.
  
Diese Abbildungen, die nur zu Beispielzwecken verwendet werden (und als solche Beispiel-IPv4- und Beispiel-IPv6-Daten enthalten), stellen nicht den tatsächlichen Kommunikationsfluss dar, sondern eher eine allgemeine Darstellung Ihres möglichen Datenverkehrs. Portdetails können auch in den untenstehenden Portdiagrammen für jedes Szenario gefunden werden.
  
In den Diagrammen wird .com für die externe Schnittstelle und .net für die interne angezeigt, welche auch Beispielmaterial ist; natürlich können Ihre eigenen Einträge vollkommen anders sein, wenn Sie Ihren eigenen endgültigen Edgeplan zusammenstellen.
  
Wir nicht mit den Director (bei dem es sich um eine optionale Komponente handelt) in den Diagrammen einschließen, aber Sie erhalten Informationen über, die separat (es wird in anderen Themen Planning erwähnten).
  
Wie bereits erwähnt, sind Beispiel-IPv6-Daten im Diagramm enthalten. Die meisten der in der Dokumentation in [Planen der Edge-Server-Bereitstellungen in Skype für Business Server 2015](edge-server-deployments.md) IPv4 bezeichnen, aber Sie werden sicherlich unterstützt, wenn Sie IPv6 verwenden möchten. Beachten Sie, dass Sie IPv6-Adressen in Ihrem zugewiesenen Adressraum benötigen und dass diese wie mit IPv4-IPs mit interner und externer Adressierung funktionieren müssen. Dank Windows können Sie die Dualstapelfunktion verwenden, die ein separater und unabhängiger Netzwerkstapel für IPv4 und IPv6 ist. Dadurch können Sie bei Bedarf gleichzeitig IPv4- und IPv6-Adressen zuweisen.
  
NAT-Geräte, die für NAT64 zulassen vorhanden sind (IPv6 IPv4) und NAT66 (IPv6 in IPv6)), und dies für die Verwendung mit Skype für Business Server gültig ist.
  
> [!IMPORTANT]
> Wenn Sie Anrufsteuerung (CAC) verwenden, müssen Sie IPv4 auf der internen Schnittstelle verwenden, damit diese funktionieren kann. 
  
## <a name="single-consolidated-skype-for-business-server-edge-server-with-private-ip-addresses-and-nat"></a>Einzelner konsolidierter Skype für Business Server-Edgeserver mit privaten IP-Adressen und Netzwerkadressenübersetzung

Bei diesem Szenario gibt es keine Option für hohe Verfügbarkeit. Das bedeutet, dass Sie weniger für Hardware ausgeben und die Bereitstellung einfacher ist. Wenn hohe Verfügbarkeit für Sie ein Muss ist, informieren Sie sich unten über die skalierten konsolidierten Szenarien.
  
![Edgeszenario für einzelnen konsolidierten Edgeserver mit privater IP bei Verwendung von NAT](../../media/Plan_LyncServer_Edge_Scenario_SingleConsolidatedEdgePrivateIP.jpg)
  
### <a name="port-diagram"></a>Portdiagramm

Wir haben auch ein Diagramm für Ports für einzelne konsolidierte Edge-Server.
  
![Umkreisnetzwerk – Edgeszenario für einzelnen konsolidierten Edgeserver](../../media/Plan_LyncServer_Edge_NetPerimeter_SingleConsolidatedEdge.jpg)
  
## <a name="single-consolidated-skype-for-business-server-edge-server-with-public-ip-addresses"></a>Einzelner konsolidierter Skype für Business Server-Edgeserver mit öffentlichen IP-Adressen

Bei diesem Szenario gibt es keine Option für hohe Verfügbarkeit. Das bedeutet, dass Sie weniger für Hardware ausgeben und die Bereitstellung einfacher ist. Wenn hohe Verfügbarkeit für Sie ein Muss ist, informieren Sie sich unten über die skalierten konsolidierten Szenarien.
  
![Edgeszenario für einzelnen konsolidierten Edgeserver mit öffentlicher IP](../../media/Plan_LyncServer_Edge_Scenario_SingleConsolidatedEdgePublicIP.jpg)
  
### <a name="port-diagram"></a>Portdiagramm

Wir haben auch ein Diagramm für Ports für einzelne konsolidierte Edge-Server.
  
![Umkreisnetzwerk – Edgeszenario für einzelnen konsolidierten Edgeserver](../../media/Plan_LyncServer_Edge_NetPerimeter_SingleConsolidatedEdge.jpg)
  
## <a name="scaled-consolidated-skype-for-business-server-edge-pool-with-dns-load-balancing-and-private-ip-addresses-and-nat"></a>Skalierte konsolidierte Skype für Business Server Edge-Pool mit DNS laden, Lastenausgleich und privaten IP-Adressen und Netzwerkadressenübersetzung

Mit diesem Szenario können Sie über hohe Verfügbarkeit in Ihrer Edgebereitstellung verfügen, wodurch Sie die Vorteile von Skalierbarkeit und Failoverunterstützung genießen können.
  
![Edgeszenario für skalierten konsolidierten Edgeserver, DNS-LB mit privater IP bei Verwendung von NAT](../../media/Plan_LyncServer_Edge_Scenario_ScaledConsolidatedEdgeDNSLBPrivateIP.jpg)
  
### <a name="port-diagram"></a>Portdiagramm

Wir haben auch ein Diagramm für einen skalierten konsolidierten Edge-Pools mit DNS-Lastenausgleich.
  
![Umkreisnetzwerk – Edgeszenario für skalierten konsolidierten Edgeserver mithilfe von DNS-LB](../../media/Plan_LyncServer_Edge_NetPerimeter_ScaledConsolidatedEdgeDNSLB.jpg)
  
## <a name="scaled-consolidated-skype-for-business-server-edge-pool-with-dns-load-balancing-and-public-ip-addresses"></a>Skalierte konsolidierte Skype für Business Server Edge-Pool mit DNS load Lastenausgleich und öffentliche IP-Adressen

Mit diesem Szenario können Sie über hohe Verfügbarkeit in Ihrer Edgebereitstellung verfügen, wodurch Sie die Vorteile von Skalierbarkeit und Failoverunterstützung genießen können.
  
![Edgeszenario für skalierten konsolidierten Edgeserver, DNS-LB mit öffentlicher IP](../../media/Plan_LyncServer_Edge_Scenario_ScaledConsolidatedEdgeDNSLBPublicIP.jpg)
  
### <a name="port-diagram"></a>Portdiagramm

Wir haben auch ein Diagramm für einen skalierten konsolidierten Edge-Pools mit DNS-Lastenausgleich.
  
![Umkreisnetzwerk – Edgeszenario für skalierten konsolidierten Edgeserver mithilfe von DNS-LB](../../media/Plan_LyncServer_Edge_NetPerimeter_ScaledConsolidatedEdgeDNSLB.jpg)
  
## <a name="scaled-consolidated-skype-for-business-server-edge-pool-with-hardware-load-balancing"></a>Eine skalierte konsolidierte Skype für Business Server Edge-Pool mit Hardwaregerät zum Lastenausgleich

Mit diesem Szenario können Sie über hohe Verfügbarkeit in Ihrer Edgebereitstellung verfügen, wodurch Sie die Vorteile von Skalierbarkeit und Failoverunterstützung genießen können.
  
![Edgeszenario für skalierten konsolidierten Edgeserver mit HLB](../../media/Plan_LyncServer_Edge_Scenario_ScaledConsolidatedEdgeHLB.jpg)
  
### <a name="port-diagram"></a>Portdiagramm

Wir haben auch ein Diagramm für skalierte konsolidierte Edge-Pools mit Hardwaregerät zum Lastenausgleich
  
![Ports und Protokolle des Edgeserver-Umkreisnetzwerks](../../media/Plan_LyncServer_Edge_NetPerimeter_ScaledConsolidatedEdgeHLB.jpg)
  
