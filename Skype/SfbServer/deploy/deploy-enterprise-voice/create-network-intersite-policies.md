---
title: Erstellen von standortübergreifenden Netzwerkrichtlinien in Skype for Business Server 2015
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
ms.assetid: b0714aae-55dc-4587-b718-34a03f596b22
description: Erstellen Sie Netzwerk standortübergreifende Richtlinien, die von Enterprise-VoIP-anrufsteuerung in Skype für Business Server verwendet werden.
ms.openlocfilehash: 73eee49022f039bf1bd36d1a06176fa94f3ef3f7
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="create-network-intersite-policies-in-skype-for-business-server-2015"></a>Erstellen von standortübergreifenden Netzwerkrichtlinien in Skype for Business Server 2015
 
Erstellen Sie Netzwerk standortübergreifende Richtlinien, die von Enterprise-VoIP-anrufsteuerung in Skype für Business Server verwendet werden. 
  
Eine standortübergreifende Netzwerkrichtlinie definiert bandbreiteneinschränkungen zwischen Standorten, die direkte WAN-Verbindungen miteinander verbunden sind.
  
> [!IMPORTANT]
> Eine standortübergreifende Netzwerkrichtlinie ist erforderlich *nur* , wenn eine standortübergreifende direktverbindung zwischen zwei Netzwerkstandorten besteht.
  
In der Region „Nordamerika“ der Beispieltopologie besteht eine direkte Verbindung zwischen den Standorten „Reno“ und „Albuquerque“. Für diese beiden Standorte ist eine standortübergreifende Richtlinie erforderlich, die ein geeignetes Bandbreitenrichtlinienprofil anwendet. Im folgenden Beispiel wird das Profil „20Mb_Link“ angewendet.
  
### <a name="to-create-a-network-inter-site-policy"></a>So erstellen Sie eine standortübergreifende Netzwerkrichtlinie

1. Starten Sie die Skype for Business Server-Verwaltungsshell: Klicken Sie auf **Start**, zeigen Sie auf **Alle Programme** und dann auf **Skype for Business 2015** und klicken Sie anschließend auf **Skype for Business Server-Verwaltungsshell**.
    
2. Führen Sie das Cmdlet „New-CsNetworkInterSitePolicy“ aus, um für zwei Standorte mit standortübergreifender Direktverbindung standortübergreifende Netzwerkrichtlinien zu erstellen und ein geeignetes Bandbreitenrichtlinienprofil anzuwenden. Führen Sie beispielsweise den folgenden Befehl aus:
    
   ```
   New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link
   ```

3. Wiederholen Sie bei Bedarf Schritt 2, um standortübergreifende Netzwerkrichtlinien für alle Netzwerkstandorte mit standortübergreifender Direktverbindung zu erstellen.
    
## <a name="see-also"></a>Siehe auch

#### 

[Neue CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/new-csnetworkintersitepolicy?view=skype-ps)
  
[Get-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/get-csnetworkintersitepolicy?view=skype-ps)
  
[Set-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/set-csnetworkintersitepolicy?view=skype-ps)
  
[Remove-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/remove-csnetworkintersitepolicy?view=skype-ps)
