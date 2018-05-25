---
title: Director (Planungstool)
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 4/8/2016
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.plan.Director
- ms.lync.plan.Director
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 02795b46-21ec-4a85-9890-959c91d97df3
description: Ein Director ist ein Server mit Skype für Business Server 2015 Communications-Software, die Benutzeranfragen authentifizieren kann, jedoch ist kein Homeserver für alle Benutzerkonten.
ms.openlocfilehash: b379388b05e4beda934b13517f36bc792b6f0748
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="director-planning-tool"></a>Director (Planungstool)
 
Ein Director ist ein Server mit Skype für Business Server 2015 Communications-Software, die Benutzeranfragen authentifizieren kann, jedoch ist kein Homeserver für alle Benutzerkonten. 
  
Diese Rolle ist optional, würde der Bereitstellung eines Directors in den folgenden zwei Szenarien werden sollen:
  
- Wenn Sie Zugriff durch externe Benutzer durch die Bereitstellung von Edge-Server aktivieren, sollten Sie auch einen Director bereitstellen. In diesem Szenario der Director externe Benutzer authentifiziert und anschließend übergibt den Datenverkehr an interne Server. Wenn ein Director zur Authentifizierung externer Benutzer verwendet wird, entlastet es Front-End-Poolserver der Aufwand für das Ausführen der Authentifizierung von romotebenutzern einhergeht. Darüber hinaus werden interne Front-End-Pools bösartigem Datenverkehr wie Denial-of-Service-Angriffen zu isolieren. Wenn das Netzwerk mit ungültigen externen Datenverkehr in einem solchen Angriff bereits ist, endet dieser Datenverkehr den Director.
    
- Wenn Sie mehrere Front-End-Pools an einem zentralen Standort bereitstellen, durch Hinzufügen eines Directors in dieser Website können Authentifizierungsanfragen optimieren und die Leistung verbessert. In diesem Szenario werden alle Anforderungen ersten den Übermittler, die sie dann auf dem richtigen Front-End-Pool weitergeleitet.
    
