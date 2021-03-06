---
title: Edgeeinstellungen – Erweiterung
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.tb.EdgeSettingsExpander
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: c73780cd-0033-4287-9ecd-ecf65ca61e62
ROBOTS: NOINDEX, NOFOLLOW
description: 'Die Einstellungen für einen vorhandenen Edgepool mit einem oder mehreren Servern werden in den folgenden Abschnitten bearbeitet:'
ms.openlocfilehash: cce6358779371d45b6db3707d01987b189a344af
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41793753"
---
# <a name="edge-settings-expander"></a>Edgeeinstellungen – Erweiterung

Die Einstellungen für einen vorhandenen Edgepool mit einem oder mehreren Servern werden in den folgenden Abschnitten bearbeitet:

- Allgemeine Einstellungen

- Einstellungen für nächsten Hop

- Edgeserver-Konfiguration


## <a name="general-settings"></a>Allgemeine Einstellungen

Vollqualifizierter Domänenname (Fully Qualified Domain Name, FQDN) des internen Pools für den Edgeserverpool. Bearbeiten Sie den FQDN des Pools, um diese Einstellung zu ändern.

Aktivieren Sie das Kontrollkästchen **Föderation für diesen Edge-Pool aktivieren (Port 5061)** , wenn Sie einen Verbund mit einem Skype for Business Server 2015-Server einrichten möchten.

Geben Sie die Portnummer unter **Interner Port für die Konfigurationsreplikation (HTTPS)** an.

## <a name="next-hop-selection-settings"></a>Einstellungen für nächsten Hop

Wählen Sie einen Director, Director-Pool, Front-End-Server oder Front-End-Serverpool aus dem Dropdown-Listenfeld aus, um den nächsten Hoppool**** anzugeben oder zu bearbeiten, den der Edgeserver für die Kommunikation mit der internen Infrastruktur verwenden soll. Nur Directors oder Front Ends, die im Topologie-Generator konfiguriert wurden, werden zur Auswahl angezeigt.

## <a name="edge-server-configuration"></a>Edgeserver-Konfiguration

Um die externen Einstellungen**** für die Edgeserver zu bearbeiten oder anzugeben, müssen Sie zunächst festlegen, ob separate IP-Adressen für den SIP-Zugriff, die Webkonferenzfunktion und den A/V-Dienst verwendet werden.

Wenn separate IP-Adressen verwendet werden sollen, aktivieren Sie das Kontrollkästchen **Separate FQDNs und IP-Adressen für Webkonferenzen und A/V aktivieren**. Für jeden Dienst muss ein DNS-A-Eintrag (Host) erstellt werden.

Für jeden externen Dienst geben Sie einen FQDN und einen zugeordneten Port an. Für den **SIP-Zugriff** würden z. B. „sip.contoso.com“ und der Port 5061 verwendet.

> [!IMPORTANT]
> Wenn Sie separate vollqualifizierte Domänennamen für die externen Dienste auswählen, muss jedem Dienst ein eindeutiger Portwert zugeordnet werden. Standardmäßig ist für SIP der Port 5061/TLS, für den Webkonferenz-Edgedienst der Port 444/TLS und für den A/V-Konferenzserver der Port 443/TLS festgelegt. Wenn Sie diese Einstellungen ändern (z. B. die Verwendung separater vollqualifizierter Domänennamen und IP-Adressen oder Ports festlegen), müssen Sie alle anderen Dienste aktualisieren, die von den ursprünglich konfigurierten Werten abhängen.

Wenn Sie festlegen, dass Ihre Organisation einen einzigen FQDN und eine einzige IP-Adresse für die externen Dienste verwendet, deaktivieren Sie das Kontrollkästchen **Separate FQDNs und IP-Adressen für Webkonferenzen und A/V aktivieren**. Bei Bedarf können Sie anschließend die Werte für den Pool-FQDN und den Port für den **SIP-Zugriff** ändern.

> [!IMPORTANT]
> Wenn Sie diese Einstellungen ändern (z. B. die Verwendung separater vollqualifizierter Domänennamen und IP-Adressen oder Ports festlegen), müssen Sie alle anderen Dienste aktualisieren, die von den ursprünglich konfigurierten Werten abhängen.

## <a name="see-also"></a>Siehe auch

Ausführliche Informationen zum Definieren und Konfigurieren der Einstellungen für die Edgedienste finden Sie unter [Define Your Edge Topology](https://technet.microsoft.com/library/787b23f1-8fa0-4c37-abf2-c516c5dd66f0.aspx).


