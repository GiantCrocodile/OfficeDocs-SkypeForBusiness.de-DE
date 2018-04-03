---
title: Hinzufügen des A / V-MCU-Pools
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.tb.AddAvMcuPoolPage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: e201875e-1e81-4756-942f-c17d177e997b
description: Alle Enterprise Edition-Front-End-Server von einem zentralen Standort, die nicht über einen verbundenen verfügen A / V-Konferenzdienst können das gleiche eigenständige A / V-konferenzpool. Für jede A / V-konferenzpool, geben Sie einen vollqualifizierten Domänennamen (FQDN) für den Pool und gibt an, ob es nur einen einzelnen A hat / V-Konferenzserver oder mehrere, Lastenausgleich und A / V-Konferenzserver.
ms.openlocfilehash: d1712829030836446c06a2e335c424d51a19e466
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="add-av-mcu-pool"></a>Hinzufügen des A / V-MCU-Pools
 
Alle Enterprise Edition-Front-End-Server von einem zentralen Standort, die nicht über einen verbundenen verfügen A / V-Konferenzdienst können das gleiche eigenständige A / V-konferenzpool. Für jede A / V-konferenzpool, geben Sie einen vollqualifizierten Domänennamen (FQDN) für den Pool und gibt an, ob es nur einen einzelnen A hat / V-Konferenzserver oder mehrere, Lastenausgleich und A / V-Konferenzserver.
  
> [!IMPORTANT]
> Sie können keinen einzelnen Server Pool in einen Pool von mehreren Servern konvertieren. Wenn Sie später entscheiden, dass Ihre Organisation einen Pool von mehreren Servern benötigt, müssen Sie den Pool einem einzelnen Server zu löschen, und fügen Sie MultiServer-Pool. 
  
> [!TIP]
> Wenn Sie planen, implementieren einen A / V-konferenzpool wählen Sie **Pool mit mehreren Computern**in der Zukunft aus. Wenngleich ein Pool per Definition mindestens zwei Computer mit Lastenausgleich umfasst, können Sie einen Pool mit einem einzigen Computer sowie einen Pool-FQDN für diesen einzelnen Computer erstellen. Wenn Sie später weitere Computer zum Pool hinzufügen möchten, müssen Sie den Topologie-Generator erneut aus, um das neue Mitglied Pool definieren, die neue Topologie veröffentlichen und richten Sie dann den neuen A / V-konferenzpool Member über die Skype für Business Server-Bereitstellungs-Assistenten. A / V-Konferenzserver-Pools, dass sie nicht zum Erstellen eines Pools Lastenausgleich laden müssen eindeutig sind. A / V-konferenzpools Lastenausgleich intern und zusätzlichen Hardware ist nicht erforderlich. 
  
