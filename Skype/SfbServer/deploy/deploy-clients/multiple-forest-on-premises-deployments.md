---
title: Lokale Bereitstellungen von Skype Room System mit mehreren Gesamtstrukturen
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/4/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 6793fca0-3970-44e4-8703-1925428c1967
description: Lesen Sie dieses Thema und erfahren Sie, wie Skype Room System in einer lokalen Umgebung mit mehrfacher Gesamtstruktur bereitgestellt wird.
ms.openlocfilehash: b5a0a2615f8174ea5e7d56dcaf0830765365bb48
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="skype-room-system-multiple-forest-on-premises-deployments"></a>Lokale Bereitstellungen von Skype Room System mit mehreren Gesamtstrukturen
 
Lesen Sie dieses Thema und erfahren Sie, wie Skype Room System in einer lokalen Umgebung mit mehrfacher Gesamtstruktur bereitgestellt wird.
  
> [!NOTE]
> Um die Bereitstellung in mehreren Gesamtstrukturen erfordert Skype Raum System Exchange Server 2013 CU6 auf 26 August 2014 veröffentlicht. Vermeiden Sie ein vorhandenes Postfach für Skype Raum System wiederverwenden. Verwenden Sie ein neues (alte Postfach löschen und Neuerstellen) Ressourcenpostfach für Skype Raum System. Informationen zum Wiederherstellen von Besprechungen verloren durch Löschen des Postfachs finden Sie unter [Connect- oder Wiederherstellen eines gelöschten Postfachs](https://technet.microsoft.com/en-us/library/jj863438%28v=exchg.150%29.aspx). 
  
Nachdem das Postfach erstellt wurde, können Sie Set-CalendarProcessing für die Postfachkonfiguration verwenden. Mehr dazu erfahren Sie in den Schritten 3–6 unter „Lokale Bereitstellungen mit einzelner Gesamtstruktur“. Aktivieren Sie nach dem Erstellen einer Exchange-Ressourcenpostfach für Skype Raum System, das Konto für Skype für Unternehmen mithilfe des Verfahrens in Skype Raum Systemkonten aktivieren für Skype für Unternehmen unter Gesamtstruktur lokale Bereitstellungen.
  
## <a name="option-1-create-a-new-resource-mailbox"></a>Option 1: Erstellen eines neuen Ressourcenpostfachs

Skype-Chatroom-System in einer Umgebung mit mehreren Gesamtstrukturen bereitstellen:
  
1. Erstellen Sie einen verknüpften Nutzer (LinkedRoomTest) in Active Directory (Authentifizierungs-Gesamtstruktur).
    
2. Führen Sie die folgenden Befehle in der Exchange Server-Verwaltungsshell aus:
    
   ```
   $cred = Get-Credential AuthForest\LinkedRoomTest
   new-mailbox -Alias LinkedRoomTest -LinkedMasterAccount AuthForest\LinkedRoomTest -LinkedDomainController AuthForest-4939.AuthForest.extest.contoso.com -UserPrincipalName LinkedRoomTest@ExchangeForest.contoso.comm -Name LinkedRoomTest -LinkedCredential $cred -LinkedRoom
   ```

## <a name="option-2-change-an-existing-room-mailbox-to-skype-room-system-linked-resource-mailbox"></a>Option 2: Ändern einer vorhandenen Raumpostfach Skype Raum Systempostfach (verknüpfte) Ressource

```
$cred=Get-Credential AuthForest\LinkedRoomTest1
Set-mailbox -Alias LinkedRoomTest1 -LinkedMasterAccount AuthForest\LinkedRoomTest1 -LinkedDomainController AuthForest-4939.AuthForest.extest.contoso.com -Name LinkedRoomTest1 -LinkedCredential $cred -Identity LinkedRoomTest1

```

