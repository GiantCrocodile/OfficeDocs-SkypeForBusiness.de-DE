---
title: Bereitstellung von Skype Room System-Konten in Office 365
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 2/6/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: c36150bb-461c-4f1c-877b-fac7fb232f7c
description: Lesen Sie dieses Thema und erfahren Sie, wie Skype Room System-Konten in Office 365 bereitgestellt werden.
ms.openlocfilehash: be90831eba5f16f5a3b41f4c74c26333bf728926
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="provisioning-skype-room-system-accounts-in-office-365"></a>Bereitstellung von Skype Room System-Konten in Office 365
 
Lesen Sie dieses Thema und erfahren Sie, wie Skype Room System-Konten in Office 365 bereitgestellt werden.
  
Der folgende Abschnitt behandelt Skype Raum Systemkonto Bereitstellung für Office 365-Mandanten.
  
## <a name="office-365-prerequisites"></a>Office 365-Softwarekomponenten

Ihr Onlinemandant muss die folgenden Anforderungen erfüllen:
  
- Office 365-Plan muss Skype für Business Online – Plan 2, Plan 3 oder Office 365 E1, E3 oder E5 enthalten.
    
- Ihres Mandanten benötigen die Möglichkeit, Konferenzen Skype für Unternehmen aktiviert.
    
- Für Ihren Mandanten muss Exchange Online aktiviert sein. 
    
- Ihr Remote-Mandantenadministrator muss über folgenden PowerShell-Zugriff verfügen:
    
  - Exchange – Remote-PowerShell-Zugriff
    
  - Skype für Business Online Remote PowerShell access
    
  - Windows Azure Active Directory-Modul für Windows PowerShell Access Office 365 Directory Access
    
Für das Skype Room-Konto ist folgende Lizenzierung erforderlich:
  
- Einen Skype für Business Online – Plan 2 oder Office 365 E1 oder E3 Lizenz ist erforderlich, um Skype Besprechungen zu aktivieren.
    
- Um den Chatroom mit dem Enterprise-VoIP-Funktion berechtigen, damit der Chatroom mit einer Telefonnummer aktiviert werden kann, ist eine Skype für Business Online – Plan 2 mit dem Cloud PBX Add-on oder Office 365 E5 erforderlich ist (1).
    
- Die Verfügbarkeit der Ausstattung für Konferenzen über das Festnetz innerhalb beliebiger Besprechungen wird von der Lizenz des Besprechungsorganisators bestimmt.
    
- Eine Exchange Online-Lizenz ist für das Skype Room-Konto nicht erforderlich, weil das Konto als Ressourcenpostfachkonto konfiguriert sein sollte.
    
## <a name="provisioning-overview"></a>Überblick über die Bereitstellung

Die folgende Abbildung bietet eine Übersicht über das Skype Raum-Systemkonto-Flusses in Office 365-Bereitstellung.
  
![Skype Room System – Schritte zur Bereitstellung für O365](../../media/354c5659-317b-4e85-a1bc-c60c07f305a4.png)
  
## <a name="identify-a-new-conference-room"></a>Erkennung eines neuen Konferenzraums

Möglicherweise haben Sie bereits ein Ressourcenpostfach Raum im Exchange, die das Feature scheduling bereitstellt, oder Sie erstellen ein Ressourcenpostfach zum ersten Mal auf Skype Raum System-Bereitstellung zu erleichtern. In jedem Fall müssen Sie einen Raum in Ihrem Mandanten verwendet werden identifizieren. Die Exchange Online-Bereitstellung und Skype für Business Provision Abschnitte bieten einen Leitfaden für beide Arten von Konten. Angenommen, beispielsweise stehen Ihnen die folgenden zwei Räume und Skype Raum System für beide bereitstellen möchten:
  
- Vorhandenes Ressourcenpostfachkonto: confrm1@contoso.onmicrosoft.com
    
- Neues Ressourcenpostfachkonto: confrm2@contoso.onmicrosoft.com
    
## <a name="exchange-online-provisioning"></a>Exchange-Onlinebereitstellung

Zunächst, eine Verbindung mit Exchange Online PowerShell gemäß die Anweisungen im Thema [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
  
Wenn ein vorhandenes Postfachkonto für die Ressource Raum für Skype Raum System festlegen möchten, führen Sie die folgenden Befehle in Exchange Online PowerShell:
  
```
$rm="confrm1@contoso.onmicrosoft.com"
$newpass='pass@word1'
Set-Mailbox -Identity $rm  -EnableRoomMailboxAccount $true -RoomMailboxPassword (ConvertTo-SecureString $newpass -AsPlainText -Force)
```

Führen Sie die folgenden Befehle in Exchange Online PowerShell, um ein neues Exchange-Postfach Ressourcenkonto für Skype Raum System zu erstellen:
  
```
$rm="confrm2@contoso.onmicrosoft.com"
$newpass='pass@word1'
New-Mailbox -Name "Conf Room 2" -MicrosoftOnlineServicesID $rm -Room  -EnableRoomMailboxAccount $true -RoomMailboxPassword (ConvertTo-SecureString $newpass -AsPlainText -Force)
```

Die oben angegebenen Befehle einrichten oder erstellen ein neues Exchange-Postfach Ressourcenkonto für Skype Raum Systemverwendung werden, da das Konto.
  
Das Cmdlet Set-CalendarProcessing in Exchange Online PowerShell können Sie nach dem Erstellen des Postfachs an, um das Postfach zu konfigurieren. Mehr dazu erfahren Sie in den Schritten 3–6 unter „Lokale Bereitstellungen mit einzelner Gesamtstruktur“.
  
## <a name="skype-for-business-online-provisioning"></a>Skype for Business Online-Bereitstellung

Nachdem ein Ressource Postfach Raum erstellt und aktiviert, wie zuvor gezeigt wurde, wird das Konto aus der Gesamtstruktur Exchange Online mit Skype für Business Online Gesamtstruktur synchronisiert werden mithilfe von Windows Azure Active Directory-Gesamtstruktur. Die folgenden Schritte sind erforderlich, das Systemkonto von Skype Raum in der Skype für Business Online Pool bereitstellen. Diese Schritte sind identisch für ein vorhandenes Postfach Ressourcenkonto oder eines neu erstellten Kontos (confrm1 oder confrm2), da Nachdem sie im Exchange Online aktiviert sind, beide Konten zu Skype für Business Online auf die gleiche Weise synchronisiert werden soll:
  
1. Erstellen Sie eine PowerShell-Remotesitzung. Beachten Sie, dass Sie benötigen Skype für Business Online Connectormodul und Microsoft Online Services-Anmeldeassistent herunterladen, und stellen Sie sicher, dass Ihr Computer konfiguriert ist. Weitere Informationen finden Sie unter [Konfigurieren von Your Computer für Lync Online-Verwaltung](http://technet.microsoft.com/library/bca143e2-659a-4161-9220-59ffd9fc2874.aspx).
    
   ```
   Import-Module LyncOnlineConnector
   $cssess=New-CsOnlineSession -Credential $cred
   Import-PSSession $cssess -AllowClobber
   ```

2. Um ein Systemkonto von Skype Raum für Skype für Unternehmen zu aktivieren, führen Sie den folgenden Befehl ein:
    
   ```
   Enable-CsMeetingRoom -Identity $rm -RegistrarPool "sippoolbl20a04.infra.lync.com" -SipAddressType EmailAddress
   ```

    Sie können die RegistrarPool Adresse, wo Ihre Skype für Unternehmensbenutzer mit den folgenden Befehl aus, um von einem Ihrer vorhandenen Konten verwaltet werden, gibt diese Eigenschaft erhalten:
    
   ```
   Get-CsOnlineUser -Identity 'alice@contoso.onmicrosoft.com'| fl *registrarpool*
   ```

## <a name="assigning-a-skype-for-business-online-license"></a>Zuweisen einer Skype for Business Online-Lizenz

Nachdem Sie ein Systemkonto von Skype Raum in Skype für Unternehmen aktiviert haben, können Sie einen Skype für Business Online (Plan 2) zuweisen oder Skype für Business Online (Plan 3)-Lizenz mithilfe von administrativen Office 365-Portal, wie beschrieben in [zuweisen oder Entfernen von Lizenzen für Office 365 für Unternehmen](https://support.office.com/en-us/article/Assign-or-remove-licenses-for-Office-365-for-business-997596b5-4173-4627-b915-36abac6786dc?ui=en-US&amp;rs=en-US&amp;ad=US) oder in [Skype für Business Add-On-Lizenzierung](https://support.office.com/en-US/article/Skype-for-Business-add-on-licensing-3ed752b1-5983-43f9-bcfd-760619ab40a7). 
  
Nachdem Sie eine Lizenz für Skype für Business Online zuweisen, werden Sie können sich anmelden, und überprüfen, dass das Konto verwenden Skype für Business Client aktiv ist.
  
## <a name="password-expiration"></a>Kennwortablauf

In Office 365 sieht die Standardrichtlinie für den Ablauf von Kennwörtern für alle Ihre Benutzerkonten eine Laufzeit von 90 Tagen vor, es sei denn, Sie konfigurieren einer andere Richtlinie für den Ablauf von Kennwörtern. Wählen Sie für Skype Raum Systemkonten, das Kennwort läuft nie ab Einstellung die folgenden Schritte aus.
  
1. Erstellen Sie eine Windows Azure Active Directory-Sitzung, indem Sie Ihre Mandantenanmeldedaten als globaler Administrator verwenden.
    
    ```
    $cred=Get-Credential admin@$org
    Connect-MsolService -Credential $cred
    ```

2. Set das Kennwort läuft nie ab Einstellung für das Skype Raum Raum Systemkonto zuvor erstellten mithilfe des folgenden Befehls:
    
   ```
   Set-MsolUser -UserPrincipalName confrm1@skypelrs.onmicrosoft.com -PasswordNeverExpires $true
   ```

Weitere Informationen finden Sie unter [Using Windows PowerShell zum Verwalten von Lync Online](http://technet.microsoft.com/library/9ef2d853-10fb-4e02-a552-dcf6818d7153.aspx).
  
