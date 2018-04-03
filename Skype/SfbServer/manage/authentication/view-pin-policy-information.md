---
title: Anzeigen von Informationen zu PIN-Richtlinien in Skype for Business Server 2015
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 8/17/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: 1d48b060-d77f-44ee-b70f-3ce128aedac4
description: 'Zusammenfassung: Hier eines Benutzers PIN-Richtlinie für Skype für Business Server 2015.'
ms.openlocfilehash: 3b62dae5cbd29c4622e30c6369a498eb48e126c7
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="view-pin-policy-information-in-skype-for-business-server-2015"></a>Anzeigen von Informationen zu PIN-Richtlinien in Skype for Business Server 2015
 
**Zusammenfassung:** Anzeigen von Informationen eines Benutzers PIN-Richtlinie für Skype für Business Server 2015.
  
Sie können die Registerkarte **PIN-Richtlinie** , um Ansicht personal Identification Number (PIN) Authentifizierung von Benutzern, die Skype für Unternehmen mit IP-Telefone verbunden sind. Stellen Sie zur Verwendung der PIN-Authentifizierung sicher, dass in den Webdiensteinstellungen die Option **PIN-Authentifizierung aktivieren** ausgewählt ist.
  
Führen Sie die folgenden Schritte aus, um eine PIN-Richtlinie auf Benutzer- oder Standortebene zu ändern. 
  
### <a name="to-view-information-about-a-pin-policy-in-skype-for-business-server-control-panel"></a>Zum Anzeigen von Informationen über eine PIN-Richtlinie in Skype Business Server-Systemsteuerung

1.  Von einem Benutzerkonto, das Mitglied der Gruppe RTCUniversalServerAdmins (oder gleichwertige Benutzerrechte verfügt), oder der CsServerAdministrator oder CsAdministrator-Rolle, melden Sie sich an einem beliebigen Computer, die im Netzwerk ist in der Bereitstellung von Skype für Business Server zugeordnet ist 2015.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen.  
    
3. Klicken Sie in der linken Navigationsleiste auf **Sicherheit** und dann auf **PIN-Richtlinie**.
    
4. Klicken Sie auf der Seite **PIN-Richtlinie** auf eine Richtlinie, klicken Sie auf **Bearbeiten** und dann auf **Details anzeigen**.
    
## <a name="viewing-pin-policies-by-using-windows-powershell-cmdlets"></a>Anzeigen von PIN-Richtlinien mithilfe von Windows PowerShell-Cmdlets

Sie können auch PIN-Richtlinien mithilfe von Windows PowerShell und das Cmdlet Get-CsPinPolicy anzeigen. Dieses Cmdlet kann von der Skype für Business Server-Verwaltungsshell oder von einer remote Windows PowerShell-Sitzung ausgeführt werden. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-view-pin-policies"></a>So zeigen Sie PIN-Richtlinien an

Anzeigen von Informationen zu allen PIN-Richtlinien, geben Sie den folgenden Befehl in der Skype für Business Server-Verwaltungsshell, und drücken Sie die EINGABETASTE:
    
  ```
  Get-CsPinPolicy
  ```

Es werden etwa folgende Informationen zurückgegeben:

  ```
  Identity             : Global
Description          :
MinPasswordLength    : 5
PINHistoryCount      : 0
AllowCommonPatterns  : False
PINLifetime          : 0
MaximumLogonAttempts :
  ```

Weitere Informationen finden Sie im Hilfethema für das Cmdlet [Get-CsPinPolicy](https://docs.microsoft.com/powershell/module/skype/get-cspinpolicy?view=skype-ps) .
  
## <a name="see-also"></a>Siehe auch

#### 

[Erstellen einer neuen PIN-Richtlinie in Skype für Business Server 2015](create-a-new-pin-policy.md)
