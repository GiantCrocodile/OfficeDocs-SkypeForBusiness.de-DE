---
title: Plan für Enterprise-VoIP in Skype for Business Server 2015
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.date: 8/18/2015
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Admin
ms.assetid: fd8d5867-0ac9-47f8-94f0-1c3ee5e25575
description: Enterprise-VoIP Grundlagen in Skype für Business Server planen, einschließlich Websites, Regionen, Netzwerkverbindungen zwischen Standorten und Nutzung Sprachdatenverkehr schätzen.
ms.openlocfilehash: a04c379e3a616a511306db62fd908af26e325418
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="plan-for-enterprise-voice-in-skype-for-business-server-2015"></a>Plan für Enterprise-VoIP in Skype for Business Server 2015
 
Enterprise-VoIP Grundlagen in Skype für Business Server planen, einschließlich Websites, Regionen, Netzwerkverbindungen zwischen Standorten und Nutzung Sprachdatenverkehr schätzen.
  
Der Bereitstellungsprozess für Enterprise-VoIP hängt von Ihrer vorhandenen Topologie, Infrastruktur und die Enterprise-VoIP-Funktionen, die Sie unterstützen möchten. Die erforderlichen Verfahren hängen von den von Ihnen ausgewählten Funktionen ab, aber Sie müssen weitere allgemeine Planungsentscheidungen treffen.
  
Überlegen Sie der Typ und Anzahl der Websites, die Sie bereitstellen möchten und deren geografischen Standorten, das Anrufvolumen an den einzelnen Standorten, die Arten von Netzwerkverbindungen, mit die Standorten zugänglich im Allgemeinen, ob Sie Redundanz und Failover für VoIP-Funktionen für die einzelnen bereitstellen möchten Website, und ob Sie vorhandene PBX-Geräte verwenden möchten. Es gibt bestimmte Aspekte wie hohe Verfügbarkeit, den Sie bei der Planung von Skype für Business Server als Ganzes berücksichtigen sollten. In den Themen in diesem Abschnitt werden diese Aspekte erläutert, wie gewünscht.
  
## <a name="sites-and-regions"></a>Standorte und Regionen

Identifizieren Sie zunächst die Websites in Ihrer Topologie, in dem Sie Enterprise-VoIP und die netzwerkregionen, zu denen diese Websites gehören, bereitgestellt wird. Insbesondere müssen Sie überlegen, wie die PSTN-Anbindung (Public Switched Telephone Network) für jeden Standort implementiert wird. Die Zuweisung von Standorten zu Regionen kann aus verwaltungstechnischer und logistischer Sicht ein entscheidender Faktor sein. Entscheiden Sie, dem die Gateways lokal bereitgestellt wird, dem Survivable Branch Appliances (SBAs) bereitgestellt wird und wo Sie SIP-Trunks (lokal oder am zentralen Standort) zu einem Internet Telephony Service Provider (ITSP) konfigurieren können.
  
## <a name="network-links-between-sites"></a>Netzwerkverbindungen zwischen Standorten

Sie müssen auch die Auslastung der Bandbreite berücksichtigen, die Sie auf der Netzwerkverbindungen zwischen Ihrem zentralen Standort und seine Zweigniederlassungen erwarten. Wenn Sie haben oder Planen der Bereitstellung ausfallsicher WAN-Verbindungen zwischen Standorten, wird empfohlen, ein Gateway an jedem Zweigstellenstandort Bereitstellen der lokalen direct inward Dialing-()-Beendigung für Benutzer an diesen Standorten bereitzustellen. Wenn Sie über ausfallsichere WAN-Verbindungen verfügen, aber die Bandbreite einer WAN-Verbindung wahrscheinlich eingeschränkt ist, konfigurieren Sie die Anrufsteuerung für diese Verbindung. Wenn Sie keine ausfallsichere WAN-Verbindungen haben, als host von weniger als 1000 Benutzern am Zweigstellenstandort, und haben keinen lokalen geschult Skype für Business Server-Administratoren sind verfügbar, es wird empfohlen, dass Sie eine Survivable Branch Appliance am Zweigstellenstandort bereitstellen. Wenn Sie zwischen 1000 und 5000 Benutzern am Zweigstellenstandort hosten, keine ausfallsichere WAN-Verbindung und geschulte Skype für Business Server-Administratoren sind verfügbar, es wird empfohlen, dass Sie einen Survivable Branch Server mit einem kleinen Gateway am Zweigstellenstandort bereitstellen. Erwägen Sie auch die Aktivierung der Medienumgehung für Verbindungen mit eingeschränkter Bandbreite, wenn Sie über ein Gatewaypeer mit Unterstützung der Medienumgehung verfügen.
  
## <a name="estimating-voice-usage-and-traffic"></a>Schätzen von VoIP-Nutzung und -Datenverkehr

Die Microsoft Lync Server 2013, Planungstool verwendet die folgenden Metriken zur Schätzung des Benutzerdatenverkehrs an jedem Standort und die Anzahl der Ports, die zur Unterstützung dieser Datenverkehr erforderlich sind.
  
> Für **geringes Datenverkehrsaufkommen** (ein Festnetzanruf pro Benutzer und Stunde) gehen Sie von 15 Benutzern pro Anschluss aus.
    
> Für **mittleres Datenverkehrsaufkommen** (zwei Festnetzanrufe pro Benutzer und Stunde) gehen Sie von 10 Benutzern pro Anschluss aus.
    
> Für **hohes Datenverkehrsaufkommen** (drei oder mehr Festnetzanrufe pro Benutzer und Stunde) gehen Sie von 5 Benutzern pro Anschluss aus.
    
Die Anzahl von Ports bestimmt wiederum die Anzahl der Vermittlungsserver und Gateways, die ausgeführt werden müssen. Die Gateways public switched Telephone Network, (PSTN), dass die meisten Organisationen erwägen, Bereich Größe 2 Ports bis 960 Ports. (Es gibt sogar größere Gateways, aber diese werden hauptsächlich von Telefoniedienstanbieter verwendet.)
  
Eine Organisation mit 10.000 Benutzern und mittlerem Datenverkehrsaufkommen würde z. B. 1000 Ports benötigen. Die Anzahl der erforderlichen Gateways entspricht der Gesamtzahl der erforderlichen Ports, die durch die Gesamtkapazität der Gateways bestimmt ist.
  
## <a name="components-features-and-options-of-enterprise-voice"></a>Komponenten, Features und Optionen von Enterprise-VoIP

Finden Sie in den folgenden Abschnitten für Weitere Informationen zur Planung der bereitstellungs von Enterprise-VoIP.
  
- [Für Enterprise-VoIP in Skype für Business Server 2015 erforderliche Komponenten](components-required-for-enterprise-voice.md)
    
- [Planen von PSTN-Konnektivität in Skype for Business Server 2015](pstn-connectivity-0.md)
    
- [Netzwerkeinstellungen für den erweiterten Enterprise-VoIP-Funktionen in Skype für Business Server 2015](network-settings-for-advanced-features.md)
    
- [Planen für die anrufsteuerung in Skype Business Server 2015](call-admission-control.md)
    
- [Planen für Notdienste in Skype Business Server 2015](emergency-services.md)
    
- [Planen Sie für die medienumgehung in Skype für Business 2015](media-bypass.md)
    
- [Planen von privaten Telefonleitungen mit Skype für Business 2015](private-telephone-lines.md)
    
- [Plan für die Standortbasierte Weiterleitung in Skype für Business 2015](location-based-routing.md)
    
- [Planen der anrufverwaltungsfunktionen in Skype für Business 2015](call-management-features.md)
    
- [Planen Sie für Enterprise Voice Resiliency in Skype für Business Server 2015](enterprise-voice-resiliency.md)
    
