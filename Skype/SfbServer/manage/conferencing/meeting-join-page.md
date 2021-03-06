---
title: Konfigurieren der Seite "Besprechungsteilnahme" in Skype for Business Server
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
ms.assetid: 6537765e-4384-416f-92f1-a7f3b39ebe56
description: 'Zusammenfassung: Hier erfahren Sie, wie Sie die Seite "Besprechungsteilnahme" in Skype for Business Server konfigurieren.'
ms.openlocfilehash: 7381db4983b5a2c1ec6dccf474f0b381e079e222
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41818516"
---
# <a name="configure-the-meeting-join-page-in-skype-for-business-server"></a>Konfigurieren der Seite "Besprechungsteilnahme" in Skype for Business Server
 
**Zusammenfassung:** Hier erfahren Sie, wie Sie die Seite "Besprechungsteilnahme" in Skype for Business Server konfigurieren.
  
Wenn ein Benutzer in einer Besprechungsanfrage auf einen Besprechungslink klickt, erkennt die Seite "Besprechungsteilnahme", ob ein Skype for Business-Client bereits auf dem Computer des Benutzers installiert ist. Wenn ein Client bereits installiert ist, wird der Client geöffnet und der Besprechung beitreten. Wenn ein Client nicht installiert ist, wird standardmäßig der Skype for Business-Client geöffnet. 
  
## <a name="configure-the-meeting-join-page"></a>Konfigurieren der Seite für den Besprechungsbeitritt

Sie können das Verhalten der Seite "Besprechungsteilnahme" ändern, wenn Sie Benutzern die Teilnahme an Besprechungen mit anderen Versionen des Clients gestatten möchten. Diese Konfigurationsoptionen wurden aus der Skype for Business Server-Systemsteuerung entfernt, aber Sie werden mithilfe des Cmdlets "festlegen-CsWebServiceConfiguration" konfiguriert.
  
**Seitensatz "Besprechungsteilnahme" – CsWebServiceConfiguration-Parameter**

|**Satz-CsWebServiceConfiguration-Parameter**|**Beschreibung**|
|:-----|:-----|
|ShowJoinUsingLegacyClientLink  <br/> |Dieser Parameter wurde für die Verwendung mit der lokalen Version von Skype for Business Server als veraltet markiert.  <br/> Wenn die Einstellung auf "true" festgelegt ist, können Benutzer, die mit einer anderen Clientanwendung als Skype for Business an einer Besprechung teilnehmen, die Möglichkeit erhalten, an der Besprechung teilzunehmen, indem Sie Ihre aktuelle Clientanwendung verwenden. Der Standardwert lautet "False".  <br/> |
|ShowAlternateJoinOptionsExpanded  <br/> |Dieser Parameter wurde für die Verwendung mit der lokalen Version von Skype for Business Server als veraltet markiert.  <br/>  Wenn diese Option auf "true" festgelegt ist, werden die Alternativen für den Beitritt zu einer Onlinekonferenz automatisch erweitert und Benutzern angezeigt. Wenn auf "false" (der Standardwert) festgelegt ist, stehen diese Optionen zur Verfügung, aber der Benutzer muss die Liste der Optionen für sich selbst anzeigen.  <br/> |
   

