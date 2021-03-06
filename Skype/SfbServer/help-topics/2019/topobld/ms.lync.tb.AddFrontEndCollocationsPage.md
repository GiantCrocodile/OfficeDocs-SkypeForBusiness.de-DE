---
title: Hinzufügen von Front-End-Server-Kollokationen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.tb.AddFrontEndCollocationsPage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 23e3bda7-a8bf-4da4-88e5-098ae2aa268f
ROBOTS: NOINDEX, NOFOLLOW
description: Bei einer Enterprise Edition-Bereitstellung befindet sich der A/V-Konferenzdienst im Front-End-Pool. Sie können den Vermittlungsserver auch im Front-End-Pool collocate, oder Sie können ihn als eigenständigen Server bereitstellen. Der A/V-Konferenzdienst ist immer in der Lage, wenn Konferenzen aktiviert sind.
ms.openlocfilehash: f651a206529ee968fc32bf86b6314c004f82c3bd
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41794884"
---
# <a name="add-front-end-server-collocations"></a>Hinzufügen von Front-End-Server-Kollokationen

Bei einer Enterprise Edition-Bereitstellung befindet sich der A/V-Konferenzdienst im Front-End-Pool. Sie können den Vermittlungsserver auch im Front-End-Pool collocate, oder Sie können ihn als eigenständigen Server bereitstellen. Der A/V-Konferenzdienst ist immer in der Lage, wenn Konferenzen aktiviert sind.

> [!NOTE]
> Ein A/V-Konferenzdienst ist erforderlich, wenn **Konferenz** auf der Seite **"Features auswählen** " ausgewählt wurde. Ein Enterprise Edition-Front-End-Pool verwendet einen zusammengefassten a/V-Konferenzdienst. Wenn Konferenz nicht ausgewählt wurde, ist der Collocate A/V-Konferenzdienst nicht verfügbar.

Sie können die collocate-Funktion auf einem Front-End-Server der Standard Edition oder in Enterprise Edition-Front-End-Pool übernehmen. Wenn Sie direkte SIP-Verbindungen zu einem qualifizierten PSTN-Gateway (Public Switched Telephone Network) bereitstellen, das die medienumgehung und den DNS-Lastenausgleich (Domain Name System) unterstützt, ist kein eigenständiger Vermittlungs Server Pool erforderlich. Ein eigenständiger Vermittlungs Server Pool ist nicht erforderlich, da qualifizierte Gateways in der Lage sind, den DNS-Lastenausgleich zu einem Pool von Vermittlungsservern durchzuführen und Datenverkehr von einem beliebigen Vermittlungsserver in einem Pool empfangen können. Wir empfehlen außerdem, dass Sie den Vermittlungs Server in einem Front-End-Pool collocate, wenn Sie IP-PBX-Anlagen bereitgestellt haben oder eine Verbindung mit dem Session Border Controller (SBC) eines Internet Telefonie-Serveranbieters herstellen, sofern eine der folgenden Bedingungen erfüllt ist:

- Die IP-PBX-oder SBC-Konfiguration ist für den Empfang von Datenverkehr von einem beliebigen Vermittlungsserver im Pool konfiguriert und kann den Datenverkehr gleicherweise an alle Vermittlungsserver im Pool weiterleiten.

- Die IP-PBX-oder SBC-Konfiguration ist für den Empfang von Datenverkehr von einem beliebigen Vermittlungsserver im Pool konfiguriert und kann den Datenverkehr gleicherweise an alle Vermittlungsserver im Pool weiterleiten.

Sie können das Planungs Tool verwenden, um zu überprüfen, ob die Auslastung vom Front-End-Pool, in dem Sie den Vermittlungs Server collocate möchten, verarbeitet werden kann. Wenn Ihre Umgebung diese Anforderungen nicht erfüllen kann, müssen Sie einen eigenständigen Vermittlungs Server Pool bereitstellen.

Im Allgemeinen wird die Verwendung des Vermittlungsservers nicht empfohlen, wenn Ihre Organisation über die Anforderungen an die Verfügbarkeit und Skalierbarkeit verfügt. Details zum abstimmen dieser Serverrollen in einem Front-End-Pool in einer Enterprise Edition-Bereitstellung finden Sie unter [definieren und Konfigurieren eines Front-End-Pools](https://technet.microsoft.com/library/713fc263-23dd-414a-b001-82932e4fe966.aspx) in der Bereitstellungsdokumentation. Details zu den A/V-Konferenzfeatures und-Komponenten finden Sie unter [Planen von Konferenzen](https://technet.microsoft.com/library/983a272a-e1b3-4d70-8f84-836b092fe526.aspx) in der Planungsdokumentation. Details zu den Enterprise-VoIP-Features und-Komponenten, einschließlich Mediation Server, finden Sie unter [Planen von Enterprise-VoIP in Skype for Business Server](../../../plan-your-deployment/enterprise-voice-solution/enterprise-voice.md) in der Planungsdokumentation.


