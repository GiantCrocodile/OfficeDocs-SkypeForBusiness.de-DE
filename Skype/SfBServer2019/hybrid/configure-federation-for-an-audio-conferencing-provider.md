---
title: Konfigurieren von Verbund für einen Anbieter von Audiokonferenzen in einer hybridbereitstellung
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: ''
ms.custom: ''
description: 'Zusammenfassung: Informationen Sie zum Konfigurieren von Verbund für einen Anbieter von Audiokonferenzen in Skype für Business Online.'
ms.openlocfilehash: 2f89045e7d2ee3e51a6526344d2dcf2f07c0d98d
ms.sourcegitcommit: 940cb253923e3537cb7fb4d7ce875ed9bfbb72db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2018
ms.locfileid: "25030756"
---
# <a name="configure-federation-for-an-audio-conferencing-provider-in-your-hybrid-deployment"></a>Konfigurieren von Verbund für einen Anbieter von Audiokonferenzen in einer hybridbereitstellung

**Zusammenfassung:** Informationen Sie zum Konfigurieren von Verbund für einen Anbieter von Audiokonferenzen in Skype für Business Online.

Wenn Sie ein Audio Conferencing Provider (ACP) in der hybridbereitstellung (lokal mit online) verwenden möchten, müssen Sie als eine zulässige Partnerserver Verbund zwischen der lokalen Bereitstellung und dem ACP Partner konfigurieren. Sie können den Verbund durch Hinzufügen der Partnerdomäne ACP und Edge-Server (Dies kann auch der Zugriffsproxy bezeichnet werden) zur Liste Partnerdomänen konfigurieren, für die lokale Bereitstellung. Ihr ACP Partner muss den FQDN des Pools lokalen Edge-Server ihrer Liste der zulässigen Partnerdomänen hinzufügen. Weitere Informationen erhalten Sie bei Ihrem Anbieter ACP. Ihr ACP Partner muss den FQDN des Pools lokalen Edge-Server ihrer Liste der zulässigen Partnerdomänen hinzufügen.

- **Hinzufügen der ACP-Domäne und des Edgeservers als zugelassene Partnerverbunddomäne**

    Um die ACP-Domäne als eine zulässige Partnerserver (Partnerverbunddomänen zulässig) hinzuzufügen, führen Sie die Schritte in [Konfigurieren der Unterstützung für externe Domänen zulässig](https://technet.microsoft.com/library/3ee6e175-986d-4c33-b03a-b9f93083dca6.aspx). Fügen Sie den FQDN des Edge-Server des ACP Partners für den Edge-Server hinzu. Sie müssen sich möglicherweise an Ihren ACP-Partner wenden, um den FQDN für seinen Edgeserver zu erhalten, der von Ihrem ACP möglicherweise auch als Zugriffsproxy bezeichnet wird.

- **Bereitstellen von den FQDN des Pools Ihrer Edge-Server für dem ACP partner**

    Der ACP-Partner muss einen Partnerverbund konfigurieren, um Ihre lokale Domäne als einen zulässigen Partnerserver hinzuzufügen, indem der FQDN Ihres Edgeserverpools als eine zugelassene Partnerverbunddomäne hinzugefügt wird.

