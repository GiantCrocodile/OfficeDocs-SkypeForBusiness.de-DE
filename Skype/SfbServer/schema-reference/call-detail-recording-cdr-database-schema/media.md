---
title: Media-Tabelle
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
description: Jeder Datensatz steht für einen Medientyp in einer Peer-zu-Peer-Sitzung verwendet. Eine Sitzung würde durch mehrere Datensätze in der Tabelle dargestellt werden, wenn mehr als eine Medientyp verwendet wird.
ms.openlocfilehash: 8833e7272c82dcbb7eef0da89d915680198589b5
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="media-table"></a>Media-Tabelle
 
Jeder Datensatz steht für einen Medientyp in einer Peer-zu-Peer-Sitzung verwendet. Eine Sitzung würde durch mehrere Datensätze in der Tabelle dargestellt werden, wenn mehr als eine Medientyp verwendet wird.
  
> [!NOTE]
> Media-Tabelle sollte nicht verwendet werden, um die Dauer Medien für eine Sitzung berechnen. Die folgende Tabelle enthält die Signalisierung Details der Austausch von Mediendaten in einer Sitzung. Austausch von Mediendaten erfolgt durch die INVITE-Anforderung und StartTime gibt die Zeit an, der die INVITE-Nachricht gesendet wurde. Die Zeit einladen bedeutet nicht unbedingt, dass das Medium Startzeit, da Media beginnt erst nach der Sessionee die Sitzung akzeptiert. Die EndTime bedeutet normalerweise die Endzeit der Sitzung. 
  
|**Spalte**|**Datentyp**|**Schlüssel/Index**|**Details**|
|:-----|:-----|:-----|:-----|
|**SessionIdTime** <br/> |datetime  <br/> |Primär, Fremd  <br/> |Zeitpunkt der sitzungsanforderung. Zusammen mit **SessionIdSeq** verwendet zur eindeutigen Identifizierung eine Sitzung. Finden Sie unter der [Dialogs-Tabelle in Skype für Business Server 2015](dialogs.md) Weitere Informationen. <br/> |
|**SessionIdSeq** <br/> |int  <br/> |Primär, Fremd  <br/> |ID-Nummer, um die Sitzung zu identifizieren. In Verbindung mit **SessionIdTime** verwendet, um eine Sitzung eindeutig zu identifizieren. Finden Sie unter der [Dialogs-Tabelle in Skype für Business Server 2015](dialogs.md) Weitere Informationen. <br/> |
|**MediaId** <br/> |tinyint  <br/> |Primär, Fremd  <br/> |Eindeutige Zahl, die diesem Medientyp identifiziert. Finden Sie weitere Informationen die [MediaList-Tabelle](medialist.md) . <br/> |
|**StartTime** <br/> |datetime  <br/> |Primary  <br/> |Hierbei handelt es sich um die Zeit, die eine Media-Anforderung gesendet wurde, nicht die tatsächlichen Medien zu starten. **StartTime** enthält die Dauer der Sitzung. <br/> |
|**EndTime** <br/> |datetime  <br/> ||Dies ist die Endzeit der Sitzung.  <br/> |
   
