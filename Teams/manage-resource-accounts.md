---
title: Verwalten von Ressourcenkonten in Teams
ms.author: jambirk
author: jambirk
manager: serdars
ms.reviewer: jastark, wasseemh
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection: Teams_ITAdmin_Help
ms.audience: Admin
appliesto:
- Microsoft Teams
localization_priority: Normal
f1keywords:
- ms.teamsadmincenter.orgwidesettings.resourceaccounts.overview
description: Verwalten von Resource-Konten in Microsoft-Teams
ms.openlocfilehash: a40d281349f6b5f8cdc8a95dbb77a7d3f9da8cc4
ms.sourcegitcommit: f5f1437ec72f67f6804ca8d785f76059d0979e39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29890756"
---
# <a name="manage-resource-accounts-in-teams"></a>Verwalten von Ressourcenkonten in Teams 

Ein Ressourcenkonto wird auch als ein deaktiviertes Benutzerobjekt in Azure Active Directory und können verwendet werden, um Ressourcen im Allgemeinen darstellen. In Exchange kann verwendet werden, Konferenzräumen, beispielsweise darstellen und ermöglicht es ihnen, Sie haben eine Telefonnummer ein. Ein Ressourcenkonto kann in Microsoft 365 oder lokal mit Skype für Business Server verwaltet werden, und diese Konten werden mithilfe von Powershell-Befehlen erstellt.

In Microsoft-Teams, os Skype für Business Online, jeden Anruf Warteschlange oder automatische wird Attendant erforderlich, um ein Ressourcenkonto zugeordneten verfügen. Ob ein Ressourcenkonto eine zugewiesene Telefonnummer benötigt wird abhängig von der beabsichtigten Verwendung von der zugehörigen Aufruf Warteschlange oder automatische Telefonzentrale. Finden Sie in den Artikeln für Anruf Warteschlangen und automatische um-Telefonzentralen verknüpft unten in diesem Artikel, bevor Sie eine Telefonnummer ein Ressourcenkonto zuweisen.

## <a name="prerequisites-to-assign-a-phone-number-to-a-resource-account"></a>Erforderliche Komponenten ein Ressourcenkonto eine Telefonnummer zuweisen

Erste Schritte beim es ist wichtig, sollten Sie einige Dinge bedenken:
  
- Ihre Organisation muss eine Lizenz Enterprise E3 plus **Telefonsystem** oder einer E5 Enterprise-Lizenz (mindestens) verfügen. Die Anzahl der **Telefonsystem** Benutzerlizenzen, die zugewiesen sind, wirkt sich auf die Anzahl der Dienst Zahlen, die für die Ressourcenkonten zugewiesenen Warteschlangen oder automatische Telefonzentralen Aufrufen bei verfügbar sind. Die Anzahl der Ressourcenkonten ab können ist abhängig von der Anzahl der **Telefonsystem** und **Audiokonferenzen** Lizenzen, die in Ihrer Organisation zugewiesen sind. Weitere Informationen zu Lizenzierung finden Sie unter [Skype für Geschäfts- und Microsoft-Teams, Add-On-Lizenzierung](/skypeforbusiness/skype-for-business-and-microsoft-teams-add-on-licensing/skype-for-business-and-microsoft-teams-add-on-licensing).

    > [!NOTE]
    > Zum Umleiten von Anrufen an Personen in Ihrer Organisation, die Online sind, sie benötigen eine Lizenz **Telefonsystem** und für Enterprise-VoIP aktiviert sein oder Office 365 aufrufen Plans. Siehe [Zuweisen von Skype for Business- und Microsoft Teams-Lizenzen](/skypeforbusiness/skype-for-business-and-microsoft-teams-add-on-licensing/assign-skype-for-business-and-microsoft-teams-licenses.md). Um diese Lizenzen für Enterprise-VoIP zu aktivieren, können Sie die Windows PowerShell verwenden. Führen Sie beispielsweise folgenden Befehl aus:  `Set-CsUser -identity "Amos Marble" -EnterpriseVoiceEnabled $true`
  
- Weitere Informationen zu Office 365 Anrufplänen finden Sie unter [Was sind Anrufpläne in Office 365?](/microsoftteams/what-are-calling-plans-in-office-365) und [Anrufpläne für Office 365](/microsoftteams/calling-plans-for-office-365).
- Sie können nur zuweisen gebührenpflichtige oder gebührenfreie Service Telefonnummern, die Sie haben Sie in der **Microsoft-Teams, Administrationscenter** oder in einem Ressourcenkonto aus einer anderen Dienstanbieter übertragen. Um gebührenfreie Servicenummern zu erhalten müssen Sie Communication Credits einrichten.

> [!NOTE]
> Ein Ressourcenkonto nicht Benutzer (Abonnent) Rufnummern zugewiesen werden – nur Service gebührenpflichtige oder gebührenfreie Telefonnummern verwendet werden können.

Eine Telefonnummer ein, um ein Ressourcenkonto zuzuweisen, müssen Sie erhalten möchten, oder übertragen Ihre vorhandenen gebührenpflichtige oder gebührenfreie Service Zahlen. Nachdem Sie die gebührenpflichtige oder gebührenfreie Service Telefonnummern erhalten möchten, sie werden angezeigt, in der **Microsoft-Teams, Administrationscenter** > **VoIP** > **Telefonnummern**und die **Typ-Nummer** aufgeführt wird als **Dienst - gebührenfreie**aufgeführt werden. Um die Rufnummern Service erhalten möchten, finden Sie unter [Getting Service Rufnummern](/skypeforbusiness/what-is-phone-system-in-office-365/getting-service-phone-numbers.md) oder Übertragung und vorhandenen Service-Nummer, finden Sie unter [Übertragen von Telefonnummern zu Office 365](/microsoftteams/transfer-phone-numbers-to-office-365).
  
> [!NOTE]
> Wenn Sie sich außerhalb der USA sind, können das Microsoft-Teams, Administrationscenter Sie um Service Zahlen zu erhalten. Wechseln Sie zum [Verwalten von Rufnummern für Ihre Organisation](/microsoftteams/manage-phone-numbers-for-your-organization) stattdessen, wie Sie von außerhalb der USA finden Sie unter.

## <a name="create-a-resource-account-in-powershell"></a>Erstellen Sie ein Ressourcenkonto in Powershell

 Sie würden ein Ressourcenkonto durch Ausführen des entsprechenden Powershell-Cmdlets (für eine oder mehrere Ressourcenkonten) nach Bedarf erstellen, und geben Sie jeweils einen Namen und so weiter. Derzeit keine Option zum Erstellen einer Ressource-Konto in der Verwaltungskonsole von Microsoft-Teams vorliegt, aber Sie können Telefonnummern bearbeiten und ändern Sie die Anruf Warteschlange oder Auto attendant Zuordnungen für ein Ressourcenkonto.

Je nachdem, ob Ihre Telefonnummer online oder lokal befindet müssen Sie in der entsprechenden Aufforderung Powershell mit Administratorberechtigungen eine Verbindung herstellen.

- Hybrid Implementierungen (Zahlen Zahlen verwaltet auf direktes Routing, OPCH und CCE) werden [Neu CsHybridApplicationEndpoint](https://docs.microsoft.com/powershell/module/skype/new-cshybridapplicationendpoint?view=skype-ps) verwenden, um ein Ressourcenkonto erstellen, die lokal verwaltet wird.  
- Nur Online Implementierungen [New-CsOnlineApplicationInstance](https://docs.microsoft.com/powershell/module/skype/new-CsOnlineApplicationInstance?view=skype-ps) verwendet, die ein Resource-Konto verfügen, die online verwaltet wird.

Es folgt ein Beispiel für online-Umgebung ein Ressourcenkonto erstellen:

``` Powershell
New-CsOnlineApplicationInstance -DisplayName Node1 -SipAddress sip:node1@litwareinc.com -OU "ou=Redmond,dc=litwareinc,dc=com"
```

Weitere Informationen zu diesem Befehl finden Sie unter [New-CsOnlineApplicationInstance](https://docs.microsoft.com/powershell/module/skype/new-csonlineapplicationinstance?view=skype-ps) .

> [!NOTE]
> Es ist am einfachsten kann die Telefonnummer ein, mit dem Microsoft-Teams, Administrationscenter festlegen, wie im nächsten Abschnitt beschrieben. Sie können auch die `Set-CsOnlineApplicationInstance` Befehl für eine Zuweisung eine Rufnummer, das Ressourcenkonto nach der anfänglichen Erstellung wie dargestellt:

``` Powershell
Set-CsOnlineApplicationInstance -Identity "CN={4f6c99fe-7999-4088-ac4d-e88e0b3d3820},OU=Redmond,DC=litwareinc,DC=com" -DisplayName Node1 -LineURI tel:+14255550100
```

Weitere Informationen zu diesem Befehl finden Sie unter [Set-CsOnlineApplicationInstance](https://docs.microsoft.com/powershell/module/skype/set-csonlineapplicationinstance?view=skype-ps) .

## <a name="manage-resource-account-settings-in-microsoft-teams-admin-center"></a>Verwalten von Einstellungen für Ressource-Konto im Microsoft-Teams, Administrationscenter

Navigieren Sie zum Verwalten von Einstellungen der Ressource-Konto im Microsoft-Teams, Administrationscenter zu **Org geltende Settings**  > **Ressource Firmen**, auswählen das Ressourcenkonto Sie Einstellungen für ändern müssen und dann auf die Schaltfläche **Bearbeiten** . Klicken Sie im Bildschirm **Bearbeiten Ressourcenkonto** werden Sie ändern die:

- **Anzeigename** für das Konto
- Rufen Sie die Warteschlange oder automatische um-Telefonzentrale, die das Konto verwendet
- Das Konto zugewiesene Telefonnummer

Klicken Sie abschließend auf **Speichern**.

## <a name="related-information"></a>Verwandte Informationen

Für Implementierungen sind, Hybrid mit Skype für Business Server:

[Planen von Cloud-Telefonzentrale](/SkypeForBusiness/hybrid/plan-cloud-auto-attendant)

[Konfigurieren von Cloud-Telefonzentralen](/SkypeForBusiness/hybrid/configure-cloud-auto-attendant)

Für Implementierungen in Teams oder Skype für Business Online:

[Was sind automatische Telefonzentralen für das Telefonsystem?](what-are-phone-system-auto-attendants)

[Einrichten einer automatischen Telefonzentrale für das Telefonsystem](/SkypeForBusiness/what-is-phone-system-in-office-365/set-up-a-phone-system-auto-attendant)

[Beispiel für Small Business - richten Sie eine automatische Telefonzentrale](https://docs.microsoft.com/en-us/SkypeForBusiness/what-is-phone-system-in-office-365/tutorial-org-aa)

[Erstellen einer Telefonsystem-Anrufwarteschleife](/SkypeForBusiness/what-is-phone-system-in-office-365/create-a-phone-system-call-queue)

[Neue CsHybridApplicationEndpoint](https://docs.microsoft.com/powershell/module/skype/new-cshybridapplicationendpoint?view=skype-ps)

[Neue CsOnlineApplicationInstance](https://docs.microsoft.com/powershell/module/skype/new-csonlineapplicationinstance?view=skype-ps)