---
title: Element abrufen
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 8/18/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: e77bf649-d62a-4d94-80de-066ba47730cd
description: 'Zusammenfassung: Informationen Sie zum Vorgang Element abrufen, der Teil der Element-Dienst ist. Der Element-Dienst ist Teil der Repository-API für die Qualitätsdashboard aufrufen. Das Anrufqualitäts-Dashboard ist ein Tool für Skype for Business Server 2015.'
ms.openlocfilehash: 6e4ba82c804937025b72da2d443c2a828d92d98a
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="get-item"></a>Element abrufen
 
**Zusammenfassung:** Informationen Sie zum Vorgang Element abrufen, der Teil der Element-Dienst ist. Der Element-Dienst ist Teil der Repository-API für die Qualitätsdashboard aufrufen. Das Anrufqualitäts-Dashboard ist ein Tool für Skype for Business Server 2015.
  
Der Vorgang Element abrufen ist Teil des Diensts Element in der Repository-API für die Qualitätsdashboard aufrufen.
  
## <a name="get-item"></a>Element abrufen

Rufen Sie gibt ein bestimmtes Element im Repository.
  
|**Methode**|**Anforderungs-URI**|**HTTP-Version**|
|:-----|:-----|:-----|
|Erhalten  <br/> |https://\<Portal\>/QoERepositoryService/Repository/Element / {ItemId}  <br/> |HTTP/1.1  <br/> |
   
 **URI-Parameter** - None.
  
 **Anfordern von Kopfzeilen** - keine zusätzlichen Header.
  
 **Anforderungstextkörper** – None.
  
 **Antwort** - die Antwort enthält einen HTTP-Statuscode und einen Satz von Antwortheader.
  
 **Statuscode** - eine erfolgreiche Ausführung Gibt Statuscode 200 (OK). Wenn eine angegebenes Element-ID nicht gefunden wird, wird der Statuscode 404 (nicht gefunden) zurückgegeben.
  
 **Antwortheader** - keine zusätzlichen Header.
  
 **Antworttext** - ist im folgenden Beispiel Antwort Nutzlast in JSON.
  
```
{
"itemId": 1652,
"userId": 0,
"content": "{\"Title\":\"All Audio Streams\",...}",
"type": "application/json",
"subItemIds": [1653, 1710]
}

```

 *ItemId* - ID des Elements.
  
 *UserId* - ID des Benutzers, der dieses Element gehört.
  
 *Content* - anwendungsspezifischen-Inhalt.
  
 *Typ* – der Typ des Inhalts. Dieses Feld wird durch die Anwendung festgelegt.
  
 *SubItemIds* - die IDs der untergeordneten Elemente, sofern vorhanden. Hierbei handelt es sich um einen Kurzschluss des Vorgangs untergeordnete Elemente abrufen, um einen Anruf zu speichern. Anwendungen können alternativ mit untergeordneten Elemente abrufen-Operation dieselbe Informationen abrufen.
  
