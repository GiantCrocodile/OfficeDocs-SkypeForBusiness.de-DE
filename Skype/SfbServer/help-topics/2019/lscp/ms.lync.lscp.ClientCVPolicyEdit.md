---
title: Clientversionsrichtlinie Erstellen einer neuen oder Bearbeiten einer vorhandenen
ms.author: laurawi
author: LauraWi
manager: serdars
ms.date: 3/23/2015
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.lscp.ClientCVPolicyEdit
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: e32c6712-6dc9-4de9-8d74-9fdccf3de1ba
description: Sie können die Versionen von Clients angeben, die in Ihrer Umgebung unterstützt werden sollen. Wenn zwei Clients unterschiedlicher Versionen interagieren, können die für einen der Clients verfügbaren Funktionen durch die Funktionen des anderen Clients eingeschränkt werden. Die größte Nutzung der Features in Skype für Business Server 2015 und zur Verbesserung der benutzerfreundlichkeit können den clientversionsfilter Sie um die Clientversionen, die verwendet werden in Ihrer Umgebung zu beschränken. Mit dem Clientversionsfilter können Sie außerdem die Kosten senken, die aufgrund der Unterstützung mehrerer Clientversionen anfallen.
ms.openlocfilehash: 6c1e895dc03d094013f41a34cb21a12a24928172
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="client-version-policy-create-new-or-edit-existing"></a>Clientversionsrichtlinie: Erstellen einer neuen oder Bearbeiten einer vorhandenen Clientversionsrichtlinie
 
Sie können die Versionen von Clients angeben, die in Ihrer Umgebung unterstützt werden sollen. Wenn zwei Clients unterschiedlicher Versionen interagieren, können die für einen der Clients verfügbaren Funktionen durch die Funktionen des anderen Clients eingeschränkt werden. Die größte Nutzung der Features in Skype für Business Server 2015 und zur Verbesserung der benutzerfreundlichkeit können den clientversionsfilter Sie um die Clientversionen, die verwendet werden in Ihrer Umgebung zu beschränken. Mit dem Clientversionsfilter können Sie außerdem die Kosten senken, die aufgrund der Unterstützung mehrerer Clientversionen anfallen.
  
> [!IMPORTANT]
> Filter werden anhand ihrer Rangfolge aufgelistet. Beispiel: Sie verfügen über einen Filter, der die Ausführung von Clientversion 1.5 zulässt, gefolgt von einem Filter, der Clients mit früheren Versionen als Version 2.0 blockiert. In diesem Fall hat der erste Filter Vorrang und Clients mit Version 1.5 können eine Verbindung herstellen. 
  
## <a name="tasks-you-can-perform"></a>Mögliche Aufgaben

Auf der Seite **Neue Clientversionsrichtlinie** bzw. **Clientversionsrichtlinie bearbeiten** können Sie die folgenden Aufgaben ausführen:
  
- Hinzufügen oder Ändern des Namens oder der Beschreibung der Clientversionsrichtlinie
    
- Hinzufügen oder Ändern der Clientversionsregeln für die Clientversionsrichtlinie
    
## <a name="ui-reference"></a>Referenz zur Benutzeroberfläche

In den folgenden Listen werden die Menüs, Befehle, Felder und Eigenschaften der Seite beschrieben.
  
- **Bereich** Gibt den Bereich (Standort, Pool oder Benutzer) der clientversionsrichtlinie an.
    
- **Name** Sie können hinzufügen oder Ändern des Namens der clientversionsrichtlinie.
    
- **Beschreibung** Sie können eine Beschreibung, die Hilfe bei der Identifizierung der Richtlinie in der Liste auf der Seite Clientversionsrichtlinie hinzufügen.
    
- **Neue** Sie können die Richtlinie eine neue clientversionsregel hinzufügen.
    
- **Details anzeigen** Diese Option öffnet ein Dialogfeld, in dem Sie die Optionen für eine clientversionsregel ändern können.
    
- **Entfernen** Diese Option wird die ausgewählte clientversionsregel aus der Richtlinie entfernt.
    
- **Weisenden Pfeile** Diese Option wird die ausgewählte clientversionsregel nach oben oder unten im Feld Priorität verschoben. Die Regeln werden in der angezeigten Reihenfolge verarbeitet.
    
Ausführliche Informationen zur Interoperabilität zwischen Clients und Clientversionen finden Sie unter [Client Interoperability in Lync 2013 Preview](http://technet.microsoft.com/library/0f126571-91a2-45d5-855c-1e4ddb45fc04.aspx) in der Planungsdokumentation. Ausführliche Informationen zur Verwendung von clientversionsrichtlinien finden Sie unter [Specify the Client Versions Supported in Your Organization](http://technet.microsoft.com/library/d256a581-9a48-4d1a-82cc-2e1f520d7d2e.aspx) in der Betriebsdokumentation.
