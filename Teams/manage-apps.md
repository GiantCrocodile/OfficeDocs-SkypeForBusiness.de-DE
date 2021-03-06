---
title: Verwalten Ihrer Apps im Microsoft Teams Admin Center
author: LanaChin
ms.author: v-lanac
manager: serdars
ms.topic: article
ms.service: msteams
audience: admin
ms.collection:
- Teams_ITAdmin_Help
- M365-collaboration
ms.reviewer: vaibhava
search.appverid: MET150
f1keywords:
- ms.teamsadmincenter.manageapps.overview
description: Erfahren Sie, wie Sie Ihre Teams-apps auf der Seite "Apps verwalten" im Microsoft Teams Admin Center verwalten.
appliesto:
- Microsoft Teams
localization_priority: Normal
ms.openlocfilehash: 226bd98c741a84a2d7f26c1808a4c8d7e9a6bb53
ms.sourcegitcommit: 8a345ca9a8ddc6a84f9e270ab55f1b28f6ba49c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "48486780"
---
<a name="manage-your-apps-in-the-microsoft-teams-admin-center"></a>Verwalten Ihrer Apps im Microsoft Teams Admin Center
======================================================

Als Administrator können Sie auf der Seite "Apps verwalten" im Microsoft Teams Admin Center alle Teams-Apps für Ihre Organisation anzeigen und verwalten. Hier können Sie den Status und die Eigenschaften von apps auf Organisationsebene anzeigen, neue benutzerdefinierte apps im App Store Ihrer Organisation genehmigen oder hochladen, Apps auf org-Ebene blockieren oder zulassen, apps zu Teams hinzufügen, Dienste für Drittanbieter-apps kaufen, die von apps angeforderten Berechtigungen anzeigen, die Zustimmung des Administrators zu apps erteilen und die organisationsweiten App-Einstellungen verwalten.

Auf der Seite "Apps verwalten" erhalten Sie einen Überblick über alle verfügbaren apps, sodass Sie über die erforderlichen Informationen verfügen, um zu entscheiden, welche apps in Ihrer Organisation zugelassen oder blockiert werden sollen. Sie können dann [App-Berechtigungsrichtlinien](teams-app-permission-policies.md), [App-Setup Richtlinien](teams-app-setup-policies.md)und [benutzerdefinierte App-Richtlinien und-Einstellungen](teams-custom-app-policies-and-settings.md) verwenden, um die APP-Umgebung für bestimmte Benutzer in Ihrer Organisation zu konfigurieren.

Navigieren Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu **Teams apps**  >  **Verwalten von apps**. Sie müssen ein globaler Administrator oder Team Dienstadministrator sein, um auf die Seite zugreifen zu können.

> [!NOTE]
> Die Seite "Apps verwalten" steht in den Microsoft 365-Bereitstellungen von Teams für die Government Community Cloud (gcc) noch nicht zur Verfügung.

## <a name="view-apps"></a>Anzeigen von apps

Sie können jede APP mit den folgenden Informationen zu jeder App anzeigen.

![Screenshot der Seite "verwaltete Apps"](media/manage-apps.png)

- **Name**: der Name der app. Klicken Sie auf den Namen der APP, um zur Seite App-Details zu wechseln, um weitere Informationen zur APP anzuzeigen. Dies umfasst eine Beschreibung der APP, ob Sie zulässig oder gesperrt ist, Version, Datenschutzrichtlinien, Nutzungsbedingungen, Kategorien, die für die APP gelten, den Zertifizierungsstatus, die unterstützten Funktionen und die APP-ID. Nachfolgend ein Beispiel:

  ![Screenshot der Seite "Apps-Details" für eine APP](media/manage-apps-app-details.png)
  
- **Zertifizierung**: Wenn die APP die Zertifizierung durchlaufen hat, wird entweder **Microsoft 365 Certified** oder **Publisher-Bestätigung**angezeigt. Klicken Sie auf den Link, um die Zertifizierungsdetails für die APP anzuzeigen. Wenn "" angezeigt **--** wird, verfügen wir nicht über Zertifizierungsinformationen für die app. Wenn Sie mehr über zertifizierte apps in Microsoft Teams erfahren möchten, lesen Sie [Microsoft 365-App-Zertifizierungsprogramm](https://docs.microsoft.com/teams-app-certification/all-apps).  
- **Publisher**: Name des Herausgebers.
- **Veröffentlichungsstatus**: Veröffentlichungsstatus für benutzerdefinierte apps.
- **Status**: Status der APP auf der Organisationsebene, wobei es sich um eine der folgenden Optionen handeln kann:

    - **Zulässig**: die APP steht allen Benutzern in Ihrer Organisation zur Verfügung.
    
    - **Blockiert**: die APP ist blockiert und steht nicht für Benutzer in Ihrer Organisation zur Verfügung.
    
    - **Organisationsweit blockiert**: die APP wird in den organisationsweiten App-Einstellungen blockiert.
    
      Es ist wichtig zu wissen, dass diese Spalte den zulässigen und blockierten Status von apps darstellt, die sich zuvor im Bereich " **organisationsweite Einstellungen** " befanden. Sie können jetzt apps auf der Seite " **apps verwalten** " auf der Organisationsebene anzeigen, blockieren und zulassen. 
- **Lizenzen**: gibt an, ob eine APP ein SaaS-Abonnement (Software as a Service) für den Kauf anbietet. Diese Spalte gilt nur für apps von Drittanbietern. Für jede Drittanbieter-App gibt es einen der folgenden Werte:
    - **Jetzt kaufen**: die APP bietet ein SaaS-Abonnement und steht zum Kauf zur Verfügung.  
    - **Erworben**: die APP bietet ein SaaS-Abonnement und Sie haben Lizenzen dafür erworben.
    - **--**: Die APP bietet kein Saas-Abonnement.
- **Benutzerdefinierte App**: gibt an, ob es sich um eine benutzerdefinierte App handelt.
- **Berechtigungen**: gibt an, ob eine Drittanbieter-oder benutzerdefinierte APP, die in Azure Active Directory (Azure AD) registriert ist, über Berechtigungen verfügt, die Zustimmung benötigen. Es wird einer der folgenden Werte angezeigt:
    - **Details anzeigen**: die APP verfügt über Berechtigungen, die Zustimmung erfordern, bevor die APP auf Daten zugreifen kann. 
    - **--**: Die APP verfügt nicht über Berechtigungen, deren Zustimmung erforderlich ist.
- **Kategorien**: Kategorien, die für die APP gelten.
- **Version**: App-Version.

Wenn Sie die gewünschten Informationen in der Tabelle anzeigen möchten, klicken Sie in der oberen rechten Ecke auf **Spalte bearbeiten** , um der Tabelle Spalten hinzuzufügen oder daraus zu entfernen.

## <a name="publish-a-custom-app-to-your-organizations-app-store"></a>Veröffentlichen einer benutzerdefinierten App im App Store Ihrer Organisation

Verwenden Sie die Seite "Apps verwalten", um apps zu veröffentlichen, die speziell für Ihre Organisation entwickelt wurden. Nachdem Sie eine benutzerdefinierte App veröffentlicht haben, steht Sie Benutzern im App Store Ihrer Organisation zur Verfügung. Es gibt zwei Möglichkeiten, eine benutzerdefinierte App im App Store Ihrer Organisation zu veröffentlichen. Die Art der Verwendung hängt davon ab, wie Sie die App abrufen.

- [Genehmigen einer benutzerdefinierten App](#approve-a-custom-app): Verwenden Sie diese Methode, wenn der Entwickler die App mithilfe der APP-Übermittlungs-API für Teams direkt an die Seite "Apps verwalten" sendet. Sie können die APP dann direkt über die Seite mit den App-Details überprüfen und veröffentlichen (oder ablehnen).
- [Hochladen eines App-Pakets](#upload-an-app-package): Verwenden Sie diese Methode, wenn der Entwickler Ihnen das App-Paket im ZIP-Format sendet. Sie veröffentlichen die APP, indem Sie das App-Paket hochladen.

###  <a name="approve-a-custom-app"></a>Genehmigen einer benutzerdefinierten App

Das Widget **ausstehende Genehmigungen** auf der Seite "Apps verwalten" benachrichtigt Sie, wenn ein Entwickler eine App mithilfe der APP-Übermittlungs-API für Teams übermittelt. Eine neu übermittelte APP wird mit einem **Veröffentlichungsstatus** von " **gesendet** " und dem **Status** " **blockiert**" aufgelistet. Wechseln Sie zur Seite App-Details, um weitere Informationen zur APP anzuzeigen, und legen Sie dann **Veröffentlichungsstatus** auf **veröffentlichen**fest.

Sie werden auch benachrichtigt, wenn ein Entwickler ein Update an eine benutzerdefinierte App sendet. Sie können das Update dann auf der Seite App-Details überprüfen und veröffentlichen (oder ablehnen). Alle Richtlinien für App-Berechtigungen und Richtlinien für die APP-Einrichtung bleiben für die aktualisierte APP erzwungen.

Weitere Informationen finden Sie unter [Veröffentlichen einer benutzerdefinierten APP, die über die Team-App-Übermittlungs-API übermittelt](submit-approve-custom-apps.md)wurde.

### <a name="upload-an-app-package"></a>Hochladen eines App-Pakets

Der Entwickler erstellt ein Teams-App-Paket mithilfe von [Teams App Studio](https://docs.microsoft.com/microsoftteams/platform/get-started/get-started-app-studio)und sendet es Ihnen dann im ZIP-Format. Wenn Sie über das App-Paket verfügen, können Sie es in den App Store Ihrer Organisation hochladen.

Wenn Sie eine neue benutzerdefinierte App hochladen möchten, wählen Sie **hochladen** aus, um das App-Paket hochzuladen. Nachdem die APP hochgeladen wurde, wird Sie nicht hervorgehoben, sodass Sie die Liste der apps auf der Seite "Apps verwalten" durchsuchen müssen, um Sie zu finden.

Wenn Sie eine APP nach dem Hochladen aktualisieren möchten, klicken Sie in der Liste der apps auf der Seite apps verwalten auf den Namen der APP, und klicken Sie dann auf **Aktualisieren**. Dadurch werden die vorhandene APP und alle App-Berechtigungsrichtlinien ersetzt, und die Richtlinien für die APP-Einrichtung bleiben für die aktualisierte APP erzwungen.

Weitere Informationen finden Sie unter [Veröffentlichen einer benutzerdefinierten app durch Hochladen eines App-Pakets](upload-custom-apps.md).

## <a name="allow-and-block-apps"></a>Zulassen und Blockieren von apps

Auf der Seite "Apps verwalten" können Sie einzelne apps auf Organisationsebene zulassen oder blockieren. Sie zeigt alle verfügbaren apps und den aktuellen App-Status auf Organisationsebene an. (Das Blockieren und zulassen von apps auf der Organisationsebene wurde vom Bereich " **organisationsweite App-Einstellungen** " hierhin verschoben.)

Wenn Sie eine App zulassen oder blockieren möchten, wählen Sie Sie aus, und klicken Sie dann auf **zulassen** oder **blockieren**. Wenn Sie eine APP blockieren, werden alle Interaktionen mit dieser APP deaktiviert, und die APP wird nicht in Teams für alle Benutzer in Ihrer Organisation angezeigt.

Wenn Sie eine APP auf der Seite "Apps verwalten" blockieren oder zulassen, wird diese APP für alle Benutzer in Ihrer Organisation blockiert oder zugelassen.  Wenn Sie eine app in einer Berechtigungsrichtlinie für Teams-App blockieren oder zulassen, ist Sie für Benutzer, denen diese Richtlinie zugewiesen ist, blockiert oder zulässig. Damit ein Benutzer eine App installieren und mit ihnen interagieren kann, müssen Sie die APP auf der Organisationsebene auf der Seite "Apps verwalten" und in der APP-Berechtigungsrichtlinie zulassen, die dem Benutzer zugewiesen ist.

 > [!NOTE]
 > Wenn Sie eine APP deinstallieren möchten, klicken Sie mit der rechten Maustaste auf die APP, und klicken Sie dann auf **deinstallieren** oder verwenden Sie das Menü **Weitere apps** auf der linken Seite.

## <a name="add-an-app-to-a-team"></a>Hinzufügen einer APP zu einem Team

Sie verwenden die Schaltfläche **zum Team hinzufügen** , um eine app in einem Team zu installieren. Beachten Sie, dass dies nur für apps gilt, die in einem Teambereich installiert werden können. Die Schaltfläche **zum Team hinzufügen** steht für apps, die nur im persönlichen Bereich installiert werden können, nicht zur Verfügung.

![Screenshot der Schaltfläche ' zum Team hinzufügen '](media/manage-apps-add-app-team.png)

1. Suchen Sie nach der gewünschten APP, und wählen Sie dann die APP aus, indem Sie links neben dem APP-Namen klicken.
2. Wählen Sie **zum Team hinzufügen**aus.
3. Suchen Sie im Bereich **zum Team hinzufügen** nach dem Team, dem Sie die APP hinzufügen möchten, wählen Sie das Team aus, und wählen Sie dann über **nehmen**aus.

## <a name="purchase-services-for-third-party-apps"></a>Dienste für apps von Drittanbietern kaufen

Sie können direkt über die Seite "Apps verwalten" nach Lizenzen für Dienste suchen, die von Drittanbieter-Apps für Benutzer in Ihrer Organisation angeboten werden. Die Spalte " **Lizenzen** " in der Tabelle gibt an, ob eine APP ein bezahltes Saas-Abonnement bietet. Klicken Sie auf **Jetzt kaufen** , um Pläne und Preisinformationen anzuzeigen und Lizenzen für Ihre Benutzer zu erwerben. Weitere Informationen finden Sie unter [erwerben von Diensten für Teams von Drittanbieter-apps im Microsoft Teams Admin Center](purchase-third-party-apps.md).

## <a name="grant-admin-consent-to-apps"></a>Erteilen der Zustimmung des Administrators zu apps

Sie können apps, die Berechtigungen für alle Benutzer in Ihrer Organisation anfordern, überprüfen und deren Zustimmung erteilen. Sie tun dies, damit Benutzer die von der APP angeforderten Berechtigungen nicht überprüfen und akzeptieren müssen, wenn Sie die app starten. Die Spalte " **Berechtigungen** " gibt an, ob eine APP Berechtigungen hat, für die eine Genehmigung erforderlich ist. Für jede APP, die in Azure AD registriert ist, wird ein Link " **Details anzeigen** " angezeigt, der Berechtigungen enthält, für die eine Genehmigung erforderlich ist. Weitere Informationen finden Sie unter [Anzeigen von App-Berechtigungen und erteilen der Zustimmung des Administrators im Microsoft Teams Admin Center](app-permissions-admin-center.md).

## <a name="view-resource-specific-consent-permissions"></a>Anzeigen von ressourcenspezifischen Genehmigungsberechtigungen

Berechtigungen für ressourcenspezifische Zustimmung (RSC) lassen die Teambesitzer die Zustimmung für eine APP erteilen, um auf die Daten eines Teams zuzugreifen und diese zu ändern. RSC-Berechtigungen sind granulare, Teams-spezifische Berechtigungen, die definieren, was eine app in einem bestimmten Team tun kann. Sie können die RSC-Berechtigungen auf der Registerkarte **Berechtigungen** auf der Seite App-Details für eine App anzeigen. Weitere Informationen finden Sie unter [Anzeigen von App-Berechtigungen und erteilen der Zustimmung des Administrators im Microsoft Teams Admin Center](app-permissions-admin-center.md).

## <a name="manage-org-wide-app-settings"></a>Verwalten von organisationsweiten App-Einstellungen

Verwenden Sie organisationsweite App-Einstellungen, um zu steuern, ob Benutzer apps von Drittanbietern installieren können und ob Benutzer benutzerdefinierte apps in Ihrer Organisation hochladen oder mit ihnen interagieren können. Organisationsweite App-Einstellungen Regeln das Verhalten für alle Benutzer und überschreiben alle anderen APP-Berechtigungsrichtlinien, die Benutzern zugewiesen sind. Sie können Sie verwenden, um schädliche oder problematische apps zu steuern.

> [!NOTE]
> Informationen zum Verwenden von organisationsweiten App-Einstellungen in Microsoft 365-Bereitstellungen von Teams in der Regierung von gcc finden Sie unter [Verwalten von App-Berechtigungsrichtlinien in Teams](teams-app-permission-policies.md).

1. Wählen Sie auf der Seite apps verwalten die Option **organisationsweite App-Einstellungen**aus. Anschließend können Sie die gewünschten Einstellungen im Panel konfigurieren.

    ![Screenshot der organisationsweiten App-Einstellungen](media/manage-apps-org-wide-app-settings.png)
    
2. Deaktivieren oder aktivieren Sie unter **apps von Drittanbietern**diese Einstellungen, um den Zugriff auf Drittanbieter-apps zu steuern:

    - **Drittanbieter-apps zulassen**: Hiermit wird gesteuert, ob Benutzer apps von Drittanbietern verwenden können. Wenn Sie diese Einstellung deaktivieren, sind Ihre Benutzer nicht in der Lage, Apps von Drittanbietern zu installieren oder zu verwenden, und der APP-Status dieser Apps wird in der Tabelle als **blockiert org-weit** angezeigt.

        > [!NOTE]
        > Wenn **Drittanbieter-apps zulassen** deaktiviert ist, werden [ausgehende webhooks](https://docs.microsoft.com/microsoftteams/platform/webhooks-and-connectors/what-are-webhooks-and-connectors) deaktiviert, was bedeutet, dass Benutzer Sie nicht erstellen können. Wenn diese Einstellung aktiviert ist, werden ausgehende webhooks für alle Benutzer aktiviert, und Sie können Sie auf Benutzerebene steuern, indem Sie die ausgehende webhook-App über [App-Berechtigungsrichtlinien](teams-app-permission-policies.md)zulassen oder blockieren. <br><br>Beachten Sie Folgendes: Wenn Sie über vorhandene [App-Berechtigungsrichtlinien](teams-app-permission-policies.md) für **Microsoft-apps** verfügen, die die Einstellung **bestimmte apps zulassen und alle anderen blockieren** verwenden, und Sie ausgehende webhooks für Benutzer aktivieren möchten, fügen Sie die ausgehende webhook-App zur Liste hinzu.
    - **Alle neuen Drittanbieter-apps zulassen, die standardmäßig im Store veröffentlicht**werden: Hiermit wird gesteuert, ob neue Drittanbieter-apps, die im App Store für Teams veröffentlicht werden, automatisch in Teams verfügbar sind. Diese Option kann nur festgesetzt werden, wenn Sie Drittanbieter-apps zulassen.

3. Deaktivieren oder aktivieren Sie unter **benutzerdefinierte apps**die Option **Interaktion mit benutzerdefinierten apps zulassen**. Mit dieser Einstellung wird gesteuert, ob Benutzer mit benutzerdefinierten apps interagieren können. Weitere Informationen finden Sie unter [Verwalten von benutzerdefinierten App-Richtlinien und-Einstellungen in Teams](teams-custom-app-policies-and-settings.md).
4. Klicken Sie auf **Speichern** , damit die App-Einstellungen für die gesamte Organisation wirksam werden.

## <a name="related-topics"></a>Verwandte Themen

- [Administratoreinstellungen für Apps in Microsoft Teams](admin-settings.md)