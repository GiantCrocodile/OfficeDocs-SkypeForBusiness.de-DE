---
title: Einrichten des Begrüssungs-bot für direktes Routing
author: LanaChin
ms.author: v-lanac
manager: serdars
ms.topic: article
ms.reviewer: filippse
ms.service: msteams
audience: admin
description: Hier erfahren Sie, wie Sie den Rückruf-bot für das direkte Routing verwenden, um unerwartete Stille zu verhindern, die auftreten können, wenn ein Anruf eingerichtet wird.
localization_priority: Normal
ms.collection:
- M365-voice
appliesto:
- Microsoft Teams
ms.openlocfilehash: 3fcb69ba1bc612fe940054ec982eb7462c6679be
ms.sourcegitcommit: a23f45ab3a2cb7b5c279356edddf61c4030c41bd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "39962502"
---
# <a name="set-up-the-ringback-bot-for-direct-routing"></a>Einrichten des Begrüssungs-bot für direktes Routing

In diesem Artikel wird der Begrüssungs-bot beschrieben, mit dem Sie unerwartete Stille vermeiden können, die auftreten können, wenn es längere Zeit dauert, bis die Anrufe eingerichtet werden. Der Rückruf-bot steht für das direkte Routing im nicht-Media-Bypass-Modus zur Verfügung.

Manchmal können eingehende Anrufe aus dem PSTN (Public Switched Telephone Network) an Teams-Clients länger als erwartet dauern. Dies kann aus verschiedenen Gründen erfolgen. In diesem Fall hört der Anrufer möglicherweise nichts, der Team-Client klingelt nicht und der Anruf kann von einigen Telekommunikationsanbietern abgebrochen werden.

Der Rückruf-bot hilft, unerwartete Stille zu vermeiden, die in diesem Szenario auftreten können. Für eingehende Anrufe vom PSTN an Teams-Clients spielt der Rückruf-bot ein unverwechselbares Audiosignal an den Anrufer ab, um anzugeben, dass die Mannschaft den Anruf annimmt.

> [!NOTE]
> Der Rückruf-bot generiert frühe Medien aus dem Back-End von Teams. In einigen Ländern und Regionen wird Ihnen möglicherweise der Anruf in Rechnung gestellt, wenn das Medium in den Fluss geht.

## <a name="configure-the-ringback-bot"></a>Konfigurieren des Rückruf-bot

Verwenden Sie die Cmdlets " [Satz-CsOnlineGateway](https://docs.microsoft.com/powershell/module/skype/set-csonlinepstngateway) " und " [New-CsOnlinePSTNGateway](https://docs.microsoft.com/powershell/module/skype/new-csonlinepstngateway) " zusammen mit dem **GenerateRingingWhileLocatingUser** -Parameter, um den Rückruf-bot zu konfigurieren.

Um den Rückruf-bot zu aktivieren, setzen Sie den **GenerateRingingWhileLocatingUser** -Parameter auf **$true**. Dies ist der Standardwert. 

Um den Rückruf-bot zu deaktivieren, setzen Sie den **GenerateRingingWhileLocatingUser** -Parameter auf **$false**. 

## <a name="related-topics"></a>Verwandte Themen

- [Übersicht über PowerShell für Microsoft Teams](teams-powershell-overview.md)