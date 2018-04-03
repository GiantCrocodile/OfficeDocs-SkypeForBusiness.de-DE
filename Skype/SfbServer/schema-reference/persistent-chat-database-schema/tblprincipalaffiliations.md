---
title: tblPrincipalAffiliations
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 45fd8484-5837-44d2-85bb-45c83546607c
description: TblPrincipalAffiliations enthält die prinzipalzuordnungen, die Mitgliedschaften in Standorten, einschließlich Active Directory-Domänendienste-Sicherheitsgruppen, in Active Directory-Containern und in Domänen beschreiben.
ms.openlocfilehash: 4e5529590a6a636c28c801392953c7fd69e9f649
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="tblprincipalaffiliations"></a>tblPrincipalAffiliations
 
TblPrincipalAffiliations enthält die prinzipalzuordnungen, die Mitgliedschaften in Standorten, einschließlich Active Directory-Domänendienste-Sicherheitsgruppen, in Active Directory-Containern und in Domänen beschreiben.
  
**Spalten**

|**Spalte**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|principalID  <br/> |Int, nicht null  <br/> |Die ID des zugeordneten Prinzipals.  <br/> |
|affiliationID  <br/> |Int, nicht null  <br/> |ID des Prinzipals, der die Zuordnung darstellt. Jedes Sicherheitsprinzipal (mit Ausnahme der System-Benutzer-Typen) hat ein Self Zugehörigkeit sowie.  <br/> |
|Index  <br/> |Int, nicht null  <br/> |Index. Der Wert für Self zugehörigkeiten ist-1, und für die anderen zugehörigkeiten erhöht sequenziell von 1 innerhalb der einzelnen \<PrincipalID AffiliationId\> Bucket.  <br/> |
|updatedBy  <br/> |Int, nicht null  <br/> |Prinzipal, die das neueste Update haben. Dies ist in der Regel 1 fest, was bedeutet, Active Directory-Synchronisierung dass.  <br/> |
   
**Schlüssel**

|**Spalten**|**Beschreibung**|
|:-----|:-----|
|\<PrincipalID, Index, affiliationID\>  <br/> |Primärschlüssel.  <br/> |
|principalID  <br/> |Fremdschlüssel mit Abfrage der tblPrincipal.prinID-Tabelle.  <br/> |
|affiliationID  <br/> |Fremdschlüssel mit Abfrage der tblPrincipal.prinID-Tabelle.  <br/> |
   
