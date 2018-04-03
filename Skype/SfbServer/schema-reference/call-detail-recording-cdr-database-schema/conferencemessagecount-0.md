---
title: ConferenceMessageCount-Ansicht
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
description: Die ConferenceMessageCount-Ansicht speichert Informationen über wie viele Nachrichten von einem Benutzer an einer Konferenz gesendet wurden. Diese Ansicht wurde in Microsoft Lync Server 2013 eingeführt.
ms.openlocfilehash: f0206145217f63e4530d2eac39c7c6533dcf154e
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="conferencemessagecount-view"></a>ConferenceMessageCount-Ansicht
 
Die ConferenceMessageCount-Ansicht speichert Informationen über wie viele Nachrichten von einem Benutzer an einer Konferenz gesendet wurden. Diese Ansicht wurde in Microsoft Lync Server 2013 eingeführt.
  
> [!NOTE]
> Die ConferenceMessageCount-Ansicht enthält alle Spalten in der [ConferenceSessionDetails-Ansicht](conferencesessiondetails.md) außerdem die unten aufgeführten Spalten.
  
|**Spalte**|**Datentyp**|**Details**|
|:-----|:-----|:-----|
|**UserUri** <br/> |nvarchar(450)  <br/> |Der URI des Benutzers, der die Nachricht gesendet hat.  <br/> |
|**UserUriType** <br/> |nvarchar(256)  <br/> |Typ der URI des Benutzers, der die Nachrichten gesendet. Finden Sie weitere Informationen der [UriTypes-Tabelle](uritypes.md) . <br/> |
|**UserTenant** <br/> |uniqueidentifier  <br/> |Mandant des Benutzers, die die Nachrichten gesendet hat. Finden Sie weitere Informationen der [Tenants-Tabelle](tenants.md) . <br/> |
|**UserMessageCount** <br/> |smallint  <br/> |Anzahl der vom Benutzer während der Sitzung gesendeten Nachrichten.  <br/> |
   
