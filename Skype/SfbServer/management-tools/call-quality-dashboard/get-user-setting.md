---
title: Abrufen einer Benutzereinstellung
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: 16611a55-79fb-487a-a936-20caca829f87
description: 'Zusammenfassung: erfahren Sie mehr über den Vorgang zum Abrufen der Benutzereinstellung, der Teil des Benutzer Einstellungs Diensts ist. Der Benutzer Einstellungsdienst ist Teil der Repository-API für das Anruf Qualitäts Dashboard. Das Dashboard für die Anrufqualität ist ein Tool für Skype for Business Server.'
ms.openlocfilehash: 4ab9d4d718a2ff411db72f38b59a758523935504
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41816754"
---
# <a name="get-user-setting"></a>Abrufen einer Benutzereinstellung
 
**Zusammenfassung:** Informieren Sie sich über den Vorgang zum Abrufen der Benutzereinstellung, der Teil des Benutzer Einstellungs Diensts ist. Der Benutzer Einstellungsdienst ist Teil der Repository-API für das Anruf Qualitäts Dashboard. Das Dashboard für die Anrufqualität ist ein Tool für Skype for Business Server.
  
Der Vorgang zum Abrufen der Benutzereinstellung ist Teil des Benutzer Einstellungs Diensts in der Repository-API für das Dashboard für die Anrufqualität.
  
## <a name="get-user-setting"></a>Abrufen einer Benutzereinstellung

Benutzereinstellung abrufen gibt eine Einstellung für einen einzelnen Benutzer zurück.
  

|**Methode**|**Anforderungs-URI**|**HTTP-Version**|
|:-----|:-----|:-----|
|Erhalten  <br/> |https://\<-\>Portal/QoERepositoryService/Repository/User/{UserID}/Setting/{Key}  <br/> |HTTP/1.1  <br/> |
   
 **URI-Parameter** -None.
  
 **Anforderungs Kopfzeilen** – keine zusätzlichen Überschriften.
  
 **Anforderungstext** – keine.
  
 **Antwort** – die Antwort enthält einen HTTP-Statuscode und einen Satz von Antwortheadern.
  
 **Statuscode** – ein erfolgreicher Vorgang gibt den Statuscode 200 (OK) zurück.
  
 **Antwortheader** – keine zusätzlichen Überschriften.
  
 **Antworttext** : Nachfolgend finden Sie eine Beispielantwort Nutzlast in JSON.
  
```json
{
"userId": 6,
"key": "ShowDescriptions",
"value": "true"
}
```

 *UserID* -ID des Benutzers.
  
 *Tasten* Kombination der Einstellung.
  
 *value* -Wert der Einstellung.
  

