---
title: Konfigurieren von DNS-Einträgen für die Pilotpoolbereitstellung
ms.author: kenwith
author: kenwith
manager: serdars
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
description: Vor der Bereitstellung des pilotpools, müssen Sie die DNS-Host-A-Einträge für den pilotpool aktualisieren. Zum erfolgreichen Durchführen dieses Verfahrens sollten Sie auf dem Server oder Domäne als Mitglied der Gruppe Domänen-Admins oder ein Mitglied der Gruppe "DnsAdmins" angemeldet sein.
ms.openlocfilehash: 13492f7972e127de7a8200a0dbe933c72aba2da7
ms.sourcegitcommit: e9f277dc96265a193c6298c3556ef16ff640071d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2018
ms.locfileid: "25029895"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a>Konfigurieren von DNS-Einträgen für die Pilotpoolbereitstellung

Vor dem Bereitstellen des pilotpools, müssen Sie die DNS-Host-A-Einträge für den pilotpool aktualisieren. Zum erfolgreichen Durchführen dieses Verfahrens sollten Sie auf dem Server oder Domäne als Mitglied der Gruppe Domänen-Admins oder ein Mitglied der Gruppe "DnsAdmins" angemeldet sein.
  
### <a name="to-configure-dns-host-a-records"></a>So konfigurieren Sie DNS-Host-A-Einträge

1. Klicken Sie auf dem Server Domain Name System (DNS) klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.
    
2. Klicken Sie in der Konsolenstruktur für Ihre Domäne erweitern Sie **Forward-Lookupzonen**, und anschließend mit der Maustaste der Domäne, in der Skype für Business Server 2019 installiert werden.
    
3. Klicken Sie auf **Neuer Host (A oder AAAA)**.
    
4. Klicken Sie auf **Name**, geben Sie den Hostnamen für die Skype für Business Server 2019 Pool (der Domänenname wird von der Zone, die der Datensatz ist in definiert und muss nicht als Teil des A-Eintrags eingegeben werden verwendet).
    
5. Klicken Sie auf **IP-Adresse**, und geben Sie die IP-Adresse für den Front-End-Pool.
    
6. Klicken Sie auf **Host hinzufügen**, und klicken Sie dann auf **OK**. 
    
7. Wenn Sie fertig sind, klicken Sie auf **Fertig**.
    
