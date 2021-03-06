---
title: Details zur QoE-Ansicht
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
ms.date: 3/9/2015
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: 6a658318-a317-4546-a44c-a9c473d8e86a
description: Ansichten decken die am häufigsten verwendeten Szenarien für die Rückgabe von Daten aus der QoE SQL-Datenbank ab. Es wird empfohlen, Ansichten zum Erstellen benutzerdefinierter Berichte zu verwenden, anstatt direkt auf die Datenbanktabellen zuzugreifen. Das liegt daran, dass Ansichten eher die Abwärtskompatibilität mit zukünftigen Versionen aufrecht erhalten.
ms.openlocfilehash: d207c2cff86c398fed62023b30d193e974cbca7a
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41807173"
---
# <a name="qoe-view-details"></a>Details zur QoE-Ansicht
 
Ansichten decken die am häufigsten verwendeten Szenarien für die Rückgabe von Daten aus der QoE SQL-Datenbank ab. Es wird empfohlen, Ansichten zum Erstellen benutzerdefinierter Berichte zu verwenden, anstatt direkt auf die Datenbanktabellen zuzugreifen. Das liegt daran, dass Ansichten eher die Abwärtskompatibilität mit zukünftigen Versionen aufrecht erhalten.
  
|**Ansichts Name**|**Beschreibung**|
|:-----|:-----|
|[AudioStreamDetail-Ansicht](audiostreamdetail.md) <br/> |Speichert Informationen zu jedem Audiostream in der Datenbank.  <br/> |
|[Medienansicht](medialine.md) <br/> |Speichert Informationen zu jeder medienzeile in der Datenbank. Eine Audiositzung enthält in der Regel eine Audio-medienzeile. Eine Audio-und Video (A/V)-Sitzung enthält in der Regel eine Audio-medienzeile und eine Video medienzeile. die Sitzung kann jedoch zwei Video Medien Linien enthalten, wenn ein Konferenzgerät verwendet wird oder wenn die Katalogansicht verwendet wird.  <br/> |
|[NetworkConfigurationSettings-Ansicht](networkconfigurationsettings.md) <br/> |Speichert Informationen zur Netzwerkkonfiguration.  <br/> |
|[Sitzungsansicht](session-0.md) <br/> |Speichert Informationen zu Sitzungen mit Datensätzen in der Datenbank.  <br/> |
|[UserAgent-Ansicht](useragent-0.md) <br/> |Speichert Informationen zu den Benutzer-Agents, die an Sitzungen teilgenommen haben, die Datensätze in der Datenbank aufweisen.  <br/> |
|[VideoStreamDetail-Ansicht](videostreamdetail.md) <br/> |Speichert Informationen zu jedem Videostream in der Datenbank.  <br/> |
   

