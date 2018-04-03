---
title: Konfigurieren der Integration zwischen lokalen Skype für Business Server 2015 und Outlook Web App
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/7/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
description: 'Zusammenfassung: Integrieren von Skype für Business Server und Outlook Web App.'
ms.openlocfilehash: 4ac4d6a71f8006e813d09631f8ccf28742940ff2
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="configure-integration-between-on-premises-skype-for-business-server-2015-and-outlook-web-app"></a>Konfigurieren der Integration zwischen lokalen Skype für Business Server 2015 und Outlook Web App
 
**Zusammenfassung:** Integrieren von Skype für Business Server und Outlook Web App.
  
Kunden, die für die Business Server 2015 Bereitstellungen lokalen Skype verwenden können Interoperabilität mit Microsoft Outlook Web App in Microsoft Exchange Online in einer hybriden Bereitstellung-Modus konfigurieren. Zu den Interoperabilitätsfunktionen gehören einmaliges Anmelden (SSO) und Sofortnachrichten sowie die Anwesenheitsintegration in die Outlook Web App-Schnittstelle. Um diese Integration aktivieren, müssen Sie den Edge-Server in Ihrer lokalen Skype für Business Server-Bereitstellung konfigurieren, durch die folgenden Aufgaben: 
  
- Konfigurieren eines freigegebenen SIP-Adressraums
    
- Konfigurieren eines Hostinganbieters auf dem Edge-Server
    
- Überprüfen der Replikation des aktualisierten zentralen Verwaltungsspeichers
    
## <a name="configure-a-shared-sip-address-space"></a>Konfigurieren eines freigegebenen SIP-Adressraums

Um lokale Skype für Business Server 2015 mit Exchange Online zu integrieren, müssen Sie einen freigegebenen SIP-Adressraum konfigurieren. Demselben Adressraum für SIP-Domäne wird von Skype für Business Server und Exchange Online-Dienst unterstützt.
  
Verwenden die Skype als Business Server-Verwaltungsshell, Konfigurieren der Edge-Server für den Verbund durch das **Set-CSAccessEdgeConfiguration** -Cmdlet mit den im folgenden Beispiel angezeigten Parametern ausführen:
  
```
Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True
```

- **AllowFederatedUsers** -Parameter gibt an, ob interne Benutzer zur Kommunikation mit Benutzern von Partnerdomänen zulässig sind. Diese Eigenschaft bestimmt zudem, ob interne Benutzer mit Benutzern in einem freigegebenen SIP-Adresse Speicherplatz Szenario mit Skype für Business Server und Exchange Online kommunizieren können.
    
Weitere Informationen zur Verwendung der Skype für Business Server-Verwaltungsshell finden Sie unter [Skype für Business Server 2015-Verwaltungsshell](../../manage/management-shell.md).
  
## <a name="configure-a-hosting-provider-on-the-edge-server"></a>Konfigurieren eines Hostinganbieters auf dem Edgeserver

Konfigurieren Sie mit der Skype für Business Server-Verwaltungsshell, einen Hostinganbieter auf dem Edgeserver durch das **New-CsHostingProvider** -Cmdlet mit den Parametern im folgenden Beispiel ausführen:
  
```
New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification
```

> [!NOTE]
> Wenn Sie Office 365 über 21Vianet in China nutzen, ersetzen Sie den Wert für den Parameter **ProxyFqdn** in diesem Beispiel („exap.um.outlook.com“) mit dem FQDN für den Dienst, der in China von 21Vianet bereitgestellt wird: „exap.um.partner.outlook.cn“.
  
- **Identität** gibt einen eindeutigen Zeichenfolgenwert für den Hostinganbieter, den Sie erstellen (z. B. "Exchange Online"). Werte, die Leerzeichen enthalten, müssen in Anführungszeichen gesetzt werden.
    
- **Enabled** gibt an, ob die Netzwerkverbindung zwischen Ihrer Domäne und dem Hostinganbieter aktiviert ist. Dieser Parameter muss auf TRUE festgelegt werden.
    
- **EnabledSharedAddressSpace** gibt an, ob der Hostinganbieter in einem freigegebenen SIP-Adresse Speicherplatz Szenario verwendet wird. Dieser Parameter muss auf TRUE festgelegt werden.
    
- **HostsOCSUsers** gibt an, ob der Hostinganbieter zum Hosten von Office Communications Server oder Skype für Business Server verwendet wird. Dieser Parameter muss auf FALSE festgelegt werden.
    
- **ProxyFQDN** gibt den vollqualifizierten Domänennamen (FQDN) für die vom Hostinganbieter verwendete Proxyserver. Für Exchange Online ist der FQDN „exap.um.outlook.com“.
    
- **IsLocal** gibt an, ob der vom Hostinganbieter verwendete Proxyserver in Ihrer Skype für Business Server-Topologie enthalten ist. Dieser Parameter muss auf FALSE festgelegt werden.
    
- **"Verificationlevel"** Gibt die Überprüfung zulässig für Nachrichten, die an und von der gehosteten Anbieter gesendet werden. Geben Sie **"usesourceverification"**, die den Überprüfungsstufen Hostinganbieter gesendeten Nachrichten enthalten benötigt. Wenn dieser Ebene nicht angegeben ist, wird die Meldung als nicht überprüfbar abgelehnt werden.
    
## <a name="verify-replication-of-the-updated-central-management-store"></a>Überprüfen der Replikation des aktualisierten zentralen Verwaltungsspeichers

Die mithilfe der Cmdlets in den vorherigen Abschnitten vorgenommenen Änderungen werden automatisch auf dem Edge-Server angewendet, und im Allgemeinen zum Replizieren von weniger als eine Minute dauern. Sie können überprüfen Sie den Replikationsstatus, und stellen dann sicher, dass die Änderungen an den Edge-Server mithilfe der folgenden Cmdlets angewendet wurden.
  
Führen Sie zum Überprüfen der Replikation-Updates auf einem Server in Ihrer Skype für Business Server-Bereitstellung das folgende Cmdlet aus:
  
```
Get-CsManagementStoreReplicationStatus
```

Führen Sie das folgende Cmdlet aus, um zu bestätigen, dass die Änderungen auf dem Edgeserver angewendet wurden:
  
```
Get-CsHostingProvider -LocalStore
```

## <a name="see-also"></a>Siehe auch

#### 

[Bereitstellen von Skype für Business Server 2015 Voicemail Benutzer-auf gehostete Exchange um-Dienste](http://technet.microsoft.com/library/306d3fb5-231b-4f0b-b8d8-0d9083b5ed77.aspx)
  
[Gehostete Exchange Unified Messaging Integration in Skype für Business Server 2015](http://technet.microsoft.com/library/f4de0165-da3b-499e-98fc-28ddd0db02d5.aspx)
