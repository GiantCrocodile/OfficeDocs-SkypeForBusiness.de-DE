---
title: Verwalten von Besprechungsrichtlinien
author: tonysmit
ms.author: tonysmit
manager: serdars
ms.topic: article
ms.service: msteams
ms.reviewer: sonua, shalenc
audience: admin
localization_priority: Normal
search.appverid: MET150
ms.collection:
- M365-collaboration
- m365initiative-meetings
appliesto:
- Microsoft Teams
f1.keywords:
- CSH
ms.custom:
- ms.teamsadmincenter.meetingpolicies.overview
- ms.teamsadmincenter.meetingpolicies.audioandvideo
- ms.teamsadmincenter.meetingpolicies.contentsharing
- ms.teamsadmincenter.meetingpolicies.general
- ms.teamsadmincenter.meetingpolicies.participantandguests
- seo-marvel-apr2020
description: Erfahren Sie, wie Sie die Einstellungen für Besprechungsrichtlinien in Teams verwalten und verwenden, um die für Besprechungsteilnehmer verfügbaren Features für Besprechungen zu steuern, die von Benutzern geplant werden.
ms.openlocfilehash: 8d701f32cbaf133b03573394d48772b12488b8fe
ms.sourcegitcommit: eaab12a7a760f8a197632e1d28773728b5d1dcef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429396"
---
# <a name="manage-meeting-policies-in-teams"></a>Verwalten von Besprechungsrichtlinien in Teams

::: zone target="docs"
Besprechungsrichtlinien werden verwendet, um die Features zu steuern, die Besprechungsteilnehmern für Besprechungen, die von Benutzern in Ihrer Organisation geplant werden, zur Verfügung stehen. Sie können die Global (org-Wide Standard)-Richtlinie verwenden, die automatisch erstellt wird, oder benutzerdefinierte Richtlinien erstellen und zuweisen. Sie können Besprechungsrichtlinien im Microsoft Teams Admin Center oder mithilfe von [PowerShell](teams-powershell-overview.md)verwalten.

> [!NOTE]
> Informationen zum Verwenden von Rollen zum Verwalten der Berechtigungen von besprechungsreferenten und Teilnehmern finden Sie unter [Rollen in einer Teambesprechung](https://support.microsoft.com/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019?ui=en-us&rs=en-us&ad=us).

Sie können Richtlinien wie folgt implementieren, die sich auf die Besprechungs Erfahrung für Benutzer auswirken, bevor eine Besprechung beginnt, während einer Besprechung oder nach einer Besprechung.

|Implementierungs  |Beschreibung  |
|---------|---------|
|Pro Organisator    |Wenn Sie eine Richtlinie pro Organisation implementieren, erben alle Besprechungsteilnehmer die Richtlinie des Organisators. So ist beispielsweise " **Personen automatisch zulassen** " eine Richtlinie pro Organisator und steuert, ob Benutzer direkt an der Besprechung teilnehmen oder in der Lobby auf Besprechungen warten, die der Benutzer, dem die Richtlinie zugewiesen ist, geplant hat.          |
|Pro Benutzer    |Wenn Sie eine Richtlinie pro Benutzer implementieren, gilt nur die Richtlinie pro Benutzer, um bestimmte Features für den Organisator und/oder die Besprechungsteilnehmer zu beschränken. So ist beispielsweise die Option "jetzt besprechen" **in Kanälen** eine Richtlinie pro Benutzer.     |
|Pro Organisator und pro Benutzer     |Wenn Sie eine Kombination aus einer pro-Organizer-und pro-Benutzer-Richtlinie implementieren, sind bestimmte Features für Besprechungsteilnehmer basierend auf Ihrer Richtlinie und der Richtlinie des Organisators eingeschränkt. So können Sie beispielsweise für die **Cloud-Aufzeichnung** eine pro-Organizer-und pro-Benutzer-Richtlinie verwenden. Aktivieren Sie diese Einstellung, damit der Besprechungsorganisator und die Teilnehmer eine Aufzeichnung starten und beenden können.

Sie können die Einstellungen in der globalen Richtlinie bearbeiten oder eine oder mehrere benutzerdefinierte Richtlinien erstellen und zuweisen. Benutzer erhalten die globale Richtlinie, es sei denn, Sie erstellen eine benutzerdefinierte Richtlinie und weisen diese zu.

> [!NOTE]
> Die Schaltfläche "Besprechungsdetails" steht zur Verfügung, wenn ein Benutzer die Audiokonferenz-Lizenzen aktiviert hat oder wenn der Benutzer eine Audiokonferenz zugelassen hat, wenn dies nicht der Fall ist, werden die Besprechungsdetails nicht zur Verfügung stehen.

## <a name="create-a-custom-meeting-policy"></a>Erstellen einer benutzerdefinierten Besprechungsrichtlinie

1. Wechseln Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu **Meetings**  >  **Besprechungsrichtlinien** für Besprechungen.
2. Klicken Sie auf **Hinzufügen**.
3. Geben Sie eine Bezeichnung und eine Beschreibung für die Richtlinie ein. Der Name darf keine Sonderzeichen enthalten und nicht mehr als 64 Zeichen lang sein.
4. Wählen Sie die gewünschten Einstellungen aus.
5. Wählen Sie **Speichern** aus.

Nehmen wir beispielsweise an, Sie haben eine Gruppe von Nutzern, und Sie möchten die Bandbreite begrenzen, die für Ihre Besprechung erforderlich ist. Sie erstellen dann eine neue benutzerdefinierte Richtlinie namens „begrenzte Bandbreite“ und deaktivieren die folgenden Einstellungen:

Unter **Audio & Video**:

- Deaktivieren Sie Cloud-Aufzeichnung zulassen.
- Deaktivieren Sie IP-Video zulassen.

Unter **Inhaltsfreigabe**:

- Deaktivieren Sie den Bildschirmfreigabemodus.
- Deaktivieren Sie Whiteboard zulassen.
- Deaktivieren Sie Freigegebene Notizen zulassen.

Weisen Sie dann die Richtlinie den Nutzern zu.

## <a name="edit-a-meeting-policy"></a>Bearbeiten einer Besprechungsrichtlinie

Sie können die globale Richtlinie und alle von Ihnen erstellten benutzerdefinierten Richtlinien bearbeiten.

1. Wechseln Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu **Meetings**  >  **Besprechungsrichtlinien** für Besprechungen.
2. Wählen Sie die Richtlinie aus, indem Sie links neben dem Richtliniennamen klicken, und wählen Sie dann **Bearbeiten** aus.
3. Nehmen Sie hier die gewünschten Änderungen vor.
4. Wählen Sie **Speichern** aus.

> [!NOTE]
> Einem Benutzer kann immer nur eine Besprechungsrichtlinie zugewiesen werden.

## <a name="assign-a-meeting-policy-to-users"></a>Nutzern eine Besprechungsrichtlinie zuweisen

[!INCLUDE [assign-policy](includes/assign-policy.md)]

> [!NOTE]
> Sie können eine Richtlinie nicht löschen, solange Sie Benutzern zugewiesen ist. Sie müssen allen betroffenen Benutzern erst eine andere Richtlinie zuweisen, bevor Sie die ursprüngliche Richtlinie löschen können.

## <a name="meeting-policy-settings"></a>Einstellungen für Besprechungsrichtlinien

Wenn Sie auf der Seite **Besprechungsrichtlinien** eine vorhandene Richtlinie auswählen oder auf **Hinzufügen** klicken, um eine neue Richtlinie hinzuzufügen, können Sie die Einstellungen für Folgendes konfigurieren.

- [Allgemein](#meeting-policy-settings---general)
- [Audio & Video](#meeting-policy-settings---audio--video)
- [Inhaltsfreigabe](#meeting-policy-settings---content-sharing)
- [Teilnehmer & Gäste](#meeting-policy-settings---participants--guests)

::: zone-end

<a name="bkgeneral"> </a>

## <a name="meeting-policy-settings---general"></a>Einstellungen für Besprechungsrichtlinien – allgemein

- [Sofortbesprechung in Kanälen zulassen](#allow-meet-now-in-channels)
- [Zulassen des Outlook-Add-ins](#allow-the-outlook-add-in)
- [Planen der Kanal Besprechung zulassen](#allow-channel-meeting-scheduling)
- [Planen privater Besprechungen zulassen](#allow-scheduling-private-meetings)
- ["Besprechung jetzt in privaten Besprechungen zulassen"](#allow-meet-now-in-private-meetings)

### <a name="allow-meet-now-in-channels"></a>Sofortbesprechung in Kanälen zulassen

Die Option " **jetzt** besprechen" ist eine benutzerspezifische Richtlinie, die vor Beginn einer Besprechung gilt. Diese Einstellung steuert, ob ein Benutzer eine ungeplante Besprechung in einem Teams-Kanal starten kann. Wenn Sie diese Einstellung aktivieren, können Benutzer **die Schaltfläche "Besprechung"** auswählen, um eine ungeplante Besprechung zu starten oder eine Besprechung im Kanal zu planen. Der Standardwert lautet „True“.

![Screenshot mit dem Symbol "jetzt besprechen" unter einer Nachricht](media/meeting-policies-meet-now.png) 

### <a name="allow-the-outlook-add-in"></a>Zulassen des Outlook-Add-ins

Hierbei handelt es sich um eine benutzerspezifische Richtlinie, die vor dem Beginn einer Besprechung gilt. Mit dieser Einstellung wird gesteuert, ob Teams-Besprechungen in Outlook (Windows, Mac, Web und Mobile) geplant werden können.

![Screenshot, der zeigt, wie Sie eine neue Besprechung planen können](media/meeting-policies-outlook-add-in.png)

Wenn Sie diese Option deaktivieren, können die Benutzer nicht mehr planen. Teambesprechungen, wenn Sie in Outlook eine neue Besprechung erstellen. In Outlook unter Windows wird beispielsweise die Option **neue Teams-Besprechung** nicht im Menüband angezeigt.

### <a name="allow-channel-meeting-scheduling"></a>Planen der Kanal Besprechung zulassen

Verwenden Sie die vorhandene AllowChannelMeetingScheduling-Richtlinie, um die Typen von Ereignissen zu steuern, die in den Team Kanal Kalendern erstellt werden können. Hierbei handelt es sich um eine benutzerspezifische Richtlinie, die vor dem Beginn einer Besprechung gilt. Diese Einstellung steuert, ob Benutzer eine Besprechung in einem Teams-Kanal planen können. Diese Einstellung ist standardmäßig aktiviert.

Wenn diese Richtlinie deaktiviert ist, können Benutzer keine neuen Kanal Besprechungen erstellen. Vorhandene Kanal Besprechungen können jedoch vom Organisator des Ereignisses bearbeitet werden.

Planen einer Besprechung wird deaktiviert.

 ![Screenshot der Option "Besprechung planen" in Teams](media/schedule-meeting-option.png)

Kanalauswahl ist deaktiviert.

![die Kalender Option zum Auswählen eines Kanals, in dem Sie eine Besprechung planen möchten.](media/meeting-policies-select-a-channel-to-meet-in.png)

Auf der Seite Kanal Beiträge werden die folgenden Features deaktiviert:

- Schaltfläche ' **Besprechung planen** ' im Feld ' Antwort verfassen '
  ![Feld ' Besprechung planen '](media/schedule-meeting-disabled-in-chat2.png)
  
- Schaltfläche " **Besprechung planen** " im Kanal Kopf
  ![Schaltfläche "Besprechung planen" im Kanal Kopf](media/schedule-now-in-header.png)

Im Kanal Kalender:

- Schaltfläche " **Neues Ereignis hinzufügen** " im Kanal Kalender-Header wird deaktiviert.
  ![Schaltfläche auf der Kanal Kalender Kopfzeile deaktiviert](media/add-new-event-disabled.png)

- Benutzer können keinen Zeit Block im Kanal Kalender ziehen und auswählen, um eine Kanal Besprechung zu erstellen.

- Benutzer können keine Tastenkombinationen zum Erstellen einer Besprechung im Kanal Kalender verwenden.

Im Admin Center:

Die Kanal Kalender-APP wird im Abschnitt **Microsoft-apps** auf der Seite App-Berechtigungsrichtlinien angezeigt.

 ![die APP-Berechtigungsrichtlinie im Team Admin Center](media/manage-microsoft-apps-policy.png)

### <a name="allow-scheduling-private-meetings"></a>Planen privater Besprechungen zulassen

Hierbei handelt es sich um eine benutzerspezifische Richtlinie, die vor dem Beginn einer Besprechung gilt. Diese Einstellung steuert, ob Benutzer private Besprechungen in Teams planen können. Eine Besprechung ist privat, wenn Sie nicht in einem Kanal in einem Team veröffentlicht wurde.

Beachten Sie Folgendes: Wenn Sie die Option " **Planen privater Besprechungen zulassen** " deaktivieren und die **Kanal Besprechungsplanung zulassen**, sind die Optionen " **erforderliche Teilnehmer hinzufügen** " und " **Kanal hinzufügen** " für Benutzer in Teams deaktiviert. Diese Einstellung ist standardmäßig aktiviert.

### <a name="allow-meet-now-in-private-meetings"></a>"Besprechung jetzt in privaten Besprechungen zulassen"

Hierbei handelt es sich um eine benutzerspezifische Richtlinie, die vor dem Beginn einer Besprechung gilt. Mit dieser Einstellung wird gesteuert, ob ein Benutzer eine ungeplante private Besprechung starten kann.  Diese Einstellung ist standardmäßig aktiviert.

<a name="bkaudioandvideo"> </a>

## <a name="meeting-policy-settings---audio--video"></a>Einstellungen für Besprechungsrichtlinien – Audio & Video

- [Transkription zulassen](#allow-transcription)
- [Cloud-Aufzeichnung zulassen](#allow-cloud-recording)
- [Modus für IP-Audio](#mode-for-ip-audio)
- [Modus für IP-Video](#mode-for-ip-video)
- [IP-Video zulassen](#allow-ip-video)
- [Medien-Bitrate (KBS)](#media-bit-rate-kbs)

### <a name="allow-transcription"></a>Transkription zulassen

Hierbei handelt es sich um eine Kombination aus einer pro-Organizer-und pro-User-Richtlinie. Mit dieser Einstellung wird gesteuert, ob Beschriftungen und Transkriptions Features bei der Wiedergabe von Besprechungsaufzeichnungen zur Verfügung stehen. Wenn Sie diese Option deaktivieren, stehen die Optionen " **Suchen** " und " **CC** " während der Wiedergabe einer Besprechungsaufzeichnung nicht zur Verfügung. Die Person, die die Aufzeichnung gestartet hat, muss diese Einstellung aktiviert haben, damit die Aufzeichnung auch Transkription umfasst.

Beachten Sie, dass die Transkription für aufgezeichnete Besprechungen derzeit nur für Benutzer unterstützt wird, für die die Sprache in Teams auf Englisch festgesetzt ist und wenn Englisch in der Besprechung gesprochen wird.

![die Transkriptions Optionen in einer Besprechung](media/meeting-policies-transcription.png)

### <a name="allow-cloud-recording"></a>Cloud-Aufzeichnung zulassen

Hierbei handelt es sich um eine Kombination aus einer pro-Organizer-und pro-User-Richtlinie. Diese Einstellung steuert, ob die Besprechungen dieses Benutzers aufgezeichnet werden können. Die Aufzeichnung kann vom Besprechungsorganisator oder von einem anderen Besprechungsteilnehmer gestartet werden, wenn die Richtlinieneinstellung für den Teilnehmer aktiviert ist und es sich um einen authentifizierten Benutzer aus derselben Organisation handelt.

Personen außerhalb Ihrer Organisation, wie etwa Föderations-und anonyme Benutzer, können die Aufzeichnung nicht starten. Gastbenutzer können die Aufzeichnung nicht starten oder beenden.

![die Aufzeichnungsoptionen](media/meeting-policies-recording.png)

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie  |Cloud-Aufzeichnung zulassen |
|---------|---------|---------|
|Daniela | Global   | Aus |
|Amanda | Location1MeetingPolicy | Ein|
|John (externer Benutzer) | Nicht zutreffend | Nicht zutreffend|

Von Daniela organisierte Besprechungen können nicht aufgezeichnet werden, und Amanda, deren Richtlinieneinstellung aktiviert ist, kann keine von Daniela organisierten Besprechungen aufzeichnen. Von Amanda organisierte Besprechungen können aufgezeichnet werden, doch Daniela, die die Richtlinieneinstellung deaktiviert hat, und John, der ein externer Benutzer ist, kann keine von Amanda organisierten Besprechungen aufzeichnen.

Weitere Informationen zur Aufzeichnung von Cloud-Besprechungen finden Sie unter [Cloud-Besprechungsaufzeichnung in Teams](cloud-recording.md).

### <a name="mode-for-ip-audio"></a>Modus für IP-Audio

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Diese Einstellung steuert, ob Audio in Besprechungen und Gruppen anrufen aktiviert werden kann. Hier sind die Werte für diese Einstellung.

|Einstellungswert |Verhalten  |
|---------|---------|
|**Ausgehendes und eingehendes Audiosignal aktiviert**    |Ausgehende und eingehende Audiodaten sind in der Besprechung zulässig. Dies ist die Standardeinstellung. |
|**Deaktiviert**     |Ausgehende und eingehende Audiodaten werden in der Besprechung deaktiviert.     |

Wenn Sie für einen Benutzer auf **deaktiviert** festgesetzt ist, kann dieser Benutzer weiterhin Besprechungen planen und organisieren, jedoch keine Audiofunktionen verwenden. Wenn Sie an einer Besprechung teilnehmen möchten, müssen Sie sich über das öffentlich geschaltete Telefonnetz (PSTN) einwählen oder den Besprechungs Anruf führen und sich per Telefon daran beteiligen. Für Besprechungsteilnehmer, denen keine Richtlinien zugewiesen sind (beispielsweise anonyme Teilnehmer), ist diese Option auf **Ausgehendes und eingehendes Audio** standardmäßig aktiviert. Wenn diese Einstellung deaktiviert ist, muss sich der Benutzer auf Teams Mobile Clients über das PSTN in die Besprechung einwählen.

Diese Einstellung gilt nicht für 1:1-Anrufe. Wenn Sie 1:1-Anrufe einschränken möchten, konfigurieren Sie eine [Anrufrichtlinie](teams-calling-policy.md) für Teams, und deaktivieren Sie die Einstellung **private Anrufe tätigen** . Diese Einstellung gilt auch nicht für Konferenzraum Geräte wie Surface Hub und Microsoft Teams rooms Devices.

Diese Einstellung steht noch nicht für Microsoft 365 Government Community Cloud (gcc), gcc-höchst-oder Department of Defense (DoD)-Umgebungen zur Verfügung.

Weitere Informationen finden Sie unter [Verwalten von Audio/Video für Besprechungsteilnehmer](#manage-audiovideo-for-meeting-participants).

### <a name="mode-for-ip-video"></a>Modus für IP-Video

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Diese Einstellung steuert, ob Video in Besprechungen und Gruppen anrufen aktiviert werden kann. Hier sind die Werte für diese Einstellung.

|Einstellungswert |Verhalten  |
|---------|---------|
|**Ausgehendes und eingehendes Video aktiviert**    | Ein-und ausgehendes Video ist in der Besprechung zulässig. Dies ist die Standardeinstellung. |
|**Deaktiviert**     | Ein-und ausgehendes Video wird in der Besprechung deaktiviert. Auf mobilen Teams können Benutzer keine Videos oder Fotos in der Besprechung freigeben. <br><br>Beachten Sie, dass der Modus für IP- **Video** auch deaktiviert bleibt, wenn der **Modus für IP-Audio** deaktiviert ist.  |

Wenn diese Option für einen Benutzer **deaktiviert** ist, kann dieser Benutzer Video oder Videos, die von anderen Besprechungsteilnehmern freigegeben wurden, nicht aktivieren. Für Besprechungsteilnehmer, denen keine Richtlinien zugewiesen sind (beispielsweise anonyme Teilnehmer), ist diese Option auf **Ausgehendes und eingehendes Video** standardmäßig aktiviert.

Diese Einstellung gilt nicht für Konferenzraum Geräte wie Surface Hub und Microsoft Teams rooms Devices.

Diese Einstellung steht noch nicht für Microsoft 365 Government Community Cloud (gcc), gcc-höchst-oder Department of Defense (DoD)-Umgebungen zur Verfügung.

> [!NOTE]
> Beachten Sie, dass diese Einstellung sowohl das ausgehende als auch das eingehende Video steuert, während die **IP-Videoeinstellung Allow** das ausgehende Video steuert. Weitere Informationen finden Sie unter [welche IP-Video Richtlinieneinstellung hat Vorrang?](#which-ip-video-policy-setting-takes-precedence) und [Verwalten von Audio/Video für Besprechungsteilnehmer](#manage-audiovideo-for-meeting-participants).

Weitere Informationen finden Sie unter [Verwalten von Audio/Video für Besprechungsteilnehmer](#manage-audiovideo-for-meeting-participants).

### <a name="allow-ip-video"></a>IP-Video zulassen

Hierbei handelt es sich um eine Kombination aus einer pro-Organizer-und pro-User-Richtlinie. Video ist eine wichtige Komponente für Besprechungen. In einigen Organisationen möchten Administratoren möglicherweise mehr Kontrolle darüber haben, welche Benutzer Besprechungen Video haben. Mit dieser Einstellung wird gesteuert, ob Video in Besprechungen, die von einem Benutzer gehostet werden, und in 1:1 und von einem Benutzer gestartete Gruppenanrufe aktiviert werden können. Auf mobilen Teams-Clients steuert diese Einstellung, ob Benutzer Fotos und Videos in einer Besprechung freigeben können.

Besprechungen, die von einem Benutzer organisiert werden, für den diese Richtlinieneinstellung aktiviert ist, ermöglichen die Videofreigabe in der Besprechung durch die Besprechungsteilnehmer, wenn die Richtlinieneinstellung für die Teilnehmer ebenfalls aktiviert ist. Besprechungsteilnehmern, denen keine Richtlinien zugewiesen sind (beispielsweise anonyme und verbundene Teilnehmer) erben die Richtlinie des Besprechungsorganisators.

> [!NOTE]
> Beachten Sie, dass diese Einstellung ausgehendes Video steuert, während der **Modus für IP-Video** Einstellungen sowohl ausgehende als auch eingehende Videos steuert. Weitere Informationen finden Sie unter [welche IP-Video Richtlinieneinstellung hat Vorrang?](#which-ip-video-policy-setting-takes-precedence) und [Verwalten von Audio/Video für Besprechungsteilnehmer](#manage-audiovideo-for-meeting-participants).

| Teams-Desktop und WebClient |Mobiler Client für Teams  |
|:-------:|:-------:|
|![Screenshot der Besprechungsteilnahme mit Audio/Video-Einstellungen auf dem Desktop](media/meeting-policies-audio-video-settings.png)    |![Screenshot der Besprechungsteilnahme Sreen mit Audio/Video-Einstellungen auf mobilen Geräten](media/meeting-policies-mobile-join.png)          |

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie  |IP-Video zulassen |
|---------|---------|---------|
|Daniela   | Global   | Ein       |
|Amanda    | Location1MeetingPolicy        | Aus      |

Von Daniela moderierte Besprechungen ermöglichen das Aktivieren von Videos. Daniela kann an der Besprechung teilnehmen und Video aktivieren. Amanda kann in Danielas Besprechung kein Video einschalten, weil Amandas Richtlinie so eingestellt ist, dass Video nicht zulässig ist. Amanda kann Videos sehen, die von anderen Teilnehmern an der Besprechung freigegeben wurden.

In Besprechungen, die von Amanda gehostet werden, kann niemand Video unabhängig von der Ihnen zugewiesenen Video Richtlinie aktivieren. Das bedeutet, dass Daniela in Amandas Besprechungen kein Video einschalten kann.  

Wenn Daniela Amanda mit Video anruft, kann Amanda den Anruf nur mit Audio annehmen.  Wenn der Anruf verbunden ist, kann Amanda Danielas Video sehen, kann aber kein Video aktivieren. Wenn Amanda Daniela anruft, kann Daniela den Anruf mit Video und Audio annehmen. Wenn der Anruf verbunden ist, kann Daniela sein Video nach Bedarf aktivieren oder deaktivieren.

Weitere Informationen finden Sie unter [Verwalten von Audio/Video für Besprechungsteilnehmer](#manage-audiovideo-for-meeting-participants).

#### <a name="which-ip-video-policy-setting-takes-precedence"></a>Welche IP-Video Richtlinieneinstellung Vorrang hat

Für einen Benutzer hat die restriktivste Richtlinieneinstellung für Video Vorrang. Hier sind einige Beispiele.

|IP-Video zulassen|Modus für IP-Video|Besprechungs Erfahrung|
|---------|---------|---------|
|Organisator: **ein**<br><br>Teilnehmer: **ein** |Teilnehmer: **deaktiviert**        |Die Einstellung **"Modus für IP-Video"** hat Vorrang. Der Teilnehmer, dem diese Richtlinie zugewiesen ist, kann Videos, die von anderen Personen freigegeben wurden, nicht aktivieren oder anzeigen.|
|Organisator: **ein**<br><br>Teilnehmer: **ein** |Teilnehmer: **Ausgangs-und eingehendes Video aktiviert**          |Der Teilnehmer, dem diese Richtlinie zugewiesen ist, kann Videos, die von anderen Personen freigegeben wurden, aktivieren oder anzeigen.         |
|Organisator: **ein**<br><br>Teilnehmer: **aus** |Teilnehmer: **Ausgangs-und eingehendes Video aktiviert**         |Die Einstellung " **IP-Video zulassen** " hat Vorrang. Teilnehmer können nur eingehendes Video sehen und können kein ausgehendes Video senden.         |
|Organisator: **ein**<br><br>Teilnehmer: **aus** |Teilnehmer: **deaktiviert**         |Die Einstellung **"Modus für IP-Video"** hat Vorrang. Der Teilnehmer kann ein-oder ausgehendes Video nicht sehen.|
|Organisator: **aus**    |       |Die Einstellung **IP-Video zulassen** hat Vorrang, da Sie für den Organisator deaktiviert ist. Niemand kann Video in Besprechungen aktivieren, die von dem Benutzer organisiert werden, dem diese Richtlinie zugewiesen ist.         |

### <a name="manage-audiovideo-for-meeting-participants"></a>Verwalten von Audio/Video für Besprechungsteilnehmer

|Wenn Sie möchten...  |Festlegen der folgenden Richtlinieneinstellungen  |
|---------|---------|
|Deaktivieren von Audio und Video für Teilnehmer an Besprechungen  |Modus für IP-Audio: **deaktiviert**<br> Modus für IP-Video: **deaktiviert**<br>IP-Video zulassen: N/A       |
|Nur eingehendes Video und Audio für Teilnehmer an Besprechungen aktivieren  |Modus für IP-Audio: **aktiviertes ausgehendes und eingehendes Audiosignal**<br> Modus für IP-Video: **Ausgangs-und eingehender Video aktiviert**<br>IP-Video zulassen: **aus**       |
|Video für Teilnehmer an Besprechungen deaktivieren (die Teilnehmer haben nur Audio)|  Modus für IP-Audio: **Aktivieren von ausgehenden und eingehenden Audiodaten**<br> Modus für IP-Video: **deaktiviert**<br>IP-Video zulassen: N/A
|Aktivieren von Audio und Video für Teilnehmer an Besprechungen    |Modus für IP-Audio: **aktiviertes ausgehendes und eingehendes Audiosignal** (Standard)<br> Modus für IP-Video: **Ausgangs-und eingehender Video aktiviert** (Standard)<br>IP-Video zulassen: **ein** (Standard)    |

Die restriktivste Richtlinie zwischen der Richtlinie des Besprechungsorganisators und der Richtlinie des Benutzers gilt. Wenn beispielsweise ein Organisator über eine Richtlinie verfügt, die das Video einschränkt, und die Richtlinie des Benutzers das Video nicht beschränkt, erben Besprechungsteilnehmer die Richtlinie des Besprechungsorganisators und haben keinen Zugriff auf Video in Besprechungen. Das bedeutet, dass Sie nur mit Audio an der Besprechung teilnehmen können.

> [!NOTE]
> Wenn ein Benutzer einen Gruppenanruf annimmt, um sich per Telefon anzumelden, wird der Bildschirm " **Telefon für Audio verwenden** " nicht angezeigt. Hierbei handelt es sich um ein bekanntes Problem, das gelöst werden muss. Um dieses Problem zu umgehen, wählen Sie unter **andere Verknüpfungsoptionen** die Option **Telefon Audio** aus.  

#### <a name="teams-mobile-clients"></a>Mobile Clients für Teams

Für Benutzer von mobilen Team-Clients wird die Möglichkeit, Fotos und Videos während einer Besprechung freizugeben, auch durch die Einstellung **IP-Video** -oder **IP-Videomodus** zulassen festgelegt. Je nachdem, welche Richtlinieneinstellung Vorrang hat, steht die Möglichkeit zum Freigeben von Videos und Fotos nicht zur Verfügung. Dies wirkt sich nicht auf die Bildschirmfreigabe aus, die Sie mithilfe einer separaten Einstellung für den [Bildschirmfreigabe Modus](#screen-sharing-mode) konfigurieren. Darüber hinaus können Sie eine [Mobilitätsrichtlinie für Teams](https://docs.microsoft.com/powershell/module/skype/new-csteamsmobilitypolicy) festlegen, um zu verhindern, dass Mobile Benutzer IP-Video über eine Mobil Funkverbindung verwenden, was bedeutet, dass Sie eine WLAN-Verbindung verwenden müssen.

### <a name="media-bit-rate-kbs"></a>Medien-Bitrate (KBS)

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Diese Einstellung bestimmt die Medien Bitrate für Audio-, Video-und videobasierte App-Freigabe Übertragungen in anrufen und Besprechungen für den Benutzer. Sie wird sowohl auf den aufwärts-als auch den Downlink-Medien Durchlauf für Benutzer im Anruf oder in der Besprechung angewendet. Mit dieser Einstellung erhalten Sie eine granulare Kontrolle über die Verwaltung der Bandbreite in Ihrer Organisation. Je nach den von Benutzern benötigten Besprechungs Szenarien empfehlen wir, genügend Bandbreite zur Verfügung zu haben, um eine gute Qualität zu erzielen. Der Mindestwert beträgt 30 Kbit/s, und der Höchstwert hängt vom Besprechungs Szenario ab. Wenn Sie mehr über die empfohlene Mindestbandbreite für Besprechungen, Anrufe und Live-Events in Teams mit guter Qualität erfahren möchten, lesen Sie [Bandbreitenanforderungen](prepare-network.md#bandwidth-requirements).

Wenn für eine Besprechung nicht genügend Bandbreite zur Verfügung steht, sehen die Teilnehmer eine Meldung, die auf schlechte Netzwerkqualität hinweist.

Für Besprechungen, die die beste Videoqualität benötigen, wie CEO-Board-Meetings und Teams-Live-Events, empfehlen wir, die Bandbreite auf 10 Mbit/s festzulegen. Auch wenn die maximale Benutzererfahrung festgelegt ist, passt sich der Media-Stack für Teams an niedrige Bandbreitenbedingungen an, wenn bestimmte Netzwerkbedingungen je nach Szenario erkannt werden.

## <a name="meeting-policy-settings---content-sharing"></a>Besprechungsrichtlinien Einstellungen – Inhaltsfreigabe

- [Bildschirmübertragungsmodus](#screen-sharing-mode)
- [Zulassen, dass ein Teilnehmer die Steuerung erteilt oder anfordert](#allow-a-participant-to-give-or-request-control)
- [Zulassen, dass ein externer Teilnehmer die Steuerung erteilt oder anfordert](#allow-an-external-participant-to-give-or-request-control)
- [PowerPoint-Freigabe zulassen](#allow-powerpoint-sharing)
- [Whiteboard zulassen](#allow-whiteboard)
- [Zulassen von freigegebenen Notizen](#allow-shared-notes)

### <a name="screen-sharing-mode"></a>Bildschirmübertragungsmodus

> [!Note]
> Diese Funktion befindet sich noch in der Entwicklung. Bei der Bildschirmfreigabe handelt es sich um eine Richtlinie pro Teilnehmer.

Mit dieser Einstellung wird gesteuert, ob die Desktop-und/oder Fenster Freigabe in der Besprechung des Benutzers zulässig ist. Besprechungsteilnehmern, denen keine Richtlinien zugewiesen sind (beispielsweise anonyme, Gast-, B2B-und Verbund Teilnehmer) erben die Richtlinie des Besprechungsorganisators.

|Einstellungswert |Verhalten  |
|---------|---------|
|**Ganzer Bildschirm**    | Vollständige Desktopfreigabe und Anwendungsfreigabe sind in der Besprechung zulässig |
|**Einzelne Anwendung**   | Die Anwendungsfreigabe ist in der Besprechung zulässig.        |
|**Deaktiviert**     |Bildschirmübertragung und Anwendungsfreigabe in der Besprechung deaktiviert.       |

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie |Bildschirmübertragungsmodus |
|---------|---------|---------|
|Daniela  | Global   | Ganzer Bildschirm |
|Amanda   | Location1MeetingPolicy  | Deaktiviert |

Von Daniela moderierte Besprechungen ermöglichen Besprechungsteilnehmern, ihren gesamten Bildschirm oder eine bestimmte Anwendung freizugeben. Wenn Amanda an Danielas Besprechung teilnimmt, kann Amanda Ihren Bildschirm oder eine bestimmte Anwendung nicht freigeben, da ihre Richtlinieneinstellung deaktiviert ist. In Besprechungen, die von Amanda gehostet werden, darf niemand Ihren Bildschirm oder eine einzelne Anwendung freigeben, unabhängig von der Ihnen zugewiesenen Richtlinie für den Bildschirmfreigabe Modus. Das bedeutet, dass Daniela Ihren Bildschirm oder eine einzige Anwendung nicht in Amandas Besprechungen freigeben kann.  

Zurzeit können Benutzer keine Videos abspielen oder Ihren Bildschirm in einer Teams-Besprechung freigeben, wenn Sie Google Chrome verwenden.

### <a name="allow-a-participant-to-give-or-request-control"></a>Zulassen, dass ein Teilnehmer die Steuerung erteilt oder anfordert

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Diese Einstellung steuert, ob der Benutzer die Steuerung des freigegebenen Desktops oder Fensters an andere Besprechungsteilnehmer weitergeben kann. Um die Steuerung zu übernehmen, zeigen Sie auf den oberen Rand des Bildschirms.

Wenn diese Einstellung für den Benutzer aktiviert ist, wird die Option **Steuerung übergeben** in der oberen Leiste einer Freigabesitzung angezeigt.

![Screenshot mit der Option "Steuerung übergeben"](media/meeting-policies-give-control.png)

Wenn die Einstellungen für den Benutzer deaktiviert sind, steht die Option " **Steuerelement angeben** " nicht zur Verfügung.

![Screenshot, der zeigt, dass die Option "Steuerelement angeben" nicht verfügbar ist](media/meeting-policies-give-control-not-available.png)

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie  |Zulassen, dass Teilnehmer die Steuerung erteilen oder anfordern |
|---------|---------|---------|
|Daniela   | Global   | Ein       |
|Babək    | Location1MeetingPolicy        | Aus   |

Daniela kann die Steuerung des freigegebenen Desktops oder Fensters an andere Teilnehmer an einer von Babək organisierten Besprechung übergeben, während Babək anderen Teilnehmern keine Kontrolle geben kann.

Verwenden Sie das AllowParticipantGiveRequestControl-Cmdlet, um mithilfe von PowerShell Steuern zu können, wer Steuerelemente steuern oder akzeptieren kann.

> [!NOTE]
> Um freigegebene Inhalte während der Freigabe zu übernehmen und zu steuern, müssen beide Parteien den Desktop Client von Teams verwenden. Die Steuerung wird nicht unterstützt, wenn eine der beiden Parteien Teams in einem Browser ausführt. Dies ist auf eine technische Einschränkung zurückzuführen, die wir planen zu beheben.

### <a name="allow-an-external-participant-to-give-or-request-control"></a>Zulassen, dass ein externer Teilnehmer die Steuerung erteilt oder anfordert

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Ob diese Gruppe für einen Benutzer von einer Organisation eingerichtet wurde, steuert nicht, was externe Teilnehmer tun können, unabhängig davon, was der Besprechungsorganisator festgestellt hat. Dieser Parameter steuert, ob externen Teilnehmern die Kontrolle über den Bildschirm des Mitarbeiters gewährt werden kann, je nachdem, was der freigaber innerhalb der Besprechungsrichtlinien Ihrer Organisation festgesetzt hat. Externe Teilnehmer an Teams-Besprechungen können wie folgt kategorisiert werden:  

- Anonymer Benutzer
- Gastbenutzer  
- B2B-Nutzer
- Federated-Benutzer  

Ob Verbundbenutzer externen Benutzern die Kontrolle überlassen können, während die Freigabe von **einem externen Teilnehmer** gesteuert wird, der die Steuerungseinstellung in Ihrer Organisation erteilt oder anfordert.

Verwenden Sie das AllowExternalParticipantGiveRequestControl-Cmdlet, um mithilfe von PowerShell Steuern zu können, ob externe Teilnehmer Steuerelemente steuern oder akzeptieren können.

### <a name="allow-powerpoint-sharing"></a>PowerPoint-Freigabe zulassen

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Mit dieser Einstellung wird gesteuert, ob der Benutzer PowerPoint-Folienstapel in einer Besprechung freigeben kann. Externe Benutzer, einschließlich Anonymous-, Guest-und Federated-Benutzer, erben die Richtlinie des Besprechungsorganisators.

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie  |PowerPoint-Freigabe zulassen |
|---------|---------|---------|
|Daniela   | Global   | Ein       |
|Amanda   | Location1MeetingPolicy        | Aus   |

Amanda kann PowerPoint-Folienstapel in Besprechungen auch dann nicht freigeben, wenn Sie der Organisator der Besprechung ist. Daniela kann PowerPoint-Folienstapel auch dann freigeben, wenn die Besprechung von Amanda organisiert ist. Amanda kann die von anderen Personen in der Besprechung freigegebenen PowerPoint-Folienstapel anzeigen, auch wenn Sie PowerPoint-Folienstapel nicht freigeben kann.

### <a name="allow-whiteboard"></a>Whiteboard zulassen

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Mit dieser Einstellung wird gesteuert, ob ein Benutzer das Whiteboard in einer Besprechung freigeben kann. Externe Benutzer, einschließlich anonymen, B2B-und Verbundbenutzern, erben die Richtlinie des Besprechungsorganisators.

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie  |Whiteboard zulassen|
|---------|---------|---------|
|Daniela   | Global   | Ein       |
|Amanda   | Location1MeetingPolicy        | Aus   |

Amanda kann das Whiteboard nicht in einer Besprechung freigeben, auch wenn Sie der Organisator der Besprechung ist. Daniela kann das Whiteboard auch dann freigeben, wenn eine Besprechung von Amanda organisiert ist.  

### <a name="allow-shared-notes"></a>Zulassen von freigegebenen Notizen

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Mit dieser Einstellung wird gesteuert, ob ein Benutzer Notizen in einer Besprechung erstellen und freigeben kann. Externe Benutzer, einschließlich anonymen, B2B-und Verbundbenutzern, erben die Richtlinie des Besprechungsorganisators. Die Registerkarte " **Besprechungsnotizen** " wird derzeit nur in Besprechungen mit weniger als 20 Teilnehmern unterstützt.

Sehen wir uns das folgende Beispiel an:

|Benutzer |Besprechungsrichtlinie  |Zulassen von freigegebenen Notizen |
|---------|---------|---------|
|Daniela   | Global   | Ein       |
|Amanda   | Location1MeetingPolicy | Aus |

Daniela kann in Amandas Besprechungen Notizen machen, und Amanda kann in keiner Besprechung Notizen machen.

## <a name="meeting-policy-settings---participants--guests"></a>Besprechungsrichtlinien Einstellungen – Teilnehmer & Gäste

Diese Einstellungen steuern, welche Besprechungsteilnehmer in der Lobby warten, bevor Sie an der Besprechung teilnehmen, sowie die Teilnahmestufe, die Sie in einer Besprechung zugelassen sind.

- [Zulassen, dass anonyme Personen eine Besprechung starten](#let-anonymous-people-start-a-meeting)
- [Automatisches zulassen von Personen](#automatically-admit-people)
- [Zulassen, dass Einwahlbenutzer die Lobby umgehen können](#allow-dial-in-users-to-bypass-the-lobby)
- [Aktivieren von Live Beschriftungen](#enable-live-captions)
- [Chat in Besprechungen zulassen](#allow-chat-in-meetings)

> [!NOTE]
>Die Optionen für die Teilnahme an einer Besprechung unterscheiden sich je nach den Einstellungen für die einzelnen Teams und der Verbindungsmethode. Wenn Ihre Gruppe über Audiokonferenzen verfügt und diese zum Herstellen einer Verbindung verwendet, lesen Sie [Audiokonferenzen](https://docs.microsoft.com/microsoftteams/audio-conferencing-in-office-365). Wenn Ihre Gruppe "Teams" keine Audiokonferenzen hat, lesen Sie [teilnehmen an einer Besprechung in Teams](https://support.office.com/article/join-a-meeting-in-teams-1613bb53-f3fa-431e-85a9-d6a91e3468c9).

### <a name="let-anonymous-people-start-a-meeting"></a>Zulassen, dass anonyme Personen eine Besprechung starten

Hierbei handelt es sich um eine Richtlinie für einzelne Organisatoren, die die Besprechungen mit Einwahlkonferenzen ermöglicht. Mit dieser Einstellung wird gesteuert, ob Einwahlbenutzer an der Besprechung teilnehmen können, ohne dass ein authentifizierter Benutzer von der Organisation anwesend ist. Diese Einstellung ist standardmäßig deaktiviert, was bedeutet, dass Einwahlbenutzer in der Wartebereich warten, bis ein authentifizierter Benutzer aus der Organisation der Besprechung beigetreten ist.

> [!NOTE]
> Wenn diese Einstellung deaktiviert ist und ein Einwahlbenutzer zuerst an der Besprechung teilnimmt und sich in der Lobby befindet, muss ein Organisationsbenutzer an der Besprechung mit einem Team-Clientteil nehmen, um den Benutzer aus der Lobby zuzulassen. Es gibt keine Lobby-Steuerelemente, die für gewählte Benutzer verfügbar sind.

### <a name="automatically-admit-people"></a>Automatisches zulassen von Personen

Hierbei handelt es sich um eine Richtlinie pro Organisator. Mit dieser Einstellung wird gesteuert, ob Personen direkt an einer Besprechung teilnehmen oder in der Lobby warten, bis Sie von einem authentifizierten Benutzer zugelassen werden. Diese Einstellung gilt nicht für Einwahlbenutzer.

![Screenshot einer Besprechung mit einem Benutzer in der Lobby](media/meeting-policies-lobby.png)

 Besprechungsorganisatoren können in der Besprechungseinladung auf **Besprechungsoptionen** klicken, um diese Einstellung für jede von Ihnen geplante Besprechung zu ändern.

> [!NOTE]
> In den Besprechungsoptionen ist die Einstellung mit "Wer kann die Lobby umgehen" gekennzeichnet. Wenn Sie die Standardeinstellung für einen beliebigen Benutzer ändern, gilt dies für alle neuen Besprechungen, die von diesem Benutzer organisiert werden, sowie für alle vorherigen Besprechungen, in denen der Benutzer die Besprechungsoptionen nicht geändert hat.
  
|Einstellungswert  |Join-Verhalten |
|---------|---------|
|**Jeder**   |Alle Besprechungsteilnehmer werden direkt an der Besprechung teilnehmen, ohne in der Lobby zu warten. Dazu gehören authentifizierte Benutzer, externe Benutzer von vertrauenswürdigen Organisationen (Federated), Gäste und anonyme Benutzer.     |
|**Jeder in Ihrer Organisation und in Verbundorganisationen**     |Authentifizierte Benutzer innerhalb der Organisation, einschließlich Gastbenutzer und die Benutzer aus vertrauenswürdigen Organisationen, werden direkt an der Besprechung teilnehmen, ohne in der Lobby zu warten.  Anonyme Benutzer warten in der Lobby.   |
|**Jeder in Ihrer Organisation**    |Authentifizierte Benutzer innerhalb der Organisation, einschließlich Gastbenutzer, nehmen an der Besprechung direkt Teil, ohne in der Lobby zu warten.  Benutzer von vertrauenswürdigen Organisationen und anonymen Benutzern warten in der Lobby. Dies ist die Standardeinstellung.           |
|**Nur Organisator**    |Nur Besprechungsorganisatoren können direkt an der Besprechung teilnehmen, ohne in der Lobby warten zu müssen. Alle anderen Personen, einschließlich authentifizierter Benutzer innerhalb der Organisation, Gastbenutzer, Benutzer von vertrauenswürdigen Organisationen und anonyme Benutzer müssen in der Lobby warten.           |

### <a name="allow-dial-in-users-to-bypass-the-lobby"></a>Zulassen, dass Einwahlbenutzer die Lobby umgehen können

Hierbei handelt es sich um eine Richtlinie pro Organisator. Diese Einstellung steuert, ob Personen, die sich per Telefon einwählen, direkt an der Besprechung teilnehmen oder in der Lobby warten, unabhängig von der Einstellung " **Personen automatisch zulassen** ". Diese Einstellung ist standardmäßig deaktiviert. Wenn diese Einstellung deaktiviert ist, warten Einwahlbenutzer in der Lobby, bis ein Organisationsbenutzer die Besprechung mit einem Team-Client verknüpft und diese zulässt. Wenn diese Einstellung aktiviert ist, werden Einwahlbenutzer automatisch an der Besprechung teilnehmen, wenn ein Organisationsbenutzer der Besprechung Beitritt.

> [!NOTE]
> Wenn ein Einwahlbenutzer an einer Besprechung teilnimmt, bevor ein Organisationsbenutzer der Besprechung Beitritt, wird er in der Lobby gespeichert, bis ein Organisationsbenutzer die Besprechung mit einem Team-Client verknüpft und diese zulässt. Wenn Sie die Standardeinstellung für einen beliebigen Benutzer ändern, gilt dies für alle neuen Besprechungen, die von diesem Benutzer organisiert werden, sowie für alle vorherigen Besprechungen, in denen der Benutzer die Besprechungsoptionen nicht geändert hat.

### <a name="enable-live-captions"></a>Aktivieren von Live Beschriftungen

Hierbei handelt es sich um eine benutzerspezifische Richtlinie, die während einer Besprechung gilt. Mit dieser Einstellung wird gesteuert, ob die Option " **Live Beschriftungen aktivieren** " für den Benutzer verfügbar ist, um in Besprechungen, an denen der Benutzer teilnimmt, Live Beschriftungen zu aktivieren und zu deaktivieren.  

![Screenshot mit der Option "Live-Beschriftungen aktivieren"](media/meeting-policies-live-captions.png)

|Einstellungswert |Verhalten  |
|---------|---------|
|**Deaktiviert, aber der Benutzer kann außer Kraft gesetzt werden**     | Live Beschriftungen werden für den Benutzer während einer Besprechung nicht automatisch aktiviert. Der Benutzer sieht im Überlaufmenü (**.**..) die Option **Live Beschriftungen aktivieren** , um Sie zu aktivieren. Dies ist die Standardeinstellung. |
|**Deaktiviert**     | Live Beschriftungen sind für den Benutzer während einer Besprechung deaktiviert. Der Benutzer kann nicht aktiviert werden.          |

<a name="bkcontentsharing"> </a>

### <a name="allow-chat-in-meetings"></a>Chat in Besprechungen zulassen

Hierbei handelt es sich um eine Einstellung für jeden Teilnehmer. Mit dieser Einstellung wird gesteuert, ob der Besprechungs Chat in der Besprechung des Benutzers zulässig ist.

<a name="bkparticipantsandguests"> </a>

## <a name="meeting-policy-settings---designated-presenter-role-mode"></a>Einstellungen für Besprechungsrichtlinien – Designated Role Mode für Referenten

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Mit dieser Einstellung können Sie den Standardwert der " **Wer kann präsentieren?** " in den **Besprechungsoptionen** des Teams-Clients ändern. Diese Richtlinieneinstellung wirkt sich auf alle Besprechungen aus, einschließlich Besprechungen jetzt abhalten.

**Wer kann präsentieren?** mit dieser Einstellung können Besprechungsorganisatoren auswählen, wer in einer Besprechung Referenten sein kann. Weitere Informationen finden Sie unter [Ändern der Teilnehmereinstellungen für eine Teambesprechung](https://support.microsoft.com/article/change-participant-settings-for-a-teams-meeting-53261366-dbd5-45f9-aae9-a70e6354f88e) und [Rollen in einer Teambesprechung](https://support.microsoft.com/article/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

Derzeit können Sie PowerShell nur zum Konfigurieren dieser Richtlinieneinstellung verwenden. Sie können eine vorhandene Team-Besprechungsrichtlinie mithilfe des Cmdlets " [festlegen-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy) " bearbeiten. Sie können auch eine neue Team-Besprechungsrichtlinie erstellen, indem Sie das Cmdlet [New-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/new-csteamsmeetingpolicy) verwenden und es Benutzern zuweisen.

Legen Sie den **DesignatedPresenterRoleMode** -Parameter auf eine der folgenden Optionen fest, um den Standardwert für " **Wer kann präsentieren?** " anzugeben:

- **EveryoneUserOverride**: alle Besprechungsteilnehmer können Referenten sein. Dies ist der Standardwert. Dieser Parameter entspricht der Einstellung **jeder** in Teams.
- **EveryoneInCompanyUserOverride**: authentifizierte Benutzer in der Organisation, einschließlich Gastbenutzer, können Referenten sein. Dieser Parameter entspricht den Einstellungen für **Personen in meiner Organisation** in Teams.
- **OrganizerOnlyUserOverride**: nur der Besprechungsorganisator kann ein Referent sein, und alle Besprechungsteilnehmer sind als Teilnehmer gekennzeichnet. Dieser Parameter entspricht der Einstellung **nur ich** in Teams.

Beachten Sie, dass nach dem Festlegen des Standardwerts die Besprechungsorganisatoren diese Einstellung in Teams weiterhin ändern können, und wählen Sie aus, wer in den von Ihnen geplanten Besprechungen anwesend sein kann.

## <a name="meeting-policy-settings---meeting-attendance-report"></a>Besprechungsrichtlinien Einstellungen – Bericht zur Besprechungs Anwesenheit

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Mit dieser Einstellung wird gesteuert, ob Besprechungsorganisatoren den [Besprechungsanwesenheitsbericht](teams-analytics-and-reports/meeting-attendance-report.md)herunterladen können.

Derzeit können Sie PowerShell nur zum Konfigurieren dieser Richtlinieneinstellung verwenden. Sie können eine vorhandene Team-Besprechungsrichtlinie mithilfe des Cmdlets " [festlegen-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy) " bearbeiten. Sie können auch eine neue Team-Besprechungsrichtlinie erstellen, indem Sie das Cmdlet [New-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/new-csteamsmeetingpolicy) verwenden und es Benutzern zuweisen.

Um einen Besprechungsorganisator zum Herunterladen des Besprechungs Anwesenheitsberichts zu aktivieren, legen Sie den **AllowEngagementReport** -Parameter auf **Enabled (aktiviert**). Wenn diese Option aktiviert ist, wird die Option zum Herunterladen des Berichts im Bereich **Teilnehmer** angezeigt.

Um zu verhindern, dass ein Besprechungsorganisator den Bericht herunterlädt, setzen Sie den Parameter auf **disabled**. Diese Einstellung ist standardmäßig deaktiviert, und die Option zum Herunterladen des Berichts steht nicht zur Verfügung.

## <a name="meeting-policy-settings---meeting-provider-for-islands-mode"></a>Besprechungsrichtlinien Einstellungen – Besprechungs Anbieter für Inseln-Modus

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Mit dieser Einstellung wird gesteuert, welches Outlook-Besprechungs-Add-in für Benutzer verwendet wird *, die sich im Inseln-Modus befinden*. Sie können angeben, ob Benutzer das Team Besprechungs-Add-in oder sowohl die Teambesprechung als auch die Skype for Business-Besprechungs-Add-Ins verwenden können, um Besprechungen in Outlook zu planen.

Sie können diese Richtlinie nur auf Benutzer anwenden, die sich im Modus "Inseln" befinden, und den **AllowOutlookAddIn** -Parameter in den Team-Besprechungsrichtlinien auf " **true** " festlegen.

Derzeit können Sie nur PowerShell verwenden, um diese Richtlinie einzurichten. Sie können eine vorhandene Team-Besprechungsrichtlinie mithilfe des Cmdlets " [festlegen-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy) " bearbeiten. Sie können auch eine neue Team-Besprechungsrichtlinie erstellen, indem Sie das Cmdlet [New-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/new-csteamsmeetingpolicy) verwenden und es Benutzern zuweisen.

Um anzugeben, welches Besprechungs-Add-in für Benutzer verfügbar sein soll, legen Sie den **PreferredMeetingProviderForIslandsMode** -Parameter wie folgt fest:

- Setzen Sie den Parameter auf **TeamsAndSfB** , um das Add-in Teams-Besprechung und das Skype for Business-Add-in in Outlook zu aktivieren. Dies ist der Standardwert.
- Setzen Sie den Parameter auf **Teams** , um nur das Team Besprechungs-Add-in in Outlook zu aktivieren. Mit dieser Richtlinieneinstellung wird sichergestellt, dass alle zukünftigen Besprechungen über einen Link "Teams-Besprechungsteilnahme" verfügen. Es werden keine vorhandenen Skype for Business-Besprechungs Verknüpfungs Verknüpfungen zu Teams migriert. Diese Richtlinieneinstellung hat keinen Einfluss auf Anwesenheit, Chat, PSTN-Anrufe oder andere Funktionen in Skype for Business, was bedeutet, dass Benutzer Skype for Business weiterhin für diese Funktionen verwenden.

  Wenn Sie den Parameter auf **Teams** setzen und dann zurück zu **TeamsAndSfB** wechseln, sind beide Besprechungs-Add-Ins aktiviert. Beachten Sie jedoch, dass vorhandene Team-Besprechungs-Join-Links nicht zu Skype for Business migriert werden. Nur Skype for Business-Besprechungen, die nach der Änderung geplant sind, haben einen Link zu Skype for Business-Besprechungen.

## <a name="meeting-policy-settings---video-filters-mode"></a>Einstellungen für Besprechungsrichtlinien – Video Filtermodus

Hierbei handelt es sich um eine Richtlinie pro Benutzer. Diese Einstellung steuert, ob Benutzer ihren Video Hintergrund in einer Besprechung anpassen können.

Derzeit können Sie nur PowerShell verwenden, um diese Richtlinie einzurichten. Sie können eine vorhandene Team-Besprechungsrichtlinie mithilfe des Cmdlets " [festlegen-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy) " bearbeiten. Oder erstellen Sie eine neue Team-Besprechungsrichtlinie mithilfe des Cmdlets [New-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/new-csteamsmeetingpolicy) , und weisen Sie die Richtlinie Benutzern zu.

Wenn Sie angeben möchten, ob Benutzer ihren Video Hintergrund in einer Besprechung anpassen können, legen Sie den **VideoFiltersMode** -Parameter wie folgt fest:

|Festlegen des Werts in PowerShell |Verhalten  |
|---------|---------|
|**Nofilters**     |Der Benutzer kann seinen Video Hintergrund nicht anpassen.|
|**BlurOnly**     |Der Benutzer hat die Möglichkeit, seinen Video Hintergrund zu verwischen. |
|**BlurandDefaultBackgrounds**     |Der Benutzer hat die Möglichkeit, seinen Video Hintergrund zu verwischen oder aus dem Standardsatz von Bildern auszuwählen, der als Hintergrund verwendet werden soll. |
|**Allfilters**     |Verwenden Sie die Option zum verwischen des Videohintergrunds, zum auswählen aus dem Standardsatz von Bildern oder zum Hochladen benutzerdefinierter Bilder, die als Hintergrund verwendet werden sollen. |

> [!NOTE]
> Bilder, die von Benutzern hochgeladen wurden, werden nicht von Teams angezeigt. Wenn Sie die Einstellung **allfilters** verwenden, sollten Sie über interne Organisationsrichtlinien verfügen, um zu verhindern, dass Benutzer anstößige oder unangemessene Bilder hochladen, oder Bilder, die Ihre Organisation nicht für die Verwendung für Teams-Besprechungs Hintergründe verwendet.

## <a name="related-topics"></a>Verwandte Themen

- [Übersicht über PowerShell für Microsoft Teams](teams-powershell-overview.md)
- [Zuweisen von Richtlinien zu Ihren Benutzern in Microsoft Teams](assign-policies.md)
- [Entfernen der RestrictedAnonymousAccess Teams-Besprechungsrichtlinie für Benutzer](meeting-policies-restricted-anonymous-access.md)
