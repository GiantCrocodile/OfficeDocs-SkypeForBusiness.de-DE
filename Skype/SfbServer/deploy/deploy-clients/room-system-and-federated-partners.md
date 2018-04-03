---
title: Skype Room System- und Skype for Business-Verbundpartner
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/4/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 1cc20323-ecba-4e87-a861-e54193e64cf0
description: Lesen Sie dieses Thema, um zu erfahren, wie Sie Skype Room System für Skype for Business-Verbundpartner einrichten.
ms.openlocfilehash: 040af495217217b3bfd10fb577b7194df354e027
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="skype-room-system-and-skype-for-business-federated-partners"></a>Skype Room System- und Skype for Business-Verbundpartner
 
Lesen Sie dieses Thema, um zu erfahren, wie Sie Skype Room System für Skype for Business-Verbundpartner einrichten.
  
## <a name="skype-room-system-and-skype-for-business-federated-partners"></a>Skype Room System- und Skype for Business-Verbundpartner

Skype Raum System nutzt die Teilnahme Skype für Business besprechungslink in der Besprechungsanfrage Kalender. Der Link für die Teilnahme ist normalerweise im Textkörper der Besprechungsanfrage zu finden. Skype Raum System hängt jedoch diesen Link, um in die MAPI-Eigenschaften der Nachricht vorhanden sein. Wenn diese Besprechungsanfrage werden an remote Organisationen (Skype für Geschäftspartner federated), standardmäßig gesendet die Remoteorganisation Skype Raum System wird nicht angezeigt, die die Teilnahme an einer Besprechung im Kalender zu verknüpfen. Tatsächlich Outlook-Benutzer, die in der Remoteorganisation nicht an die Skype für Business-Besprechung mit einem Klick rechts des Kalenders item oder aus teilnehmen können innerhalb einer besprechungserinnerung. Sie öffnen Besprechung einladen, und klicken Sie auf teilnehmen Skype für Business Besprechung im Textkörper der Nachricht. 
  
Der Grund für dieses Einschränkung ist, dass Outlook und Microsoft Exchange keine spezielle Methode dafür kennen, Informationen für den Versand von Nachrichten über das Internet mit einzuschließen. Diese Methode, die als „Transport Neutral Encapsulation Format“ (TNEF) bezeichnet wird, ist für Nachrichten, die aus einem Exchange-Unternehmen extern versendet werden, standardmäßig deaktiviert. Für eine Besprechung teilnehmen Hyperlink einfügen auf einem Skype Raum Remotesystem, muss die sendende Organisation TNEF mithilfe des folgenden Befehls aktivieren:
  
```
New-RemoteDomain -DomainName Contoso.com -Name Contoso
Set-RemoteDomain -Identity Contoso -TNEFEnabled $true
```

Nachdem TNEF für das Remote-Unternehmen aktiviert worden ist, wird jede über das Internet an das Unternehmen gesendete Nachricht als Anlage im TNEF-Format geschickt. Mit TNEF aktiviert Wenn eine Skype für wird Business Besprechungsanfrage gesendet, der Skype für Verbundpartner Business, Skype Raum System sind in der Lage, die Verknüpfung Skype für Business Besprechung Rendern und Remotebenutzer können Skype für Business-Besprechungen teilnehmen. 