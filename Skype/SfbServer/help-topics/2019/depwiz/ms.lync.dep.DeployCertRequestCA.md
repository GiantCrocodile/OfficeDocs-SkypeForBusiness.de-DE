---
title: Zertifikatsanforderung (Zertifizierungsstelle)
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
ms.custom:
- ms.lync.dep.DeployCertRequestCA
ms.prod: skype-for-business-itpro
f1.keywords:
- CSH
localization_priority: Normal
ms.assetid: a609f1b0-ae13-44ca-a467-b7fb14ff18a1
ROBOTS: NOINDEX, NOFOLLOW
description: 'Beim Erstellen einer Zertifikatsanforderung an eine Onlinezertifizierungsstelle (im Allgemeinen ein Server im internen Netzwerk) auf der Seite Zertifizierungsstelle auswählen werden zwei Optionen angezeigt:'
ms.openlocfilehash: 6c52a46bf40211d05ea47205d2573627910d3ba6
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41796756"
---
# <a name="certificate-request-certificate-authority"></a>Zertifikatsanforderung (Zertifizierungsstelle)
 
Beim Erstellen einer Zertifikatsanforderung an eine Onlinezertifizierungsstelle (im Allgemeinen ein Server im internen Netzwerk) auf der Seite **Zertifizierungsstelle auswählen** werden zwei Optionen angezeigt:
  
1. Wählen Sie eine Zertifizierungsstelle aus der Liste mit den in Ihrer Umgebung erkannten Stellen aus.
    
2. Wählen Sie eine andere Zertifizierungsstelle aus.
    
Wenn Sie die erste Option auswählen, wird eine Dropdownliste angezeigt, die alle auf Windows Server basierenden Zertifizierungsstellen enthält, die in Ihrer Umgebung erkannt werden. Wählen Sie die Zertifizierungsstelle aus, die für Ihr Zertifikat geeignet ist. Möglicherweise müssen Sie sich bei Ihrem Zertifizierungsstellenadministrator erkundigen, welche Zertifizierungsstelle Sie auswählen sollen.
  
Bei Wahl der zweiten Option geben Sie den vollqualifizierten Domänennamen und die Zertifizierungsstelleninstanz der Zertifizierungsstelle ein, die Sie für das Zertifikat verwenden möchten. Diese Option kommt in Frage, wenn die gewünschte Zertifizierungsstelle keine Windows Server-basierte Zertifizierungsstelle ist, jedoch für Windows Server-basierte Zertifizierungsstellen funktioniert.
  
> [!IMPORTANT]
> Für eine erfolgreiche Zertifikatsanforderung müssen Sie Mitglied der entsprechenden Gruppen sein. In der Regel verfügen Zertifizierungsstellen über eine andere Berechtigungsanforderung als die Anforderungen für die Installation von Skype for Business Server auf Servern. Informieren Sie sich über die Voraussetzungen für das Anfordern des Zertifikats bei Ihrem Zertifizierungsstellenadministrator. 
  

