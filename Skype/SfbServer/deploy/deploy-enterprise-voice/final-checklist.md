---
title: Anruf Admission Control endgültigen Prüfliste zur Bereitstellung von Skype für Business Server 2015
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Admin
ms.assetid: d56a525f-3da5-4ac0-a311-0c5efd98c9df
description: Endgültige Checkliste für die Bereitstellung von Call Admission Control (CAC) in Skype für Business Server Enterprise-VoIP.
ms.openlocfilehash: 9971d59f0b9c3c2c1f9bfd5e8176122715b19d20
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="call-admission-control-deployment-final-checklist-for-skype-for-business-server-2015"></a>Bereitstellung der Anrufsteuerung: endgültige Prüfliste für Skype for Business Server 2015
 
Endgültige Checkliste für die Bereitstellung von Call Admission Control (CAC) in Skype für Business Server Enterprise-VoIP. 
  
Überprüfen Sie anhand der folgenden Liste, ob Sie alle erforderlichen Konfigurationsaufgaben für die Bereitstellung der Anrufsteuerung (Call Admission Control, CAC) abgeschlossen haben.
  
- Wenn eine oder mehrere Edgeserver bereitgestellt werden, muss jede externe IP-Adresse der Subnetliste in den netzwerkkonfigurationseinstellungen, denen eine Bitmaske 32 hinzugefügt werden. Sie sollten dieses Subnetz (IP-Adresse) außerdem der Netzwerkstandort-ID für den geografischen Standort zuordnen, an dem der A/V-Edgedienst bereitgestellt wurde.
    
    > [!NOTE]
    > Edge-Server sind zum Implementieren der Anrufsteuerung nicht erforderlich. 
  
- Stellen Sie sicher, dass die Anrufsteuerung aktiviert ist, als der angegebene in [Aktivieren der anrufsteuerung in Skype für Business Server 2015](enable-call-admission-control.md).
    
- Stellen Sie sicher, dass die Anrufsteuerung an allen zentralen Standorten aktiviert ist. Dies kann über den Topologie-Generator erfolgen. Wenn eine Warnung generiert wird, wenn Sie veröffentlichen, ignoriert *jedoch nicht* .
    
- Stellen Sie sicher, dass alle im Unternehmensnetzwerk verwalteten Subnetze in den Netzwerkkonfigurationseinstellungen konfiguriert sind. Es ist außerdem wichtig, dass jedes Subnetz einem Netzwerkstandort zugeordnet werden soll, wie unter [Bereitstellen von netzwerkregionen, Standorten und Subnetzen in Skype für Business 2015](deploy-network.md)erläutert wird.
    
- Stellen Sie sicher, dass die Subnetz- oder IP-Adressen aller Front-End-Server, Survivable Branch Appliances (SBAs), A/V-Konferenzserver (sofern in einem separaten Pool bereitgestellt) und Vermittlungsserver in den Netzwerkkonfigurationseinstellungen konfiguriert sind.
    
