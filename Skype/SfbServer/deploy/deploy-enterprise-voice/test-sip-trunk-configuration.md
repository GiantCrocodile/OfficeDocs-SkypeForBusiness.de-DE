---
title: Testen der SIP-Trunk-Konfigurationseinstellungen in Skype for Business Server
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: quickstart
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.collection:
- IT_Skype16
- Strat_SB_Admin
ms.custom: ''
ms.assetid: c8712308-0e2d-4e39-8f90-d1a250487a94
description: 'Zusammenfassung: Hier erfahren Sie, wie Sie die SIP-Trunk-Konfigurationseinstellungen mithilfe der Skype for Business Server-Verwaltungsshell testen.'
ms.openlocfilehash: a85af538f5729310c75e57313b049dcb14d09542
ms.sourcegitcommit: dd3a3ab4ddbdcfe772f30fb01ba3b97c45c43dd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "41766908"
---
# <a name="test-sip-trunk-configuration-settings-in-skype-for-business-server"></a>Testen der SIP-Trunk-Konfigurationseinstellungen in Skype for Business Server
 
**Zusammenfassung:** Erfahren Sie, wie Sie die SIP-Trunk-Konfigurationseinstellungen mithilfe der Skype for Business Server-Verwaltungsshell testen können.
  
SIP-Trunk-Konfigurationseinstellungen definieren die Beziehung und die Funktionen zwischen einem Vermittlungsserver und dem PSTN-Gateway (Public Switched Telephone Network, Festnetz), einer IP-Nebenstellenanlage (Public Branch Exchange, PBX) oder einem Session Border Controller (SBC) beim Dienstanbieter. Diese Einstellungen geben unter anderem Folgendes an:
  
- Ob Medienumgehung für die Trunks aktiviert werden soll.
    
- Die Bedingungen, unter denen RTCP-Pakete (Real-Time Transport Control Protocol) gesendet werden.
    
- Ob SRTP-Verschlüsselung (Secure Real-Time Protocol) für jeden Trunk erforderlich ist.
    
Wenn Sie Skype for Business Server installieren, wird eine globale Sammlung von SIP-Trunk-Konfigurationseinstellungen für Sie erstellt. Darüber hinaus können Administratoren benutzerdefinierte Auflistungen mit Einstellungen auf Standort- oder Dienstebene erstellen (nur für den PSTN-Gatewaydienst). Administratoren können außerdem mit dem Test-CsTrunkConfiguration-Cmdlet überprüfen, ob ein Trunk eine von einem Benutzer gewählte Rufnummer in eine für das Gateway kompatible Rufnummer konvertieren kann.
  
Trunk-Konfigurationseinstellungen können nur mit Windows PowerShell und dem [Test-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/test-cstrunkconfiguration?view=skype-ps)-Cmdlet. Dieses Cmdlet kann entweder über die Skype for Business Server-Verwaltungsshell oder über eine Remotesitzung der Skype for Business Server-Verwaltungsshell ausgeführt werden.
  
### <a name="to-test-sip-trunk-configuration-settings"></a>Testen von Konfigurationseinstellungen für SIP-Trunks

- Mit dem folgenden Befehl wird überprüft, ob mit den Trunk-Konfigurationseinstellungen für den Standort Redmond die gewählte Rufnummer 4255551212 ordnungsgemäß konvertiert werden kann.
    
  ```powershell
  $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
  Test-CsTrunkConfiguration -DialedNumber 4255551212 -TrunkConfiguration $trunk
  ```


