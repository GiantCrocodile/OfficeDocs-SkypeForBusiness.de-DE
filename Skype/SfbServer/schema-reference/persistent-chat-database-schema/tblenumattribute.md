---
title: Enumattribute
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 17f8b87e-36a6-4f6a-8630-7c76b61a7595
description: "\"Enumattribute\" ist eine hardkodierte Tabelle mit den Attributen Visibility und Behavior, die in der Node-Tabelle verwendet werden."
ms.openlocfilehash: 24208b56aba586af500a2f659a2d5cbf1a47234d
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="tblenumattribute"></a>Enumattribute
 
"Enumattribute" ist eine hardkodierte Tabelle mit den Attributen Visibility und Behavior, die in der Node-Tabelle verwendet werden.
  
**Spalten**

|**Spalte**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|attributeID  <br/> |Smallint, nicht null  <br/> |ID des Attributs.  <br/> |
|Attributname  <br/> |Nvarchar (256), nicht null  <br/> |Name des Attributs.  <br/> |
   
**Schlüssel**

|**Spalte**|**Beschreibung**|
|:-----|:-----|
|attributeID  <br/> |Primärschlüssel.  <br/> |
   
**Tabellenwerte**

|**attributeID**|**Attributname**|
|:-----|:-----|
|1  <br/> |Sichtbarkeit.  <br/> |
|2  <br/> |Verhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch

#### 

[tblNode](tblnode.md)
