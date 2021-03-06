---
title: Verwenden von OneDrive for Business und SharePoint für Besprechungsaufzeichnungen
author: cichur
ms.author: v-cichur
ms.reviewer: hao.moy
manager: serdars
ms.topic: article
audience: admin
ms.service: msteams
search.appverid: MET150
description: Hier erfahren Sie, wie Sie von Stream zu OneDrive for Business und SharePoint-Besprechungs Speicher in Microsoft Teams wechseln.
localization_priority: Normal
f1.keywords:
- NOCSH
ms.collection:
- M365-collaboration
- m365initiative-meetings
appliesto:
- Microsoft Teams
ms.openlocfilehash: 46d3b53f62a3bb497f173c9efd418b7ed88444c7
ms.sourcegitcommit: 1e16c6c7112bdde03209c12468b5705ddd116a62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "49578508"
---
# <a name="use-onedrive-for-business-and-sharepoint-or-stream-for-meeting-recordings"></a>Verwenden von OneDrive for Business und SharePoint oder Stream für Besprechungsaufzeichnungen

> [!Note]
> Die Änderung von der Verwendung von Microsoft Stream zu OneDrive for Business und Microsoft SharePoint für Besprechungsaufzeichnungen ist ein Phasen orientierter Ansatz.

|<div style="width:290px">Datum&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</div> |Ereignis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|5. Oktober 2020 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| Sie können die Team-Besprechungsrichtlinie aktivieren, damit Besprechungsaufzeichnungen in OneDrive for Business und SharePoint statt in Microsoft Stream (klassisch) gespeichert werden.|
|Rollout ab 11. Januar 2021 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Alle neuen Teams-Besprechungsaufzeichnungen werden in OneDrive for Business und SharePoint gespeichert, es sei denn, Sie verzögern diese Änderung, indem Sie die Team-Besprechungsrichtlinien Ihrer Organisation ändern und diese explizit auf **Stream** festlegen. Das Anzeigen der Richtlinien Berichterstattung als Stream reicht nicht aus. Sie müssen den Richtlinienwert explizit auf **Stream** festlegen.|
|Rollout ab 1. März 2021 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|**Unternehmenskunden**<br>Es können keine neuen Besprechungsaufzeichnungen in Microsoft Stream (klassisch) gespeichert werden. alle Kunden erhalten automatisch Besprechungsaufzeichnungen, die auf OneDrive for Business und SharePoint gespeichert werden, selbst wenn Sie Ihre Teams-Besprechungsrichtlinien in **Stream** geändert haben. Wir empfehlen, dass Kunden diese Funktion vor diesem Datum ausrollen, damit Sie den Zeitpunkt der Freigabe kontrollieren können. |
|Rollout ab 7. Juli 2021 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|**Education-Kunden**<br>Es können keine neuen Besprechungsaufzeichnungen in Microsoft Stream (klassisch) gespeichert werden. alle Kunden erhalten automatisch Besprechungsaufzeichnungen, die auf OneDrive for Business und SharePoint gespeichert werden, selbst wenn Sie Ihre Teams-Besprechungsrichtlinien in **Stream** geändert haben. Wir empfehlen, dass Kunden diese Funktion vor diesem Datum ausrollen, damit Sie den Zeitpunkt der Freigabe kontrollieren können. Wir haben diesen Zeitplan aktualisiert, damit Education-Kunden in der Lage sind, in-Progress-Semester abzuschließen. |

> [!Note]
> Wir empfehlen Unternehmens-und Bildungskunden, die Änderung in Ihrer Organisation besser zu kontrollieren, wenn Sie mit der Änderung vertraut sind, anstatt darauf zu warten, dass dies geschieht.

Microsoft Teams hat eine neue Methode zum Speichern von Besprechungsaufzeichnungen. Als erste Phase des Übergangs vom klassischen Microsoft-Stream auf den [neuen Datenstrom](https://docs.microsoft.com/stream/streamnew/new-stream)speichert diese Methode Aufzeichnungen zu Microsoft OneDrive for Business und SharePoint in Microsoft 365 und bietet zahlreiche Vorteile.

Zu den Vorteilen der Verwendung von OneDrive for Business und SharePoint für das Speichern von Aufzeichnungen gehören:

- Aufbewahrungsrichtlinien für Teams-Besprechungsaufzeichnung (TMR) (S + C E5-autoaufbewahrungs Etiketten)
- Profitieren Sie von OneDrive for Business und SharePoint-Informations-Governance
- Einfaches Einrichten von Berechtigungen und Freigabe
- Freigeben von Aufzeichnungen für Gäste (externe Benutzer) mit expliziter Freigabe
- Zugriffs Fluss anfordern
- Bereitstellen von OneDrive for Business-und SharePoint-freigegebenen Links
- Höhere Kontingente
- Besprechungsaufzeichnungen sind schneller verfügbar
- Support für **lokale** Mandanten
- Multi-Geo-Unterstützung – Aufzeichnungen werden in einer für diesen benutzerspezifischen Region gespeichert.
- Unterstützung für Ihren eigenen Schlüssel (BYOK)
- Verbesserte Transkriptions Qualität und Sprecher Zuordnung

Es gibt einige Einschränkungen, die berücksichtigt werden sollten:

- Es werden nur Englisch-Untertitel und-Transkripte vorhanden sein.
- Sie können keine Transkripte oder deren Inhalt durchsuchen.
- Sie können die Transkripte nicht bearbeiten, aber Sie können die Beschriftungen aus-und einschalten.
- Sie können steuern, mit wem Sie die Aufzeichnung freigeben, aber Sie können Personen mit freigegebenen Zugriff nicht blockieren, indem Sie die Aufzeichnung herunterladen.
- Wenn die Aufzeichnung die Speicherung beendet hat, wird keine e-Mail angezeigt, aber die Aufzeichnung wird nach Abschluss des Besprechungs Chats angezeigt. Dies geschieht viel schneller als in Stream zuvor.

Schauen Sie sich die "Besprechungsaufzeichnung" an, um weitere Informationen zu erhalten.

> [!VIDEO https://www.youtube.com/embed/8iol0KfCeL8]

## <a name="set-up-the-meeting-recording-option-for-onedrive-for-business-and-sharepoint"></a>Einrichten der Option "Besprechungsaufzeichnung" für OneDrive for Business und SharePoint

Die Option "Besprechungsaufzeichnung" ist eine Einstellung auf der Richtlinienebene "Teams". Im folgenden Beispiel wird gezeigt, wie die globale Richtlinie eingerichtet wird. Stellen Sie sicher, dass Sie die Option für die Besprechungsaufzeichnung für die Richtlinien festlegen, die Sie Ihren Benutzern zugewiesen haben.

> [!Note]
> Änderungen an den Gruppen Besprechungsrichtlinien dauern eine Weile. Schauen Sie nach ein paar Stunden nach der Festlegung zurück, und melden Sie sich erneut an.

1. Installieren Sie Skype for Business Online PowerShell.
**Hinweis**: Skype for Business Online Connector ist derzeit Teil des neuesten Teams PowerShell-Moduls. Wenn Sie die neueste Version von Teams PowerShell verwenden, müssen Sie den Skype for Business Online-Connector nicht installieren. Weitere Informationen finden Sie unter [Verwalten von Skype for Business Online mit PowerShell](https://docs.microsoft.com/microsoft-365/enterprise/manage-skype-for-business-online-with-microsoft-365-powershell?view=o365-worldwide&preserve-view=true).

    a. Laden Sie [Skype for Business Online PowerShell](https://docs.microsoft.com/microsoft-365/enterprise/manage-skype-for-business-online-with-microsoft-365-powershell?view=o365-worldwide&preserve-view=true)herunter.

    b. Folgen Sie den Anweisungen, um Sie zu installieren.

    c. Starten Sie Ihren Computer neu.

2. Starten von PowerShell als Administrator

3. Importieren Sie den SkypeOnline-Connector, und registrieren Sie sich als Teamadministrator.

   ```powershell
   Import-Module SkypeOnlineConnector
   $sfbSession = New-CsOnlineSession
   Import-PSSession $sfbSession
   ```

4. Verwenden Sie " [CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy) ", um eine Team-Besprechungsrichtlinie für den Übergang vom Datenstrom Speicher zu OneDrive for Business und SharePoint einzurichten.

   ```powershell
   Set-CsTeamsMeetingPolicy -Identity Global -RecordingStorageMode "OneDriveForBusiness"
   ```

> [!Note]
> Wenn einige Ihrer Benutzer eine Richtlinie pro Organisator oder pro Benutzer zugewiesen haben, müssen Sie diese Einstellung für diese Richtlinie festlegen, wenn Sie möchten, dass Sie auch die Besprechungsaufzeichnungen in OneDrive for Business und SharePoint speichern. Weitere Informationen finden Sie unter [Verwalten von Besprechungsrichtlinien in Teams](meeting-policies-in-teams.md).

## <a name="opt-out-of-onedrive-for-business-and-sharepoint-to-continue-using-stream"></a>Deaktivieren von OneDrive for Business und SharePoint, um den Datenstrom weiterhin verwenden zu können

Auch wenn eine Richtlinie besagt, dass Sie auf **Stream** eingestellt ist, ist Sie möglicherweise nicht eingestellt. In der Regel ist die Standardeinstellung **Stream**, wenn die Richtlinie nicht festgelegt ist. Wenn Sie jedoch die Nutzung von SharePoint oder OneDrive for Business deaktivieren möchten, müssen Sie die Richtlinie auf **Stream** zurücksetzen, um sicherzustellen, dass Sie die Standardeinstellung ist.

```PowerShell
Set-CsTeamsMeetingPolicy -Identity Global -RecordingStorageMode "Stream"
```

## <a name="permissions-or-role-based-access"></a>Berechtigungen oder rollenbasierter Zugriff

> [!Note]
> Wir empfehlen, dass der Empfänger ein angemeldeter Benutzer sein muss, wenn er Besprechungsaufzeichnungen für Teams freigibt. Dies kann erreicht werden, indem Sie die Option **Personen in (Ihrer Organisation)** auswählen, wenn Sie die Datei wie in [SharePoint-Dateien oder-Ordner](https://support.microsoft.com/office/share-sharepoint-files-or-folders-1fe37332-0f9a-4719-970e-d2578da4941c?redirectSourcePath=%25252fen-US%25252farticle%25252fShare-sites-or-documents-with-people-outside-your-organization-80E49744-E30F-44DB-8D51-16661B1D4232&ui=en-US&rs=en-US&ad=US)dokumentiert freigeben. Die externe Freigabe ist nicht für die Verteilung von umfangreichen Dateien oder eine große Anzahl von Dateien vorgesehen. Um Betrugs-und Missbrauchs Szenarien vorzubeugen, können Probleme auftreten, wenn Sie eine große Datenmenge an externe Benutzer weitergeben.

|Besprechungstyp                               | Wer hat auf Record geklickt?| Wo landet die Aufzeichnung?                               |Wer hat Zugriff? R/W, r oder Freigabe                                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|1:1-Anruf mit internen Parteien             |Anrufer                 |OneDrive for Business-Konto des Anrufers                        |Der Anrufer ist Besitzer und hat vollständige Rechte. <br /><br />Der aufgerufene (im gleichen Mandanten) hat nur Lesezugriff. Kein Freigabe Zugriff. <br /><br /> Der aufgerufene (wenn in einem anderen Mandanten) hat keinen Zugriff. Der Anrufer muss ihn für den aufgerufenen freigeben.|
|1:1-Anruf mit internen Parteien             |Callee                 |OneDrive for Business-Konto des berufenen                        |Der aufgerufene ist Besitzer und hat vollständige Rechte. <br /><br />Der Anrufer (wenn in demselben Mandanten schreibgeschützter Zugriff verfügbar ist. Kein Freigabe Zugriff. <br /><br />Der Anrufer (wenn in einem anderen Mandanten) hat keinen Zugriff. Der Anrufer muss ihn an den Anrufer weitergeben.|
|1:1-Anruf mit einem externen Anruf             |Anrufer                 |OneDrive for Business-Konto des Anrufers                        |Der Anrufer ist Besitzer und hat vollständige Rechte.<br /> <br />Der aufgerufene hat keinen Zugriff. Der Anrufer muss ihn für den aufgerufenen freigeben.|
|1:1-Anruf mit einem externen Anruf             |Callee                 |OneDrive for Business-Konto des berufenen                        |Der aufgerufene ist Besitzer und hat vollständige Rechte.<br /><br />Der Anrufer hat keinen Zugriff. Der Anrufer muss ihn an den Anrufer weitergeben.|
|Gruppenanruf                                 |Ein beliebiges Mitglied des Anrufs |Mitglied, das auf das OneDrive for Business-Konto des Eintrags geklickt hat  |Das Mitglied, das auf Record geklickt hat, hat vollständige Rechte. <br /><br /> Andere Mitglieder desselben Mandanten haben Lese Rechte. <br /><br /> Andere Mitglieder eines anderen Mandanten haben keine Rechte daran.|
|Adhoc/geplante Besprechung                    |Organisator              |OneDrive for Business-Konto des Organisators                     |Organizer hat vollständige Rechte an der Aufzeichnung. <br /><br /> Alle anderen Mitglieder der Besprechung haben Lesezugriff.|
|Adhoc/geplante Besprechung                    |Anderes Besprechungs Mitglied   |Mitglied, das auf Datensatz geklickt hat                                  |Das Mitglied, das auf Record geklickt hat, hat vollständige Rechte an der Aufzeichnung. <br /><br />Organizer hat Bearbeitungsrechte und kann diese freigeben.<br /><br /> Alle anderen Mitglieder haben Lesezugriff.|
|Adhoc/geplante Besprechung mit externen Benutzern|Organisator              |OneDrive for Business-Konto des Organisators                     |Organizer hat vollständige Rechte an der Aufzeichnung.<br /> <br /> Alle anderen Mitglieder der Besprechung vom gleichen Mandanten wie der Organisator haben Lesezugriff. <br /><br /> Alle anderen externen Mitglieder haben keinen Zugriff, und der Organisator muss Sie freigeben.|
|Adhoc/geplante Besprechung mit externen Benutzern|Anderes Besprechungs Mitglied   |Mitglied, das auf Datensatz geklickt hat                                  |Das Mitglied, das auf Record geklickt hat, hat vollständige Rechte an der Aufzeichnung. Organizer hat Bearbeitungsrechte und kann diese freigeben. <br /><br /> Alle anderen Mitglieder der Besprechung vom gleichen Mandanten wie der Organisator haben Lesezugriff. <br /><br />Alle anderen externen Mitglieder haben keinen Zugriff, und der Organisator muss Sie freigeben.|
|Kanal Besprechung                            |Kanalmitglied         |SharePoint-Standort des Teams für diesen Kanal                   |Das Mitglied, das auf Record geklickt hat, hat Bearbeitungsrechte für die Aufzeichnung. <br /> <br />Die Berechtigungen jedes anderen Mitglieds basieren auf der SharePoint-Berechtigung für den Kanal.|

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Wo werden die Besprechungsaufzeichnungen gespeichert?**

- Bei nicht Kanal Besprechungen wird die Aufzeichnung in einem Ordner mit dem Namen **Aufzeichnungen** gespeichert, der sich auf der obersten Ebene des OneDrive for Business befindet, das der Person gehört, die die Besprechungsaufzeichnung gestartet hat. Beispiel:

  <i>Recorder-OneDrive for Business</i> / **Aufnahmen**

- Bei Kanal Besprechungen wird die Aufzeichnung in der Bibliothek "Teams-Website Dokumentation" in einem Ordner mit dem Namen " **Aufzeichnungen**" gespeichert. Beispiel:

  <i>Name des Teams – Kanalname</i> / **Dokumente** / **Aufnahmen**

**Wie behandle ich Aufnahmen von ehemaligen Mitarbeitern?**

Da Videos genauso wie jede andere Datei in OneDrive for Business und SharePoint sind, werden die Behandlung von Besitz und Aufbewahrung nach dem Verlassen eines Mitarbeiters dem normalen [OneDrive for Business-und SharePoint-Prozess]( https://docs.microsoft.com/onedrive/retention-and-deletion#the-onedrive-deletion-process)folgen.

**Wer hat die Berechtigung zum Anzeigen der Besprechungsaufzeichnung?**

- Für Besprechungen ohne Kanal wird für alle Besprechungsteilnehmer, mit Ausnahme externer Benutzer, automatisch ein Link persönlich freigegeben abgerufen. Externe Benutzer müssen explizit der freigegebenen Liste vom Besprechungsorganisator oder der Person hinzugefügt werden, die die Besprechungsaufzeichnung gestartet hat.

- Bei Kanal Besprechungen werden Berechtigungen von der Liste Besitzer und Mitglieder des Kanals geerbt.

**Wie kann ich Protokolle verwalten?**

Kunden, die sich für diese Vorschau entscheiden, stehen in ihren Teams-Besprechungsaufzeichnungen, die zu OneDrive for Business und SharePoint migriert werden, keine Untertitel zur Verfügung.Wir arbeiten daran, Beschriftungen, beginnend mit Untertiteln in englischer Sprache, zu Besprechungsaufzeichnungen in Q4 CY2020 hinzuzufügen.

In Teams-Besprechungsaufzeichnungen stehen Untertitel für Kunden zur Verfügung, die sich für das Zulassen von Abschriften entschieden haben, wie in [Teams Cloud-Aufzeichnungen](cloud-recording.md) beschrieben

Beschriftungen tragen dazu bei, den Betrachter aller Fähigkeiten inklusiven Inhalt zu erstellen. Als Besitzer können Sie Beschriftungen ausblenden, obwohl die Aufzeichnung weiterhin für Teams verfügbar ist, es sei denn, Sie löschen die Beschriftungen aus Teams. Informationen [zum Aktivieren oder Deaktivieren von Besprechungsaufzeichnungen](cloud-recording.md#set-up-teams-cloud-meeting-recording-for-users-in-your-organization)

Untertitel werden für Teams-Besprechungsaufzeichnungen für 60 Tage ab dem Zeitpunkt, zu dem die Besprechung aufgezeichnet wird, unterstützt.

Untertitel werden nicht vollständig unterstützt, wenn die Besprechungsaufzeichnung für Teams von Ihrem ursprünglichen Speicherort auf OneDrive for Business oder SharePoint verschoben oder kopiert wird.

**Wie wird das Speicherkontingent beeinträchtigt?**

Teams, die Dateien aufzeichnen, Leben in OneDrive for Business und SharePoint und sind in Ihrem Kontingent für diese Dienste enthalten. Siehe Kontingent für [SharePoint-Kontingent](https://docs.microsoft.com/sharepoint/sites/plan-site-maintenance-and-management#quotas) und [OneDrive for Business](https://docs.microsoft.com/onedrive/set-default-storage-space).

Sie erhalten mehr Speicherplatz mit [OneDrive for Business](https://docs.microsoft.com/office365/servicedescriptions/sharepoint-online-service-description/sharepoint-online-limits) im Vergleich zu Datenstrom und mehr ersetzbarem Speicher mit SharePoint.

**Wie kann ich eine Besprechungsaufzeichnung für Teams wiedergeben?**

Ihr Video wird auf dem Video Player von OneDrive for Business oder SharePoint wiedergegeben, je nachdem, wo Sie auf die Datei zugreifen.

**Wenn Sie beabsichtigen, das Hinzufügen zu Datenstrom zu verwerfen, bleiben die vorhandenen Videos unverändert und für wie lange?**

Stream als Plattform wird in naher Zukunft nicht mehr als veraltet markiert. Die Videos, die aktuell in Stream vorhanden sind, bleiben dort, bis wir mit der Migration beginnen. Bei der Migration werden diese Videos auch nach OneDrive for Business oder SharePoint migriert. Weitere Informationen finden Sie [hier](https://docs.microsoft.com/stream/streamnew/classic-migration) .

**Wie kann ich eine Aufbewahrungs Bezeichnung anwenden?**

Hier erfahren Sie [, wie Sie eine Aufbewahrungs Beschriftung automatisch anwenden](https://docs.microsoft.com/microsoft-365/compliance/apply-retention-labels-automatically?view=o365-worldwide#microsoft-teams-meeting-recordings).

**Wie weisen ich meinen Benutzern in Microsoft Teams Richtlinien zu und welche Richtlinien haben Vorrang?**

Sehen Sie [, welche Richtlinie Vorrang hat?](https://docs.microsoft.com/MicrosoftTeams/assign-policies#which-policy-takes-precedence).
