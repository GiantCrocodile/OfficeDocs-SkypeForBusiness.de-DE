---
title: Suche CcLog
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.date: 3/20/2017
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: bbae05f9-d8de-40dc-8968-d225dcde80e4
description: Das Cmdlet „Search-CcLog“ durchsucht die Listen für ein- und ausgehende Anrufe im Protokollverzeichnis der Skype for Business Cloud Connector Edition-Appliance.
ms.openlocfilehash: 3d7d34f2e069b9c4ed728dcc805af5ccf9d13067
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="search-cclog"></a>Suche CcLog
 
Das Cmdlet „Search-CcLog“ durchsucht die Listen für ein- und ausgehende Anrufe im Protokollverzeichnis der Skype for Business Cloud Connector Edition-Appliance.
  
```
Search-CcLog [[-StartTime] <datetime>] [[-EndTime] <datetime>] [[-FileName] <string>]
```

## <a name="examples"></a>Beispiele
<a name="Examples"> </a>

### <a name="example-1"></a>Beispiel 1

Im folgenden Beispiel werden die Listen für ein- und ausgehende Anrufe im Protokollverzeichnis der Appliance mithilfe des Standarddateinamens durchsucht:
  
```
Search-CcLog -StartTime "8/31/2012 8:00AM" -EndTime "8/31/2012 6:00PM"
```

### <a name="example-2"></a>Beispiel 2

Im nächsten Beispiel werden die Listen für ein- und ausgehende Anrufe mithilfe des angegebenen Dateipfads und Namens durchsucht:
  
```
Search-CcLog -StartTime "8/31/2012 8:00AM" -EndTime "8/31/2012 6:00PM" -FileName "C:\Log\LogFile.log"
```

## <a name="detailed-description"></a>Detaillierte Beschreibung
<a name="DetailedDescription"> </a>

Das Cmdlet  Search-CsClsLogging bietet eine Befehlszeilenoption zum Durchsuchen der vom zentralisierten Protokollierungsdienst erstellten Protokolldateien.
  
## <a name="parameters"></a>Parameter
<a name="DetailedDescription"> </a>

|**Parameter**|**Erforderlich**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|StartTime  <br/> | Erforderlich <br/> |System.Datetime  <br/> |  Anfangszeitpunkt (Datum und Uhrzeit) für die zu durchsuchenden Protokolleinträge. Wird in der lokalen Zeitzone angegeben. <br/> |
|EndTime  <br/> |Erforderlich  <br/> |System.Datetime  <br/> |Endzeitpunkt (Datum und Uhrzeit) für die zu durchsuchenden Protokolleinträge. Wird in der lokalen Zeitzone angegeben.  <br/> |
|Dateiname  <br/> |Erforderlich  <br/> |System.String  <br/> |Gibt den vollständigen Pfad der Textdatei mit den Suchergebnissen an.  <br/> |
   
## <a name="input-types"></a>Eingabetypen
<a name="InputTypes"> </a>

Keine. Das Cmdlet „Search-CcLog“ akzeptiert keine Pipelineeingaben.
  
## <a name="return-types"></a>Rückgabetypen
<a name="ReturnTypes"> </a>

Keine
  
## <a name="see-also"></a>Siehe auch
<a name="ReturnTypes"> </a>

[Start-CcLogging](start-cclogging.md)
  
[Stop-CcLogging](stop-cclogging.md)
  
