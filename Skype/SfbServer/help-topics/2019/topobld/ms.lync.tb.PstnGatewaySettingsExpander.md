---
title: PSTN-Gatewayeinstellungen – Erweiterung
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 3/26/2015
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.tb.PstnGatewaySettingsExpander
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 0fd103df-150d-4ea8-b522-18dbc50f5061
description: 'Ändern Sie die folgenden Felder, um die Einstellungen für ein PSTN-Gateway (Public Switched Telephone Network) zu bearbeiten oder zu ändern:'
ms.openlocfilehash: b13580053783ae6b6934fa40e93b493280fd6d3c
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="pstn-gateway-settings-expander"></a>PSTN-Gatewayeinstellungen – Erweiterung
 
Ändern Sie die folgenden Felder, um die Einstellungen für ein PSTN-Gateway (Public Switched Telephone Network) zu bearbeiten oder zu ändern:
  
Der FQDN oder die IP-Adresse des Gateways ist ein erforderlicher Eintrag, der festlegt, ob der vollqualifizierte Domänenname (FQDN)**** des PSTN-Gateways über einen DNS-A-Eintrag (Host), einen statischen HOSTS-Dateieintrag oder die IP-Adresse des PSTN-Gateways definiert ist.
  
Beim SIP-Transportprotokoll kann es sich um das Transmission Control Protocol (TCP) oder Transport Layer Security (TLS) handeln. Als Standardeinstellung ist TLS festgelegt. In der Dokumentation des Gatewayherstellers finden Sie die von Ihrem Gateway unterstützten Protokolle. Als Standardeinstellung ist TLS festgelegt, und wenn das Gateway TLS unterstützt, ist dies die Option mit höherer Sicherheit.
  
Wählen Sie aus, ob für das Gateway IPv4 und IPv6 aktiviert werden soll.
  
Die **alternative IP-Adresse für Medien** ist eine Definition für den Vermittlungsserver für den bereitgestellte PSTN-Gateway eine andere IP-Adresse für Mediendatenverkehr als die standardmäßig konfigurierten IP-Adresse verfügt, die in der Regel für SIP-Datenverkehr vorgesehen ist. Wenn Sie diesen Parameter definieren, unterstützt das PSTN-Gateway eine unterschiedliche unterstützt einen anderen Netzwerkschnittstelle oder den Pfad für Medien. Wenn diese Adresse leer ist, wird das PSTN-Gateway nicht alternativen Pfad für Medien unterstützt.
  
