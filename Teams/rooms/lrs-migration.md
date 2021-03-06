---
title: Migrieren von lync Room-System Geräten zu Microsoft Teams-Chatrooms
ms.author: v-lanac
author: lanachin
ms.reviewer: sohailta
manager: serdars
audience: ITPro
ms.topic: quickstart
ms.service: msteams
f1.keywords:
- NOCSH
localization_priority: Normal
ms.collection:
- M365-collaboration
ms.assetid: ''
description: In diesem Thema erfahren Sie, wie Sie lync Room-System Geräte zur Verwendung der Microsoft Teams Rooms-Software migrieren.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 1b8b71637ec944c4d68fafbdde4263971590c453
ms.sourcegitcommit: cddaacf1e8dbcdfd3f94deee7057c89cee0e5699
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2020
ms.locfileid: "43137589"
---
# <a name="migrate-lync-room-system-lrs-devices-to-microsoft-teams-rooms"></a>Migrieren von lync-Geräten (lync Room System) zu Microsoft Teams-Räumen

Lync-Geräte (LRS) mit der Software für das Skype Room System Version 1 (SRS v1) haben [am 9. Oktober 2018 das Ende des Supports](https://support.microsoft.com/help/4043450/products-reaching-end-of-support-for-2018)erreicht. Dies bedeutet, dass keine Produktupdates oder -fixes mehr für die Skype Room Systems v1-Software zur Verfügung gestellt werden. Kunden mit Lync Room System-Geräten und Skype Room System v1-Software empfehlen wir, ihre Geräte auf Microsoft Teams-Räume zu aktualisieren.

Microsoft Teams Rooms-Software arbeitet mit Microsoft Teams zusätzlich zu Skype for Business Server und Online Diensten für Besprechungen und Anrufe auf allen Microsoft Teams rooms unterstützte Geräte.

Ihre vorhandenen Geräte funktionieren **möglicherweise** nach dem Ende des Skype Room System V1-Software Supports weiterhin. Wenn diese Software jedoch einen Softwarefehler trifft, der von Microsoft benötigt wird, um einen Fix freizugeben, wird er nicht unterstützt. SRS v1 verwendet TLS 1.0/1,1, das in Zukunft von Microsoft als veraltet markiert wird. Weitere Informationen finden Sie unter [vorbereiten auf TLS 1.0/1.1-deprecated](https://techcommunity.microsoft.com/t5/Skype-for-Business-Blog/Preparing-for-TLS-1-0-1-1-Deprecation-O365-Skype-for-Business/bc-p/223608). 

## <a name="which-devices-are-affected"></a>Welche Geräte sind betroffen?

Nachfolgend finden Sie eine Liste der Geräte, die von dieser Änderung betroffen sind:

- Crestron RL
- [Crestron RL2](https://www.crestron.com/Products/Featured-Solutions/Crestron-RL-2)
- [Intelligente Raumsysteme](https://support.smarttech.com/en/hardware/room-systems-skype)
- [Polycom CX8000](https://www.polycom.com/products-services/products-for-microsoft/skype-for-business/cx8000.html)

## <a name="upgrade-options"></a>Aktualisierungsoptionen

Es gibt mehrere Optionen zum Upgrade von lync Room-Systemen auf die nächste Generation von Microsoft Teams-Räumen.

### <a name="crestron-hardware-trade-in-program"></a>Crestron-Hardware-Trade-in-Programm

Crestron wird ein Upgrade auf das [Crestron SR-System](https://www.crestron.com/products/featured-solutions/crestron-sr) oder eine Entsprechung für alle nicht-Crestron lync Room-System Kunden (z. b. Smart oder Polycom LRS) bereitstellen. Details zu diesem Programm finden Sie [hier](https://support.crestron.com/app/answers/answer_view/a_id/1000220) oder <!-- For details, -->[e-Mail senden](mailto:lrsupgrade@crestron.com) Crestron-LRS-Unterstützung.  

### <a name="crestron-rl2-upgrade-to-microsoft-teams-rooms"></a>Crestron RL2-Upgrade auf Microsoft Teams-Chatrooms

Vorhandene Crestron-RL2 (auch als Crestron-RL200 bezeichnet) Kunden können ein Upgrade-Kit erwerben, um aktuelle RL2 auf RL3 mit einem für minimale Kosten pro Gerät zu aktualisieren. Details zu diesem Programm finden Sie [hier](https://crestron.com/Products/Workspace-Solutions/Unified-Communications/Crestron-RL-2/CCS-UC-250-KIT).

### <a name="smart-room-systems-upgrade"></a>Smart Room Systems-Upgrade

Für Smart LRS-Kunden arbeitet Smart mit Ausnahme des Crestron-Hardware-Trade-in-Programms auch an der Bereitstellung einer Lösung für das Upgrade auf Microsoft Teams-Chatrooms. Dieses Upgrade wird von Smart Technologies Inc. dem Kunden unter Produktsupport zur Verfügung gestellt. Weitere Informationen hierzu finden Sie [hier](https://support.smarttech.com/docs/hardware/room-systems-skype/srs-skype-v2/en/about/default.cshtml).


## <a name="what-should-you-do"></a>Was sollten Sie tun?

Wir empfehlen, dass Sie die lync Room-System Geräte vor der TLS 1.0/1.1-Missbilligung mithilfe der oben genannten Upgrade-Optionen in Microsoft Teams rooms aktualisieren. Darüber hinaus empfiehlt es sich, vorhandene Geräte durch neue Geräte zu ersetzen, die für Microsoft Teams-Räume zertifiziert sind. Weitere Informationen finden Sie unter [Room Devices](https://aka.ms/roomdevices) , und schauen Sie sich auch die [Anforderungen von Microsoft Teams rooms](https://docs.microsoft.com/skypeforbusiness/plan-your-deployment/clients-and-devices/requirements)an.  


> [!NOTE]
> Microsoft Teams Rooms-Software unterstützt das TLS 1,2-Protokoll ab dem 14. Dezember 2018 mit App-Version 4.0.64.0. Für lokale Kunden erfordert die Aktivierung der Kommunikation über TLS 1,2 für Microsoft Teams-Räume Skype for Business Server 2015 Kumulatives Update 9 (CU9) oder Skype for Business Server 2019 Kumulatives Update 1 (CU1). Die Änderung sollte keine Auswirkungen auf Skype for Business Online-Kunden haben, da Kunden Änderungen Forward-und abwärtskompatibel sind.
