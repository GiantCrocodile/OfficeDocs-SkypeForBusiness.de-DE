---
title: Hohe Verfügbarkeit (Planungstool)
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 4/8/2016
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.plan.HighAvailability
- ms.lync.plan.HighAvailability
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 14a897b3-2406-46c7-b08f-490085b3d048
description: Das Hauptfenster Hochverfügbarkeits-Schema für die meisten Serverrollen in Skype für Business Server 2015 basiert auf Serverredundanz über pooling. Wenn ein Server ausfällt, auf dem eine bestimmte Serverrolle ausgeführt wird, übernehmen die anderen Server im Pool, auf denen die gleiche Rolle ausgeführt wird, die Last dieses Servers.
ms.openlocfilehash: 8441db5ee4a84c573ed6a1642473b827382e4654
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="high-availability-planning-tool"></a>Hohe Verfügbarkeit (Planungstool)
 
Das Hauptfenster Hochverfügbarkeits-Schema für die meisten Serverrollen in Skype für Business Server 2015 basiert auf Serverredundanz über pooling. Wenn ein Server ausfällt, auf dem eine bestimmte Serverrolle ausgeführt wird, übernehmen die anderen Server im Pool, auf denen die gleiche Rolle ausgeführt wird, die Last dieses Servers.
  
Skype für Business Server 2015 erfordert mindestens zwei Front-End-Servern, um hohe Verfügbarkeit zu aktivieren. Das Planungstool verwendet die folgenden Kriterien, um festzustellen, ob sie zusätzliche Server hinzufügen, um hohe Verfügbarkeit zu unterstützen:
  
- Wenn die Bereitstellung mindestens zwei Front-End-Server enthält, werden das Planungstool keinen zusätzlichen Server hinzugefügt.
    
- Wenn die Bereitstellung Edge-Server enthält, wird ein zusätzlicher Server hinzugefügt. 
    
- Wenn die Bereitstellung beständigen Chat enthält, das Planungstool für das Hinzufügen eines zusätzlichen Servers, aber nicht erhöhen der Anzahl Pool. Angenommen, wenn die Bereitstellung bereits vier Servern enthält, das Planungstool schlägt (für insgesamt fünf Servern) einen weiteren Server hinzufügen jedoch behält einen einzelnen Pool. 
    
Das Planungstool fügt auch eine Spiegeldatenbank SQL für alle Datenbanken. Beispielsweise wenn eine Front-End-SQL Server-Datenbank vorhanden ist, wird das Planungstool die anderen Datenbank als der Spiegeldatenbank für diese Vorlage hinzufügen und nennen Sie es als"Front-End Spiegel SQL-Datenbank.
  
Weitere Informationen zur Vorbereitung Ihrer Umgebung für hohe Verfügbarkeit finden Sie unter [Planen für hohe Verfügbarkeit und notfallwiederherstellung in Skype für Business Server 2015](../../plan-your-deployment/high-availability-and-disaster-recovery/high-availability-and-disaster-recovery.md).
  
