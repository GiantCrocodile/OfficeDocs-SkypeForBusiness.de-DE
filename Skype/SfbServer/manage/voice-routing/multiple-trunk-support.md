---
title: Mehrere trunk-Unterstützung in Skype for Business Server
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
description: Die Skype for Business Server-Funktionalität unterstützt mehrere Zuordnungen zwischen Gateways und Vermittlungsservern. Diese Zuordnungen werden durch Definieren eines Trunks erstellt, bei dem es sich um eine logische Zuordnung zwischen einem Vermittlungs Server Pool und einem PSTN-Gateway (Public Switched Telephone Network), Sitzungs Grenz Controller (SBC) oder IP-PBX handelt. Verwenden Sie den Topologie-Generator, um Gateways mit Vermittlungsservern (also Trunks) zu verknüpfen.
ms.openlocfilehash: 6f950f089d23687f0215bd9db1f253eb57c17c75
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41816945"
---
# <a name="multiple-trunk-support-in-skype-for-business-server"></a>Mehrere trunk-Unterstützung in Skype for Business Server

Die Skype for Business Server-Funktionalität unterstützt mehrere Zuordnungen zwischen Gateways und Vermittlungsservern. Diese Zuordnungen werden durch Definieren eines Trunks erstellt, bei dem es sich um eine logische Zuordnung zwischen einem Vermittlungs Server Pool und einem PSTN-Gateway (Public Switched Telephone Network), Sitzungs Grenz Controller (SBC) oder IP-PBX handelt. Verwenden Sie den Topologie-Generator, um Gateways mit Vermittlungsservern (also Trunks) zu verknüpfen.

- Um einen trunk in Skype for Business Server zuzuweisen oder zu entfernen, müssen Sie zuerst einen trunk in Topology Builder definieren. Ein trunk besteht aus der folgenden Zuordnung: vollständig qualifizierter Domänenname (Fully Qualified Domain Name, FQDN), Mediation Server-Abhör Port, Gateway-FQDN und Gateway-Abhör Port.
- Zum Konfigurieren mehrerer Trunks können Sie mehrere Zuordnungen zwischen dem gleichen Gateway und dem Vermittlungs Server erstellen. Dies bietet zusätzliche Widerstandsfähigkeit für die Enterprise-VoIP-Infrastruktur, die besonders in interoperational-Szenarien (Private Branch Exchange) verwendet werden kann. 

Beim Definieren eines Trunks muss er einer Route zugeordnet werden. Um einen trunk einer Route zuzuordnen, definieren Sie einen einfachen Namen für den trunk im Topologie-Generator. Dieser einfache Name wird als trunk-Name in der Skype for Business Server-Systemsteuerung verwendet, in der Trunks mit Routen verknüpft werden können. Der einfache trunk-Name wird als Gateway-Name aus der Skype for Business Server-Verwaltungsshell verwendet.

`New-CsVoiceRoute -Identity <RouteId> -NumberPattern <String> -PstnUsages @{add="<UsageString>"} -PstnGatewayList @{add="<TrunkSimpleName>"}`

Der Administrator muss einen Standard trunk auswählen, der einem Vermittlungs Server zugeordnet ist. Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den zugehörigen Vermittlungs Server, und klicken Sie dann auf **Eigenschaften**. Geben Sie das Standardgateway für den Vermittlungs Server an. 

Das folgende Diagramm zeigt die verschiedenen Trunks, die für jeden Vermittlungs Server und jedes Gateway definiert sind. 

![Mehrere trunk-Aufgaben](../../media/multiple-trunk-assignments.jpg)
