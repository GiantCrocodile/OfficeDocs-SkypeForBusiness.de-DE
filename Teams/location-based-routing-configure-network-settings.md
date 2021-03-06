---
title: Konfigurieren von Netzwerkeinstellungen – standortbasiertes Routing
author: LanaChin
ms.author: v-lanac
manager: serdars
ms.topic: article
ms.reviewer: roykuntz
audience: admin
ms.service: msteams
search.appverid: MET150
description: Hier erfahren Sie, wie Sie netzwerkregionen,-Standorte und-Subnetze für standortbasiertes Routing für das direkte Routing erstellen und einrichten.
localization_priority: Normal
f1.keywords:
- NOCSH
ms.collection:
- M365-voice
appliesto:
- Microsoft Teams
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 8025467a0581c95a40551244948a8e6b7c0ecbc8
ms.sourcegitcommit: 3e5cac88911611c94c0330bf50af9c34db308cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2020
ms.locfileid: "45372055"
---
# <a name="configure-network-settings-for-location-based-routing"></a>Konfigurieren der Netzwerkeinstellungen für das standortbasierte Routing

Wenn Sie dies noch nicht getan haben, lesen Sie [Planen des ortsbasierten Routings für das direkte Routing](location-based-routing-plan.md) , um weitere Schritte zu überprüfen, die Sie ausführen müssen, bevor Sie die Netzwerkeinstellungen für standortbasiertes Routing konfigurieren.

In diesem Artikel wird beschrieben, wie Sie Netzwerkeinstellungen für standortbasiertes Routing konfigurieren. Nachdem Sie die direkte Weiterleitung des Telefonsystems in Ihrer Organisation bereitgestellt haben, besteht der nächste Schritt darin, netzwerkregionen, Netzwerk Websites und Netzwerk-Subnets zu erstellen und einzurichten.

## <a name="define-network-regions"></a>Definieren von netzwerkregionen

Eine netzwerkregion enthält eine Sammlung von Netzwerk Websites und verbindet verschiedene Teile eines Netzwerks über mehrere geographische Bereiche hinweg. Eine schrittweise Anleitung zum Konfigurieren von netzwerkregionen finden Sie unter [Verwalten Ihrer Netzwerktopologie für Cloud-Features in Teams](manage-your-network-topology.md).

## <a name="define-network-sites"></a>Definieren von Netzwerk Websites

Eine Netzwerk Website steht für einen Standort, an dem Ihre Organisation über einen physikalischen Ort verfügt, beispielsweise ein Büro, einen Satz von Gebäuden oder einen Campus. Sie müssen jede Netzwerk Website in Ihrer Topologie einem Netzwerkbereich zuordnen. Eine schrittweise Anleitung zum Konfigurieren von Netzwerk Websites finden Sie unter [Verwalten der Netzwerktopologie für Cloud-Features in Teams](manage-your-network-topology.md).

Eine bewährte Methode für standortbasiertes Routing ist das Erstellen einer separaten Website für jeden Standort, der über eine eindeutige PSTN-Konnektivität verfügt. Sie können eine Website erstellen, die für standortbasiertes Routing oder eine Website aktiviert ist, die für standortbasiertes Routing nicht aktiviert ist. So können Sie beispielsweise eine Website erstellen, die für standortbasiertes Routing nicht aktiviert ist, damit Benutzer, die für standortbasiertes Routing aktiviert sind, PSTN-Anrufe tätigen können, wenn Sie zu dieser Website wechseln.

## <a name="define-network-subnets"></a>Definieren von Netzwerk-Subnetzen

Jedes Subnetz muss einer bestimmten Netzwerk Website zugeordnet sein. Sie können mehrere Subnetze mit derselben Netzwerk Website verknüpfen, aber Sie können nicht mehrere Websites mit demselben Subnetz verknüpfen. Eine schrittweise Anleitung zum Konfigurieren von Netzwerksubnets finden Sie unter [Verwalten Ihrer Netzwerktopologie für Cloud-Features in Teams](manage-your-network-topology.md).

Für standortbasiertes Routing müssen IP-Subnetze an der Stelle, an der Teams-Endpunkte eine Verbindung mit dem Netzwerk herstellen können, definiert und einem definierten Netzwerk zugeordnet werden, um eine Maut Umgehung durchzusetzen. Diese Zuordnung von Subnetzen ermöglicht standortbasiertes Routing, die Endpunkte geografisch zu finden, um festzustellen, ob ein bestimmter PSTN-Anruf zulässig ist. Sowohl IPv6-als auch IPv4-Subnetze werden unterstützt. Wenn Sie feststellen, ob sich ein Teams-Endpunkt an einer Website befindet, überprüft standortbasiertes Routing zunächst auf eine übereinstimmende IPv6-Adresse. Wenn keine IPv6-Adresse vorhanden ist, überprüft standortbasiertes Routing auf eine IPv4-Adresse.

## <a name="define-trusted-ip-addresses-external-subnets"></a>Definieren von vertrauenswürdigen IP-Adressen (externe Subnetze)

Vertrauenswürdige IP-Adressen sind die Internet externen IP-Adressen des Unternehmensnetzwerks und werden verwendet, um zu ermitteln, ob sich der Endpunkt des Benutzers innerhalb des Unternehmensnetzwerks befindet. Eine schrittweise Anleitung zum Konfigurieren von vertrauenswürdigen IP-Adressen finden Sie unter [Verwalten Ihrer Netzwerktopologie für Cloud-Features in Teams](manage-your-network-topology.md).

Wenn die externe IP-Adresse des Benutzers mit einer IP-Adresse übereinstimmt, die sich in der Liste der vertrauenswürdigen IP-Adressen befindet, überprüft standortbasiertes Routing, um das interne Subnetz zu ermitteln, in dem sich der Endpunkt des Benutzers befindet. Wenn die externe IP-Adresse des Benutzers nicht mit einer IP-Adresse übereinstimmt, die in der Liste vertrauenswürdiger IP-Adressen definiert ist, wird der Endpunkt als an einem unbekannten Speicherort klassifiziert, und alle PSTN-Anrufe an oder von einem Benutzer, der für standortbasiertes Routing aktiviert ist, werden blockiert.

## <a name="next-steps"></a>Nächste Schritte

Wechseln Sie zum [Aktivieren des ortsbasierten Routings für das direkte Routing](location-based-routing-enable.md).

## <a name="related-topics"></a>Verwandte Themen

- [Netzwerkeinstellungen für Cloud-Sprachfeatures in Teams](cloud-voice-network-settings.md)
