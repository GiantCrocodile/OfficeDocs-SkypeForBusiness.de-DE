---
title: Zertifikatsanforderung (Zertifizierungsstelle)
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/26/2015
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.dep.DeployCertRequestCA
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: a609f1b0-ae13-44ca-a467-b7fb14ff18a1
description: 'Wenn eine Anforderung an eine Onlinezertifizierungsstelle (CA) zu tätigen (normalerweise sind Server, die im internen Netzwerk) auf der Seite Zertifizierungsstelle (Certification Authority, CA) für die auswählen, werden Sie zwei Optionen angezeigt:'
ms.openlocfilehash: 6fea8ba9500e1612ff13796f4c58550687baa99a
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="certificate-request-certificate-authority"></a>Zertifikatsanforderung (Zertifizierungsstelle)
 
Beim Erstellen einer Zertifikatsanforderung an eine Onlinezertifizierungsstelle (im Allgemeinen ein Server im internen Netzwerk) auf der Seite **Zertifizierungsstelle auswählen** werden zwei Optionen angezeigt:
  
1. Wählen Sie eine Zertifizierungsstelle aus der Liste mit den in Ihrer Umgebung erkannten Stellen aus.
    
2. Wählen Sie eine andere Zertifizierungsstelle aus.
    
Wenn Sie die erste Option auswählen, sehen Sie ein Dropdown-Listenfeld, das alle Windows Server-basierten Zertifizierungsstellen enthält, die in Ihrer Umgebung erkannt werden. Wählen Sie die Zertifizierungsstelle, die für das Zertifikat geeignet ist. Möglicherweise müssen den Zertifizierungsstellen-Administrator wissen, welche Zertifizierungsstelle auswählen zu konsultieren.
  
Bei Wahl der zweiten Option geben Sie den vollqualifizierten Domänennamen und die Zertifizierungsstelleninstanz der Zertifizierungsstelle ein, die Sie für das Zertifikat verwenden möchten. Diese Option kommt in Frage, wenn die gewünschte Zertifizierungsstelle keine Windows Server-basierte Zertifizierungsstelle ist, jedoch für Windows Server-basierte Zertifizierungsstellen funktioniert.
  
> [!IMPORTANT]
> Für eine erfolgreiche Zertifikatsanforderung müssen Sie Mitglied der entsprechenden Gruppen sein. Zertifizierungsstellen verfügen normalerweise über eine andere Berechtigung Anforderung die Anforderungen für die Installation von Skype für Business Server auf Servern. Informieren Sie sich über die Voraussetzungen für das Anfordern des Zertifikats bei Ihrem Zertifizierungsstellenadministrator. 
  
