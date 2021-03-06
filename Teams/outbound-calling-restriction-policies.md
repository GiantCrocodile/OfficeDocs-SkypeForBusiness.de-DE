---
title: Einschränkungen für ausgehende Anrufe-Audiokonferenzen & PSTN-Anrufe
ms.reviewer: ''
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
search.appverid: MET150
ms.collection:
- M365-voice
audience: Admin
appliesto:
- Skype for Business
- Microsoft Teams
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Audio Conferencing
- seo-marvel-mar2020
description: Administratoren können den Typ von Audiokonferenz-und Endbenutzer-PSTN-anrufen steuern, die von Benutzern vorgenommen werden können.
ms.openlocfilehash: e085f996226a59d88339b20e64dd06f68ef566ce
ms.sourcegitcommit: ee217e1d7188842c7becd19387fd421b485c3575
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "48908654"
---
# <a name="outbound-calling-restriction-policies-for-audio-conferencing-and-user-pstn-calls"></a>Einschränkungsrichtlinien für ausgehende Anrufe für Audiokonferenzen und PSTN-Anrufe

Als Administrator können Sie die Steuerelemente für ausgehende Anrufe verwenden, um den Typ der Audiokonferenzen und Endbenutzer-PSTN-Anrufe einzuschränken, die von Benutzern in Ihrer Organisation verwendet werden können. 

Steuerelemente für ausgehende Anrufe können auf Benutzerebene angewendet werden und bieten die folgenden zwei Steuerelemente, um die einzelnen ausgehenden Anrufe unabhängig voneinander zu beschränken. Standardmäßig sind beide Steuerelemente so eingestellt, dass Auslands-und Inlandsanrufe zugelassen werden. 

|Steuerelement|Beschreibung|Steuerelementoptionen|
|:-----|:-----|:-----|
|PSTN-Anrufe für Audiokonferenzen|Schränkt den ausgehenden Typ ein </br>Anrufe, die innerhalb von zulässig sind </br>Besprechungen, die von einem Benutzer organisiert werden.|Beliebiges Ziel (Standard)</br>Im gleichen Land oder in derselben Region wie der Organisator </br> [Zone nur für Länder oder Regionen](audio-conferencing-zones.md) </br>Nicht zulassen|
|PSTN-Anrufe für Endbenutzer|Schränkt die Art der Anrufe ein </br>, die von einem Benutzer vorgenommen werden können.|International und Domestic (Standard)</br>Inlandsanruf</br>Keine|

Wenn Sie feststellen möchten, welche Länder und Regionen als Zone A gelten, lesen Sie [Länder-und Regions Zonen für Audiokonferenzen](audio-conferencing-zones.md).

   > [!NOTE]
   > Ein Anruf wird als "Domestic" bezeichnet, wenn sich die gewählte Rufnummer im selben Land befindet, in dem Microsoft 365 oder Office 365 für den Organisator der Besprechung eingerichtet wurde (im Fall von Audiokonferenzen) oder der Endbenutzer (im Fall von PSTN-anrufen des Endbenutzers). 

> [!NOTE]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

## <a name="restrict-audio-conferencing-outbound-calls"></a>Einschränken von ausgehenden Anrufen für Audiokonferenzen

![Ein Symbol mit dem Microsoft Teams-Logo](media/teams-logo-30x30.png) **Verwenden des Microsoft Teams Admin Centers**

1. Klicken Sie in der linken Navigationsleiste auf **Benutzer** , und klicken Sie dann in der Liste der verfügbaren Benutzer auf den Anzeigenamen des Benutzers.

3. Klicken Sie neben **Audiokonferenzen** auf **Bearbeiten**.

4. Wählen Sie unter **Einwahl von Besprechungen** die gewünschte Option für die Wahl Beschränkung aus.

5. Klicken Sie auf **Speichern**. 

![Ein Symbol mit dem Skype for Business-Logo](media/sfb-logo-30x30.png) **Unter Verwendung des Skype for Business Admin Centers**

1. Wechseln Sie im **Skype for Business Admin Center** im linken Navigationsbereich zu **Audiokonferenz-**  >  **Benutzer** , und wählen Sie den Benutzer in der Liste der verfügbaren Benutzer aus.

2. Klicken Sie im Bereich „Aktion" auf **Bearbeiten**.

3.  Wählen Sie unter **Einschränkungen für Auswahlen in Besprechungen dieses Benutzers** die gewünschte Option für das Auswählen von Einschränkungen aus.

      ![Die Einschränkungen für Optionen für Auswahlen](media/restrictions-to-dial-outs.png)
      

4. Klicken Sie auf **Speichern**.

> [!Note]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

**Verwendung von PowerShell**

Einschränkungen für ausgehende Anrufe werden durch eine einzelne Richtlinie mit dem Namen OnlineDialOutPolicy gesteuert, die ein Einschränkungs Attribut für jede hat. Die Richtlinie kann nicht angepasst werden, es gibt jedoch vordefinierte Richtlinieninstanzen für jede Kombination der Einstellungen. 

Sie können das Get-CSOnlineDialOutPolicy-Cmdlet verwenden, um die ausgehenden Anruf Richtlinien anzuzeigen und Sie Benutzern mithilfe des Grant-CSDialOutPolicy-Cmdlets zuzuweisen. (Bitte beachten Sie, dass das Grant-Cmdlet das Wort "Online" nicht enthält, wie es das Get-Cmdlet tut.) 

Die folgende Tabelle enthält eine Übersicht über die einzelnen Richtlinien.

|||
|:-----|:-----|
|Identity = ' Tag: DialoutCPCandPSTNInternational '    |    Der Benutzer in der Konferenz kann sich in Auslands-und Inlands Nummern einwählen, und dieser Nutzer kann auch ausgehende Anrufe an Auslands-und Inlands Nummern tätigen.    |
|Identity = ' Tag: DialoutCPCDomesticPSTNInternational '  |    Der Benutzer in der Konferenz kann sich nur an inländische Rufnummern anwählen, und dieser Benutzer kann ausgehende Anrufe an Auslands-und Inlands Nummern tätigen.    |
|    Identity = ' Tag: DialoutCPCDisabledPSTNInternational '    |    Der Benutzer in der Konferenz kann keine Anrufe tätigen. Dieser Nutzer kann ausgehende Anrufe an Auslands-und Inlands Nummern tätigen.    |
|    Identity = ' Tag: DialoutCPCInternationalPSTNDomestic '    |    Der Benutzer in der Konferenz kann sich in Auslands-und Inlands Nummern einwählen, und dieser Nutzer kann nur ausgehende Anrufe an eine inländische PSTN-Nummer tätigen.    |
|    Identity = ' Tag: DialoutCPCInternationalPSTNDisabled '    |    Der Benutzer in der Konferenz kann sich in Auslands-und Inlands Nummern einwählen, und dieser Nutzer kann außer Notrufnummern keine ausgehenden Anrufe an eine PSTN-Nummer tätigen.    |
|    Identity = ' Tag: DialoutCPCandPSTNDomestic '    |    Der Benutzer in der Konferenz kann sich nur an inländische Rufnummern anwählen, und dieser Benutzer kann nur ausgehende Anrufe an inländische PSTN-Nummern tätigen.    |
|    Identity = ' Tag: DialoutCPCDomesticPSTNDisabled '    |    Der Benutzer in der Konferenz kann sich nur an inländische Rufnummern anwählen, und dieser Nutzer kann außer Notrufnummern keine ausgehenden Anrufe an eine PSTN-Nummer tätigen.    |
|    Identity = ' Tag: DialoutCPCDisabledPSTNDomestic '    |    Der Benutzer in der Konferenz kann keine Anrufe tätigen, und dieser Benutzer kann nur ausgehende Anrufe an inländische PSTN-Nummern tätigen.    |
|    Identity = ' Tag: DialoutCPCandPSTNDisabled '    |    Der Benutzer in der Konferenz kann keine Auswahlen vornehmen, und dieser Benutzer kann außer Notrufnummern keine ausgehenden Anrufe an eine PSTN-Nummer tätigen.    |
|    Identity = ' Tag: DialoutCPCZoneAPSTNInternational '    |    Der Benutzer in der Konferenz kann nur in die [Zone A Länder und Regionen](audio-conferencing-zones.md)wählen, und dieser Benutzer kann ausgehende Anrufe an Auslands-und Inlands Nummern tätigen.    |
|    Identity = ' Tag: DialoutCPCZoneAPSTNDomestic '    |    Der Benutzer in der Konferenz kann nur in die [Zone A Countries (Länder und Regionen](audio-conferencing-zones.md)) wählen, und dieser Benutzer kann nur ausgehende Anrufe an eine inländische PSTN-Nummer tätigen.    |
|    Identity = ' Tag: DialoutCPCZoneAPSTNDisabled '    |    Der Benutzer in der Konferenz kann sich nur in die [Zone A Countries (Länder) und Regionen](audio-conferencing-zones.md)einwählen, und dieser Nutzer kann nicht außer Notrufnummern ausgehende Anrufe an eine PSTN-Nummer tätigen.    |
