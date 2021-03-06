---
title: Vertraulichkeits Bezeichnungen für Microsoft Teams
author: lanachin
ms.author: v-lanac
manager: serdars
ms.reviewer: abgupta
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
ms.collection:
- M365-collaboration
appliesto:
- Microsoft Teams
f1.keywords:
- NOCSH
localization_priority: Normal
search.appverid: MET150
description: Hier erfahren Sie, wie Sie Vertraulichkeits Beschriftungen in Microsoft Teams definieren und verwenden.
ms.openlocfilehash: 21d70bf48448ccef5555078e4aba65bb10d5d6a2
ms.sourcegitcommit: d7e0406276def8bc731aa6dcbd49802441ec5138
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "48476720"
---
# <a name="sensitivity-labels-for-microsoft-teams"></a>Vertraulichkeits Bezeichnungen für Microsoft Teams

Mit [Vertraulichkeits Beschriftungen](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels) können Teams-Administratoren den Zugriff auf vertrauliche organisatorische Inhalte regulieren, die während der Zusammenarbeit in Teams erstellt wurden. Sie können Vertraulichkeits Bezeichnungen und die zugehörigen Richtlinien im [Security & Compliance Center](https://docs.microsoft.com/microsoft-365/compliance/go-to-the-securitycompliance-center)definieren. Diese Bezeichnungen und Richtlinien werden automatisch auf Teams in Ihrer Organisation angewendet.  

## <a name="whats-the-difference-between-sensitivity-labels-and-teams-classification-labels"></a>Was ist der Unterschied zwischen Vertraulichkeits Beschriftungen und Klassifikations Etiketten für Teams?

Vertraulichkeits Beschriftungen unterscheiden sich von Klassifizierungs Beschriftungen, die Sie mit PowerShell erstellen müssen. Klassifikations Beschriftungen sind Textzeichenfolgen, die einer Gruppe zugeordnet werden können, denen jedoch keine eigentlichen Richtlinien zugeordnet sind. Sie verwenden Klassifizierungs Beschriftungen als Metadaten, um Richtlinien mithilfe interner Tools und Skripts manuell durchzusetzen.

Auf der anderen Seite werden die Vertraulichkeits Beschriftungen und ihre Richtlinien durch eine Kombination aus den Gruppen Plattform, Security & Compliance Center und Teams Services automatisch durchgesetzt. Vertraulichkeits Beschriftungen bieten leistungsstarke Infrastrukturunterstützung zum Sichern vertraulicher Daten Ihrer Organisation.  

Verwenden Sie die Anweisungen in [Azure Active Directory-Klassifikations-und-Vertraulichkeits Beschriftungen für Microsoft 365-Gruppen](https://docs.microsoft.com/microsoft-365/compliance/migrate-aad-classification-sensitivity-labels), um Ihre vorhandenen Gruppen von der Verwendung von Klassifizierungs Beschriftungen zur Verwendung von Vertraulichkeits Beschriftungen zu migrieren.
## <a name="create-manage-and-publish-sensitivity-labels-for-teams"></a>Erstellen, verwalten und Veröffentlichen von Vertraulichkeits Etiketten für Teams

Informationen zum Aktivieren, erstellen und Veröffentlichen von Vertraulichkeits Bezeichnungen für Teams finden Sie unter [Azure Active Directory-Klassifikations-und-Vertraulichkeits Beschriftungen für Microsoft 365-Gruppen](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).

>[!IMPORTANT]
>Das Erstellen, aktualisieren und Löschen von Vertraulichkeits Beschriftungen erfordert eine sorgfältige Sequenzierung bei der Veröffentlichung von Etiketten für Benutzer. Jede Abweichung in der Sequenz kann zu beständigen Team Erstellungsfehlern für alle Benutzer führen. Daher ist es wichtig, die folgenden Schritte auszuführen, wenn Sie <a href="#createpublishlabels">Etiketten erstellen und veröffentlichen</a>, <a href="#modifydeletelabels">veröffentlichte Etiketten ändern und löschen</a>sowie <a href="#manageerrors">Fehler bei der Teamerstellung verwalten</a>.

**Erstellen und Veröffentlichen von Etiketten** <a name="createpublishlabels"> </a>

Wenn eine Beschriftung im Security & Compliance Center erstellt und veröffentlicht wird, kann es bis zu 10 Minuten dauern, bis die Beschriftung auf der Benutzeroberfläche für die TEAMERSTELLUNG sichtbar wird. Führen Sie die folgenden Schritte aus, um die Bezeichnung für alle Benutzer im Mandanten zu veröffentlichen:
1. Erstellen Sie die Beschriftung, und veröffentlichen Sie Sie für einige ausgewählte Benutzerkonten im Mandanten.
2. Wenn das Label veröffentlicht wird, warten Sie 10 Minuten.
3. Versuchen Sie nach 10 Minuten, ein Team mit dem Label zu erstellen, indem Sie eines der Benutzerkonten verwenden, die auf das Etikett zugreifen können.
4. Wenn das Team erfolgreich in Schritt 3 erstellt wurde, veröffentlichen Sie die Beschriftung für die verbleibenden Benutzer im Mandanten.

**Ändern und Löschen von veröffentlichten Etiketten** <a name="modifydeletelabels"> </a>

Das Löschen oder Ändern der Bezeichnung, während Sie mit Vertraulichkeitsrichtlinien verknüpft ist, kann zu Team Erstellungsfehlern im gesamten Mandanten führen. Daher müssen Sie vor dem Löschen oder Ändern einer Bezeichnung zunächst die Zuordnung der Bezeichnung von den zugehörigen Richtlinien aufheben. Führen Sie die folgenden Schritte aus.  
So löschen oder ändern Sie ein Etikett:
1. Entfernen Sie die Beschriftung aus allen Richtlinien, die die Bezeichnung verwenden. Alternativ können Sie auch die Richtlinien selbst löschen.
2. Wenn das Etikett aus den Richtlinien entfernt wird oder die Richtlinien selbst gelöscht werden, warten Sie 10 Minuten, bevor Sie fortfahren.
3. Starten Sie nach 10 Minuten die Team Erstellungs Schnittstelle, und stellen Sie sicher, dass die Beschriftung für keinen Benutzer im Mandanten mehr sichtbar ist.
4. Nun können Sie die Beschriftung problemlos löschen oder ändern.

**Verwalten von Team Erstellungsfehlern** <a name="manageerrors"> </a>

Wenn die TEAMERSTELLUNG zu einem beliebigen Zeitpunkt während der öffentlichen Vorschau fehlschlägt, haben Sie zwei Möglichkeiten:
 - Stellen Sie sicher, dass Vertraulichkeits Beschriftungen für Benutzer während der Teamerstellung nicht zwingend erforderlich sind.
 - Deaktivieren Sie die Vertraulichkeits Beschriftungen mithilfe der Skripts unter [Aktivieren dieser Vorschau](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites#enable-this-preview).

Beachten Sie, dass die EnableMIPLabels-Einstellung wie folgt auf "false" festgelegt werden muss:

```console
$setting["EnableMIPLabels"] = "False"
```

## <a name="using-sensitivity-labels-with-teams"></a>Verwenden von Vertraulichkeits Beschriftungen in Teams

Im folgenden finden Sie einige Beispielszenarien für die Verwendung von Vertraulichkeits Beschriftungen in Teams in Ihrer Organisation.

### <a name="privacy-setting-of-teams"></a>Datenschutzeinstellungen für Teams

Sie können eine Vertraulichkeits Beschriftung erstellen, die den Benutzern beim Anwenden während der Teamerstellung ermöglicht, Teams mit einer bestimmten Einstellung für Privatsphäre (öffentlich oder privat) zu erstellen.

Beispielsweise erstellen Sie im Security & Compliance Center ein Etikett mit dem Namen "vertraulich", und Sie konfigurieren Teams so, dass jedes Team, das mit diesem Label erstellt wurde, ein privates Team sein muss. Wenn ein Benutzer ein neues Team erstellt und das **vertrauliche** Etikett auswählt, ist die einzige Datenschutzoption, die dem Benutzer zur Verfügung steht, **Privat**. Andere Datenschutzoptionen wie Public und org-Wide sind für den Benutzer deaktiviert.

![Screenshot der vertraulichen Vertraulichkeits Kennzeichnung](media/sensitivity-labels-confidential-example.png)

Auch wenn der Benutzer beim Erstellen eines neuen Teams " **Allgemein** " auswählt, kann er nur öffentliche oder organisationsweite Teams erstellen.

![Screenshot der allgemeinen Vertraulichkeits Beschriftung](media/sensitivity-labels-general-example.png)

Wenn das Team erstellt wird, wird die Vertraulichkeits Bezeichnung in der oberen rechten Ecke der Kanäle im Team angezeigt.

![Screenshot der Vertraulichkeits Beschriftung im Team Kanal](media/sensitivity-labels-channel.png)

Ein Teambesitzer kann die Vertraulichkeits Beschriftung und die Datenschutzeinstellung des Teams jederzeit ändern, indem er zum Team wechselt und dann auf **Team bearbeiten**klickt.

![Screenshot der Vertraulichkeits Beschriftung im Team Kanal](media/sensitivity-labels-edit-team.png)

### <a name="guest-access-to-teams"></a>Gastzugriff auf Teams

Sie können angeben, ob ein Team, das mit einer bestimmten Bezeichnung erstellt wurde, Gastzugriff ermöglicht. Teams, die mit einer Beschriftung erstellt wurden, die keinen Gastzugriff zulässt, stehen nur Benutzern in Ihrer Organisation zur Verfügung. Personen außerhalb Ihrer Organisation können dem Team nicht hinzugefügt werden.

### <a name="sensitivity-labels-in-the-microsoft-teams-admin-center"></a>Vertraulichkeits Bezeichnungen im Microsoft Teams Admin Center

Sie können Vertraulichkeits Beschriftungen einrichten, wenn Sie im Microsoft Teams Admin Center ein Team erstellen oder bearbeiten. Vertraulichkeits Beschriftungen sind auch in den teameigenschaften und in der Spalte **Klassifizierung** auf der Seite Teams Verwalten des Microsoft Teams admin Centers sichtbar.

## <a name="known-issues"></a>Bekannte Probleme

**Unterstützung für Vertraulichkeits Beschriftungen in Teams-Diagramm-APIs, PowerShell-Cmdlets und-Vorlagen**

Derzeit können Benutzer keine Vertraulichkeits Bezeichnungen für Teams anwenden, die direkt über Diagramm-APIs, PowerShell-Cmdlets und Vorlagen erstellt wurden.

**Unterstützung für Vertraulichkeits Beschriftungen in Teams edu-SKUs**

Vertraulichkeits Beschriftungen werden derzeit für Kunden, die Team Education-SKUs verwenden, nicht unterstützt.

**Bearbeiten von Vertraulichkeits Beschriftungen direkt in einer SharePoint-Websitesammlung für private Kanäle**

Private Kanäle, die in einem Team erstellt werden, erben die Vertraulichkeits Bezeichnung, die in einem Team angewendet wurde. Darüber hinaus wird dieselbe Bezeichnung automatisch für die SharePoint-Websitesammlung für den privaten Kanal übernommen.

Wenn ein Benutzer die Vertraulichkeits Beschriftung auf einer SharePoint-Websitesammlung für einen privaten Kanal direkt aktualisiert, wird diese Bezeichnung nicht im Team-Client aktualisiert. In diesem Szenario wird den Benutzern weiterhin die auf ein Team angewendete Vertraulichkeits Bezeichnung in der Kopfzeile privater Kanal angezeigt.

**Ausbreitungs Zeiten für Änderungen, die auf Vertraulichkeits Beschriftungen außerhalb der Teams-App angewendet werden**

Änderungen an Vertraulichkeits Beschriftungen außerhalb der Teams-App können bis zu 24 Stunden dauern, bis Sie in der Teams-App wiedergegeben werden. Dies gilt für alle Änderungen, die vorgenommen wurden, um Bezeichnungen für einen Mandanten zu aktivieren oder zu deaktivieren, Änderungen an Etikettennamen, Einstellungen und Richtlinien.

Darüber hinaus kann es bis zu 24 Stunden dauern, bis Änderungen an einer Bezeichnung, die direkt an eine Gruppe oder SharePoint-Websitesammlung, die das Team zurückgibt, an die Teams-App weitergegeben werden.
