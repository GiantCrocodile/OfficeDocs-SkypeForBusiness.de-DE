---
title: MediaList-Tabelle
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 7/12/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
description: Die MediaList-Tabelle ist eine statische Tabelle, in der die Liste der verschiedenen Medientypen gespeichert ist.
ms.openlocfilehash: b44a6dd8a4263f50cd187b6c4b154815e1e6350a
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="medialist-table"></a>MediaList-Tabelle
 
Die MediaList-Tabelle ist eine statische Tabelle, in der die Liste der verschiedenen Medientypen gespeichert ist.
  
|**Spalte**|**Datentyp**|**Schlüssel/Index**|**Details**|
|:-----|:-----|:-----|:-----|
|**MediaId** <br/> |tinyint  <br/> |Primary  <br/> |Werte: 1-7  <br/> |
|**Media** <br/> |nvarchar(256)  <br/> || Statische Zuordnung von MediaID- und Media-Werten <br/>  1 – Sofortnachrichten <br/>  2 – Dateiübertragung <br/>  3 – Remoteunterstützung <br/>  4 – Anwendungsfreigabe <br/>  5 – Audio <br/>  6 – Video <br/>  7 – Anwendungseinladung <br/> |
   
Wenn Sie versuchen, den Modalitätstyp für die Werte in LcsCDR.SessionDetailsView.MediaTypes zu bestimmen, müssen Sie das folgende Join-Snippet verwenden:  
  
```
LEFT JOIN on Media.MediaId = MediaList.MediaId
```

