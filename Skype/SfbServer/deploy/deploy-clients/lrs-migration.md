---
title: Migrieren von Lync Raum System Geräte zu Skype Raum System, Version 2
ms.author: jambirk
author: jambirk
ms.reviewer: sohailta
manager: serdars
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: ''
description: Lesen Sie in diesem Thema erfahren, wie Lync Raum Systemkomponenten Verwendung die Systemsoftware Skype Raum v2 migrieren.
ms.openlocfilehash: 954d7893572c1d97506f4b6845792b0b940c3f2b
ms.sourcegitcommit: 6212645c485c41aafe1206bf7d39171ce35837b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2018
ms.locfileid: "24968635"
---
# <a name="migrate-lync-room-system-lrs-devices-to-skype-room-system-v2"></a>Migrieren von Lync Raum System (LRS) Geräte zu Skype Raum System v2 
Lync Raum System (LRS) Geräte mit Skype Raum System Version 1 (SRS v1) Software werden Ablauf des Supports auf 9 Oktober 2018 erreichen. Dies bedeutet, dass Skype Raum Systemsoftware Produktupdates oder Hotfixes nach diesem Datum nicht abgerufen werden. Kunden mit Lync Raum System im Geräte-Skype Raum Systemsoftware v1, sollten ihre Geräte auf Skype Raum System, Version 2 (SRS v2) zu aktualisieren.

Skype Raum System Version 2 (SRS v2) Software arbeitet mit Microsoft-Teams, zusätzlich zu Skype Business Server und Online-Dienste für Besprechungen und Aufrufen von auf allen Geräten von SRS v2 unterstützt.

Ihre vorhandenen Geräte **können** weiterhin funktionsfähig, nach dem Ende des Skype Raum Systemsoftware v1 unterstützen. Diese Software einen Software-Fehler, der ein Update freigeben Microsoft benötigt werden schließlich erreicht, oder Sie haben einen Fall, in dem eine vorhandene Kommunikationsprotokoll von Skype Raum System v1 Software Änderungen verwendet oder wird nicht mehr unterstützt. Eine solche bekannte Änderung ist das Verwerfen von TLS 1.0 / 1.1 in Microsoft Office 365. Erfahren Sie mehr über die [Vorbereitung auf das Verwerfen der TLS 1.0/1.1](https://techcommunity.microsoft.com/t5/Skype-for-Business-Blog/Preparing-for-TLS-1-0-1-1-Deprecation-O365-Skype-for-Business/bc-p/223608).  

## <a name="which-devices-are-affected"></a>Welche Geräte betroffen sind?
Hier wird die Liste der Geräte, die von dieser Änderung betroffen sind:
- [Intelligente Raum-Systeme](https://smartkapp.com/products/smart-room-systems)
- [Crestron RL2](https://www.crestron.com/en-US/Products/Featured-Solutions/Crestron-RL-2)
- [Polycom CX8000](http://www.polycom.com/products-services/products-for-microsoft/skype-for-business/cx8000.html)
- Crestron RL

## <a name="upgrade-options"></a>Upgrade-Optionen
Es gibt mehrere Optionen für das Upgrade von Lync Raum Systeme auf die nächste Generation von Skype Raum Systeme (SRS v2).

### <a name="crestron-hardware-trade-in-program"></a>Crestron Hardware Rückkauf Programm
Crestron wird ein Upgrade der [Crestron SR-System](https://www.crestron.com/en-us/products/featured-solutions/crestron-sr) oder einer gleichwertigen für alle nicht-Crestron Lync Raum System Kunden bereitstellen. Finden Sie unter Details dieses Programms [hier](https://support.crestron.com/app/answers/answer_view/a_id/1000220) oder <!-- For details, --> [e-Mail](mailto:lrsupgrade@crestron.com) Crestron LRS Support.  


### <a name="crestron-rl2-to-rl3"></a>Crestron RL2 auf RL3
Bestehende Crestron RL2 (auch als Crestron RL200 bezeichnet) Kunden können ein Aktualisierungspaket zum Aktualisieren des aktuellen RL2 RL3 Verwendung erwerben eine minimale Kosten pro Gerät. Finden Sie unter Details dieses Programms [hier](https://support.crestron.com/app/answers/answer_view/a_id/1000220) oder <!-- For details, --> [e-Mail](mailto:lrsupgrade@crestron.com) Crestron LRS Support.  


### <a name="smart-room-systems-upgrade--diy-program"></a>Intelligente Raum Systeme Upgrade & DIY Programm
SMART LRS Kunden, ausreichend Abstand zu platzieren Crestron Hardware Rückkauf Programm arbeiten Microsoft und EFFIZIENT auch auf die Bereitstellung einer Lösung für das upgrade auf Skype Raum System v2. Microsoft ist eine DIY Lösung auch für intelligente LRS Kunden testen. Weitere Informationen zu dieser Programme werden auf dieser Seite in frühe Oktober 2018 bereitgestellt. Stellen Sie sicher, dass Sie für die Updates auf diese Upgradeoptionen zu überprüfen.

<!--  
For later 
### Do-It-Yourself
A Do-It-Yourself option is also available for customers with upgrade to Windows 10 and Skype Room Systems v2 software. Windows 10 Enterprise Licenses are available through [approved resellers](https://www.microsoft.com/en-us/Licensing/how-to-buy/how-to-buy.aspx) and Skype Room System V2 software will be available through this guide. 
 
  
To use this option however, customers must additionaly buy a [Logitech Screen Share](https://www.logitech.com/en-us/product/screen-share) adapter. Microsoft will provide instructions on how to use this adapter with Skype Room System v2 software. 


Look for upgrade instructions on this page shortly. 
  
### Summary of upgrade options
This table lists summary of all available options for existing LRS devices:
<!--  For later 
| Upgrade Option | SMART Room Systems | Crestron RL2 | Polycom CX8000 | Crestron RL |
|:--- |:--- |:--- |:--- |:--- |
|**Crestron hardware </br>Trade-in program**|Available|Available|Available|Available|
|**Crestron RL3**|Not Available|Available|Not Available|Not Available|
|**Do-It-Yourself**|Available|Not Available|Not Available|Not Available|
| | | | | |
-->

## <a name="what-should-you-do"></a>Was sollten Sie tun?
Es wird empfohlen, dass Sie Lync Raum Systemkomponenten Skype Raum Systemen V2 vor TLS 1.0/1.1 das Verwerfen von oben erwähnten Upgradeoptionen aktualisieren möchten. Darüber hinaus können Sie auch bedenken, Austauschen von vorhandenen Geräten mit neuer für SRS v2 zertifizierte Geräte. Finden Sie unter Details in [Skype Raum Systemen v2 Anforderungen](https://docs.microsoft.com/en-us/skypeforbusiness/plan-your-deployment/clients-and-devices/requirements).  

> [!NOTE]
> Fingereingabe und Whiteboard-Funktionalität ist in Skype Raum System v2 noch nicht unterstützt. Unterstützung von Touch und Whiteboard ist noch nicht verarbeiteten für Skype Raum System v2 und H1 CY2019 hinzugefügt werden.