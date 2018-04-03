---
title: Konfigurieren von Archivierungshaftungsausschlüssen für externe Benutzer in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 394ac291-05cd-4fa1-acb3-714af538b47f
description: 'Zusammenfassung: Lesen Sie dieses Thema, um Informationen zum Konfigurieren eines Archivierungshaftungsausschlusses für Skype für Business Server 2015.'
ms.openlocfilehash: 3790160024010084c69df7d9865f17622fca4f0d
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="configure-archiving-disclaimers-for-external-users-in-skype-for-business-server-2015"></a>Konfigurieren von Archivierungshaftungsausschlüssen für externe Benutzer in Skype for Business Server 2015
 
**Zusammenfassung:** Lesen Sie dieses Thema, um Informationen zum Konfigurieren eines Archivierungshaftungsausschlusses für Skype für Business Server 2015.
  
Wenn Ihre Organisation mit externen Partnern kommuniziert, müssen Sie die Partner darüber informieren, dass diese Kommunikationen archiviert werden. Wenn Sie einen Edge-Server bereitstellen und Föderation für Ihre Organisation zu aktivieren, werden Sie gefragt, ob Sie automatisch ein Archivierungshaftungsausschlusses an externe Partner senden möchten. 
  
Wenn Sie diese Konfiguration ändern müssen, können Sie die Skype für Business Server-Systemsteuerung oder Windows PowerShell **Set-CsAccessEdgeConfiguration** -Cmdlet verwenden. Cmdlets für kann entweder von der Skype für Business Server-Verwaltungsshell oder von einer remote Windows PowerShell-Sitzung ausgeführt werden.
  
Um externe Benutzer für die Zusammenarbeit mit Benutzern in Ihrer Skype für Business Server-Bereitstellung zu aktivieren, müssen Sie auch mindestens eine externe Zugriffsrichtlinie zur Unterstützung der Zugriff durch externe Benutzer konfigurieren. Weitere Informationen hierzu finden Sie unter Verwalten von XMPP-Verbundpartner für Ihre Organisation. Ausführliche Informationen zur Steuerung des Zugriffs für bestimmte Partnerdomänen finden Sie unter „Control Access by Individual Federated Domains“.
  
## <a name="enable-or-disable-archiving-disclaimer-using-the-control-panel"></a>Aktivieren oder Deaktivieren des Archivierungshaftungsausschlusses mithilfe der Systemsteuerung

1. Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen. 
    
3. Klicken Sie in der linken Navigationsleiste auf **Partnerverbund und externer Zugriff** und dann auf **Zugriffs-Edgekonfiguration**.
    
4. Klicken Sie auf der Registerkarte **Zugriffs-Edgekonfiguration** auf **Global**, klicken Sie auf **Bearbeiten** und dann auf **Details einblenden**.
    
5. Aktivieren oder deaktivieren Sie im Abschnitt **Zugriffs-Edgekonfiguration bearbeiten** unter **Partnerverbund und Verbindung mit öffentlichen Chatdiensten aktivieren** das Kontrollkästchen **Archivierungshaftungsausschluss an Verbundpartner senden**, um das automatische Versenden eines Archivierungshaftungsausschlusses zu aktivieren bzw. zu deaktivieren.
    
6. Klicken Sie auf **Commit ausführen**.
    
## <a name="enable-or-disable-archiving-disclaimer-using-windows-powershell"></a>Aktivieren oder Deaktivieren des Archivierungshaftungsausschlusses mithilfe von Windows PowerShell

Zum Aktivieren des Archivierungshaftungsausschlusses legen Sie den Wert der Eigenschaft **EnableArchivingDisclaimer** auf „True“ ($True) fest:
  
```
Set-CsAccessEdgeConfiguration -EnableArchivingDisclaimer $True
```

Zum Deaktivieren des Archivierungshaftungsausschlusses legen Sie den Wert der Eigenschaft **EnableArchivingDisclaimer** auf „False“ ($False) fest:
  
```
Set-CsAccessEdgeConfiguration -EnableArchivingDisclaimer $False
```

