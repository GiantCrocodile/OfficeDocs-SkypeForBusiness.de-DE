---
title: in "tblscopeprincipal"
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 422d6c7f-7ba7-4dd4-bacc-95ace47959ff
description: in "tblscopeprincipal" enthält die Bereiche, die Knoten zugewiesen.
ms.openlocfilehash: ba2927598cdff07368cb017866ec41bfa7540f48
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="tblscopeprincipal"></a>in "tblscopeprincipal"
 
in "tblscopeprincipal" enthält die Bereiche, die Knoten zugewiesen.
  
**Spalten**

|**Spalte**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|scopeNodeID  <br/> |Int, nicht null  <br/> |Knoten-ID, die auf der Bereich angewendet wird.  <br/> |
|scopePrinID  <br/> |Int, nicht null  <br/> |Prinzipal-ID.  <br/> |
|scopeIsDenied  <br/> |Bit, nicht null  <br/> |True, wenn Bereichstyp verweigern. False, wenn ermöglichen.  <br/> |
|scopeUpdatedBy  <br/> |Int, nicht null  <br/> |ID des Prinzipals, der diesen Eintrag zuletzt aktualisiert.  <br/> |
   
**Schlüssel**

|**Spalte**|**Beschreibung**|
|:-----|:-----|
|\<ScopeNodeID scopePrinID\>  <br/> |Primärschlüssel.  <br/> |
|scopeNodeID  <br/> |Fremdschlüssel mit Abfrage der tblNode.nodeID-Tabelle.  <br/> |
|scopePrinID  <br/> |Fremdschlüssel mit Abfrage der tblPrincipal.prinID-Tabelle.  <br/> |
   
