---
title: Hinzufügen von Front-End-Computern
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.tb.AddFrontEndMachinePage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: e7fe2522-1bd2-416a-9dbb-51cacea9c6e0
ROBOTS: NOINDEX, NOFOLLOW
description: Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) jedes Computers an, den Sie als Front-End-Server in diesem Pool hinzufügen möchten. Nach dem Hinzufügen eines Computers zur Liste können Sie den vollqualifizierten Domänennamen des Computers zu einem beliebigen Zeitpunkt vor der Veröffentlichung der Topologie aktualisieren oder aus dem Pool entfernen. Nachdem Sie die Topologie veröffentlicht haben, müssen Sie den Server im Topologie-Generator durch Ändern des FQDN löschen und dann einen neuen Server zum Pool mit dem neuen FQDN hinzufügen. Details zum Hinzufügen eines Front-End-Pools zur Topologie finden Sie unter Definieren und Konfigurieren eines Front-End-Pools in der Bereitstellungsdokumentation.
ms.openlocfilehash: a4ff4ce7a7fc775e33657dc2f8602d62163ed1d4
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41798542"
---
# <a name="add-front-end-machine"></a>Hinzufügen von Front-End-Computern

Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) jedes Computers an, den Sie als Front-End-Server in diesem Pool hinzufügen möchten. Nach dem Hinzufügen eines Computers zur Liste können Sie den vollqualifizierten Domänennamen des Computers zu einem beliebigen Zeitpunkt vor der Veröffentlichung der Topologie aktualisieren oder aus dem Pool entfernen. Nachdem Sie die Topologie veröffentlicht haben, müssen Sie den Server im Topologie-Generator durch Ändern des FQDN löschen und dann einen neuen Server zum Pool mit dem neuen FQDN hinzufügen. Details zum Hinzufügen eines Front-End-Pools zur Topologie finden Sie unter [definieren und Konfigurieren eines Front-End-Pools](https://technet.microsoft.com/library/713fc263-23dd-414a-b001-82932e4fe966.aspx) in der Bereitstellungsdokumentation.

> [!IMPORTANT]
> Beachten Sie, dass der Topologie-Generator angibt, dass Sie bis zu 20 Front-End-Server in einem Pool haben können. Die maximal unterstützte Anzahl von Servern ist 12. Sie können bis zu 20 statefull-Server im Fabric definieren, von denen 12 gleichzeitig aktiv und online sein können.


