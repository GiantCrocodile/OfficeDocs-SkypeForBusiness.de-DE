---
title: Hinzufügen des FQDN des Front-End-Pools
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.tb.AddFrontEndPoolPage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 02ae996c-a1c6-4ff4-b6d6-bdef4ad44d2a
ROBOTS: NOINDEX, NOFOLLOW
description: Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Front-End-Pools an, den Sie erstellen. Sie können den FQDN eines Pools nicht ändern, nachdem Sie die Topologie mit dem Front-End-Pool veröffentlicht haben. Wenn Sie einen Pool umbenennen müssen, müssen Sie den Pool löschen und dann einen neuen Pool mit dem neuen FQDN hinzufügen.
ms.openlocfilehash: 0c6fdf24ec19fe56ff86d4a5b43af2e48aedb3e2
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41798522"
---
# <a name="add-front-end-pool-fqdn"></a>Hinzufügen des FQDN des Front-End-Pools
 
Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Front-End-Pools an, den Sie erstellen. Sie können den FQDN eines Pools nicht ändern, nachdem Sie die Topologie mit dem Front-End-Pool veröffentlicht haben. Wenn Sie einen Pool umbenennen müssen, müssen Sie den Pool löschen und dann einen neuen Pool mit dem neuen FQDN hinzufügen.
  
> [!TIP]
> Wenn Sie beabsichtigen, in Zukunft einen Front-End-Pool zu implementieren, wählen Sie den **Pool für mehrere Computer**aus. Wenngleich ein Pool per Definition mindestens zwei Computer mit Lastenausgleich umfasst, können Sie einen Pool mit einem einzigen Computer sowie einen Pool-FQDN für diesen einzelnen Computer erstellen. Wenn Sie bereit sind, dem Pool später weitere Computer hinzuzufügen, müssen Sie den Topology Builder erneut ausführen, um das neue Poolmitglied zu definieren, die neue Topologie zu veröffentlichen und dann den neuen Front-End-Pool-Member über den Skype for Business Server-Bereitstellungs-Assistenten einzurichten. Darüber hinaus müssen Sie das neue Poolmitglied den entsprechenden Lastenausgleichs Komponenten für den Pool, DNS-Lastenausgleich (Domain Name System) oder Hardwarelastenausgleichs hinzufügen. In vielen Fällen sind beide Lastenausgleichssysteme vorhanden. Stellen Sie sicher, dass Sie beide den neuen Mitgliedsserver hinzufügen. 
  

