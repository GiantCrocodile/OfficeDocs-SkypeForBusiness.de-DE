---
title: Beispieldatenbankabfragen für beständigen Chat
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 545b1a93-9758-4344-98cc-aa0e559d494f
description: Dieser Abschnitt enthält Beispielabfragen für die Datenbank für beständigen Chat.
ms.openlocfilehash: 1e2d457a31061dcfb3c332a067069cbd4a8a9ebd
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="sample-persistent-chat-database-queries"></a>Beispieldatenbankabfragen für beständigen Chat
 
Dieser Abschnitt enthält Beispielabfragen für die Datenbank für beständigen Chat.
  
Mithilfe des folgenden Beispiels können Sie eine Liste der aktivsten beständigen Chat Rooms nach einem bestimmten Datum abrufen.
  
```
SELECT nodeName as ChatRoom, COUNT(*) as ChatMessages
  FROM tblChat, tblNode
  WHERE channelId = nodeID AND dbo.fnTicksToDate(chatDate) > '1/1/2011'
  GROUP BY nodeName
  ORDER BY ChatMessages DESC

```

Verwenden Sie das folgende Beispiel, um eine Liste der aktivsten Benutzer nach einem bestimmten Datum abrufen.
  
```
SELECT prinName as Name, count(*) as ChatMessages
  FROM tblChat, tblPrincipal
  WHERE prinID = userId AND dbo.fnTicksToDate(chatDate) > '1/1/2011'
  GROUP BY prinName
  ORDER BY ChatMessages DESC

```

Verwenden Sie das folgende Beispiel zum Abrufen einer Liste aller Benutzer, die jemals eine Nachricht mit "Hello World" gesendet.
  
```
SELECT nodeName as ChatRoom, prinName as Name, content as Message
  FROM tblChat, tblNode, tblPrincipal
  WHERE channelId = nodeID AND userId = prinID AND content like '%Hello World%'
```

Verwenden Sie das folgende Beispiel, um eine Liste der Gruppenmitgliedschaften für einen bestimmten Prinzipal abrufen.
  
```
SELECT prinName as Name    
  FROM tblPrincipalAffiliations as pa, tblPrincipal
  where principalID = 7 and affiliationID = prinID
```

Verwenden Sie im folgenden Beispiel wird eine Liste aller Chatrooms abrufen, die ein Benutzer, Jane Dow, direktes Mitglied ist.
  
```
SELECT DISTINCT nodeName as ChatRoom, prinName as Name          
  FROM tblPrincipalRole, tblPrincipal, tblNode
  WHERE  prinRoleNodeID = nodeID AND prinRolePrinID = prinID AND prinName = 'Jane Dow'
```

Verwenden Sie im folgenden Beispiel wird eine Liste von Einladungen abrufen, die ein Benutzer erhalten hat.
  
```
SELECT prinName
      ,nodeName
      ,invID   
      ,createdOn
  FROM tblPrincipalInvites as inv, tblPrincipal as p, tblNode as n
  where inv.prinID = 5 AND inv.prinID = p.prinID and inv.nodeID = n.nodeID
  ORDER BY invID DESC
```

