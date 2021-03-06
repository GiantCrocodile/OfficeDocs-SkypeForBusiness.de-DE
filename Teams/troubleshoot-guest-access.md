---
title: Behandeln von Problemen mit Gastzugriff in Microsoft Teams
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.topic: article
ms.service: msteams
audience: admin
ms.collection:
- Teams_ITAdmin_Help
- M365-collaboration
ms.reviewer: corbinm
search.appverid: MET150
description: Hier erhalten Sie Hilfe bei der Problembehandlung und dem Lösen von Problemen mit dem Gastzugriff in Microsoft Teams.
f1.keywords:
- NOCSH
localization_priority: Normal
appliesto:
- Microsoft Teams
ms.openlocfilehash: 0ce7744aa18fe8ffe3fc83ca40649672f521bbba
ms.sourcegitcommit: 43e5a4aac11c20dd5a4c35b59695f309e1559e82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2020
ms.locfileid: "48346356"
---
# <a name="troubleshoot-problems-with-guest-access-in-microsoft-teams"></a>Behandeln von Problemen mit Gastzugriff in Microsoft Teams

- Wenn Sie wissen möchten, ob Ihr Problem bekannt ist, lesen Sie [Support Teams in Ihrer Organisation](Known-issues.md).
- Wenn Sie nach Support für aktuelle Probleme mit dem Gastzugriff in Teams suchen möchten, wechseln Sie zu [Problembehandlung für Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/troubleshoot/).
- Gäste sind Personen außerhalb Ihrer Organisation. Wenn sich eine Person in Ihrer Organisation befindet (beispielsweise ihre Mitarbeiter, Auftragnehmer oder Agenten vor Ort), können Sie nicht als Gäste hinzugefügt werden. Das gleiche gilt für Ihre Partner.
- Informationen zu geplanten neuen oder aktualisierten Funktionen für den Gastzugriff finden Sie in der [Microsoft Teams-Roadmap](https://aka.ms/teamsroadmap).
- Teilen Sie uns auf der [Microsoft Teams-UserVoice](https://aka.ms/TeamsUserVoice)-Website Ihre Wünsche mit.

## <a name="if-your-guests-are-seeing-license-errors"></a>Wenn Ihre Gäste Lizenzfehler sehen

Für den Gastzugriff in Microsoft Teams wird Azure Active Directory (Azure AD) Business-to-Business (B2B) und dessen Lizenzierungsmodell genutzt. Der Gastzugang ist in allen Abonnements von Microsoft 365 Business Standard, Office 365 Enterprise und Office 365 Education enthalten. Eine zusätzliche Microsoft 365- oder Office 365-Lizenz ist nicht erforderlich.

> [!NOTE]
> Teams müssen für den Home-Mandanten eines Gasts aktiviert sein, damit Gäste sich anmelden und Teams als Gast für einen anderen (Ressourcen-) Mandanten verwenden können.

Wenn Sie Lizenzierungsfehler sehen, stellen Sie sicher, dass Sie das [Abrechnungsmodell für Azure AD External Identitys](https://docs.microsoft.com/azure/active-directory/external-identities/external-identities-pricing) lesen, um Lizenzierungsanforderungen zu ermitteln, die Ihren Anforderungen für den Gastzugriff in Ihrer Organisation entsprechen.

- Gastlizenzen werden für die einladende Organisation gezählt. Denken Sie daran, wenn Sie die Anzahl der benötigten Lizenzen berechnen.
- Lizenzen werden für Ihre Organisation gezählt, unabhängig davon, ob die eingeladenen Gäste aus einer anderen Microsoft 365-Organisation stammen oder Ihre persönlichen e-Mail-Adressen verwenden.

## <a name="support-for-b2b-user-types"></a>Unterstützung von B2B-Benutzertypen

Derzeit unterstützt Teams nur die Gastbenutzer vom Typ "Zustand 1" und "Zustand 2" [gemäß der Definition durch Azure B2B](https://docs.microsoft.com/azure/active-directory/b2b/user-properties).

## <a name="related-topics"></a>Verwandte Themen

[Gastzugriff in Teams](guest-access.md)

[Teams-Problembehandlung](https://docs.microsoft.com/MicrosoftTeams/troubleshoot/teams)