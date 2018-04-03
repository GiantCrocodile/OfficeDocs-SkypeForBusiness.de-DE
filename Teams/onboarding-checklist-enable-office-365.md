---
title: Onboarding Prüfliste für die Aktivierung von Office 365-Dienst für Microsoft-Teams
author: rmw2890
ms.author: MyAdvisor
manager: lehewe
ms.date: 03/16/2018
ms.topic: article
ms.service: msteams
ms.reviewer: rowille
description: Führen Sie die Core sowie die Aufgabe Aufgaben und Aktivitäten in der Prüfliste beim Konfigurieren von Office 365 für Teams.
MS.collection: Strat_MT_TeamsAdmin
appliesto:
- Microsoft Teams
ms.openlocfilehash: f3b5163d6bf89c6c78e44560d857620f28ee1ac9
ms.sourcegitcommit: d70e5a5e7d05a2226c1d011895fb12187d73fad0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2018
---
# <a name="enable-office-365"></a>Aktivieren von Office 365
 
| Nein | Aktivität oder Aufgabe| Beschreibung| Abgeschlossen? | Weitere Informationen|
|----|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | Erstellen eines Office 365-Mandanten| Vor Ihrer Organisation die Vorteile der Teams nutzen kann, müssen Sie ein Office 365-Mandanten einrichten. Finden Sie unter bei Office 365 Mandanten, finden Sie unter der Anleitung in der Spalte **Zusatzinformationen** fehlender. | | [Einrichten von Office 365 Business](https://support.office.com/article/Set-up-Office-365-for-business-6a3a29a0-e616-4713-99d1-15eda62d04fa) <br/><br/>[Wenn Sie weitere Hilfe benötigen, steht das Microsoft FastTrack für Office 365-Team unterstützen](https://fasttrack.microsoft.com/office) |
| 2  | Office 365-Lizenzen erwerben | Basierend auf das Ergebnis der Arbeit an, die Sie während der Phase der Teams Visionierung haben, arbeiten Sie mit Ihrer Gruppe Beschaffung, um sicherzustellen, dass Ihre Organisation verfügt über die erforderliche Lizenz SKUs erworben oder Add-On-Dienste, und sie können jetzt den Mandanten zugewiesen werden. | | [Office 365-Lizenzierung für Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/office-365-licensing) <br/><br/>[Kaufen Sie Lizenzen für Ihre Office 365 for Business-Abonnements](https://support.office.com/article/Buy-licenses-for-your-Office-365-for-business-subscription-36081d8d-b3fa-4948-8c34-e217bba825e1) |
| 3  | Zuweisen von Office 365-Lizenzen zu dem Mandanten | In der Regel erhalten Sie oder Ihr Lizenzierung Administrator eine Verknüpfung von Microsoft Lizenzierung durch, um Ihre Lizenzen Ihres Office 365-Mandanten hinzufügen. <br/><br/>Je nach welcher Kanal, die Sie zum Kauf von Lizenzen verwendet, müssen Sie möglicherweise eine der in der Spalte **Zusatzinformationen** aufgeführten Führungslinien besuchen. | | [Hinzufügen von Lizenzen zu einem Abonnement mit einem Product Key beglichen](https://support.office.com/article/Add-licenses-to-a-subscription-paid-for-using-a-product-key-4fb4bd7e-3920-4ce0-98fb-0c06e3fedf53) <br/><br/>[Hinzufügen von Lizenzen zu einem Abonnement über das Volume Licensing Service Center erworben haben](https://support.office.com/article/Add-licenses-to-a-subscription-purchased-through-the-Volume-Licensing-Service-Center-82ba88fa-ebdf-4d44-a7b3-cea82b25d71a) |
| 4  | OPTIONAL: Aktivieren Sie Communications haben | Communications haben ist eine optionale Funktion, die Sie für Rufnummern in Ihrer Organisation Konferenz Bridge gebührenfreie Zugriff bereitstellen oder um Konferenzorganisator anwählen internationale Besprechungsteilnehmern gewähren verwenden. <br/><br/>Zusätzlich zu den standard Audiokonferenzen pro-Benutzer-Lizenz können Organisationen Volume und Lizenzierung ein Bezahlung pro Minute Angebot Audio Konferenzfunktionen aktivieren auswählen. <br/><br/>Entscheiden, ob Communications haben für Ihre Organisation erforderlich ist und – wenn er ist – durch Hinzufügen der Communications haben Add-on-Lizenzvertrags zu Ihrem Mandanten zu aktivieren. | | [Was ist Guthaben für Kommunikationen?](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-and-microsoft-teams-add-on-licensing/what-are-communications-credits) <br/><br/>[Einrichten von Guthaben für Kommunikationen für Ihre Organisation](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-and-microsoft-teams-add-on-licensing/set-up-communications-credits-for-your-organization) <br/><br/>[Audiokonferenz mit Minutenabrechnung](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-and-microsoft-teams-add-on-licensing/audio-conferencing-pay-per-minute) |
| 5  | Bestätigen Sie, dass Lizenzen für den Office 365-Mandanten verfügbar sind | Besuchen Sie Office 365 Admin-Portal, und stellen Sie sicher, dass die Lizenz-SKUs und Menge, die Sie in Ihrem Office 365-Mandanten erwarten, angezeigt. <br/><br/>Verwenden Sie den Verweis in **zusätzliche Informationen** , um diese schrittweise durchlaufen werden. | | [Welche Office 365 for Business-Abonnements sind?](https://support.office.com/article/What-Office-365-for-business-subscription-do-I-have-092252f8-08df-4cdb-a8d2-b8653caa29a1) |
| 6  | Konfigurieren der Umgebung für Identitäten. | Benutzer können direkt (in dem online Bereitstellungsmodell) in Office 365 erstellt oder mit Ihrem Office 365-Mandanten aus lokalen Active Directory synchronisiert werden. <br/><br/>Bestimmen Sie, ob cloudidentitäten, synchronisierten Identitäten oder Identitätsverbund verwendet werden soll. Bestimmen der richtigen Identitätstyp liegt außerhalb des Gültigkeitsbereichs dieser Prüfliste; Allerdings finden Sie Links zu Informationen über diese Optionen in der Spalte **Zusatzinformationen** . <br/><br/>**Hinweis:** Wenn Sie nutzen synchronisiert oder Identitätsverbund, sicher, dass die lokalen-Benutzerprinzipalnamen (UPNs) entsprechen der Office 365 UPNs, und alle erforderlichen Attribute werden für die Synchronisierung mit Azure Active Directory verbinden konfiguriert. Die Attribute aufgeführt, die für Teams erforderlich sind, verwenden Sie bei der Attributliste für Skype für Business Online. | | [Grundlegendes zu Office 365-Identität und Azure Active Directory](https://support.office.com/article/Understanding-Office-365-identity-and-Azure-Active-Directory-06a189e7-5ec6-4af2-94bf-a22ea225a7a9) <br/><br/>[Vorbereiten der Bereitstellung von Benutzern durch verzeichnissynchronisierung zu Office 365](https://support.office.com/article/Prepare-to-provision-users-through-directory-synchronization-to-Office-365-01920974-9e6f-4331-a370-13aea4e82b3e) <br/><br/>[Azure Active Directory verbinden Sync: Attribute mit Azure Active Directory synchronisiert.](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-attributes-synchronized) |
| 7  | Mandantenadministratoren bestätigen | Arbeiten Sie mit Ihren Sicherheitsteams bei der einer Office 365-Verwaltungsmodell entwickeln. <br/><br/>Achten Sie darauf zu identifizieren und dokumentieren alle Mandanten und Service-Administratoren. | | [Informationen zu Office 365-Administratorrollen](https://support.office.com/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d) |
| 8  | Implementieren von Administratorrollen für Ihre Mandanten | Überprüfen Sie, ob Ihr Verwaltungsmodell den Bedürfnissen Ihrer Organisation entspricht, und weisen Sie Office 365-Administratorrollen an Ihre Administratoren. | | [Zuweisen von Administratorrollen in Office 365 für Unternehmen](https://support.office.com/article/Assign-admin-roles-in-Office-365-for-business-eac4d046-1afd-4f1a-85fc-8219c79e1504) |
| 9  | Melden Sie sich bei der Hochladevorgang aufrufen Quality Dashboard (CQD) Ihre Informationen zum Erstellen von an. | Jeder Bereitstellung von Teams, sollte die CQD um erhalten Einblicke in die Qualität und Zuverlässigkeit aller Anrufe, mit denen Teams nutzen. <br><br>Verwenden Sie die CQD-Anweisungen in der Spalte **zusätzliche Informationen** aufgeführt, um den größten Nutzen aus diesem Tool abzurufen. | | [Planung für Dienstverwaltung und Qualität](https://docs.microsoft.com/MicrosoftTeams/envision-planning-for-service-management-and-quality-complete-guide) <br/><br/>[Handbuch für die Qualität Experience-Überprüfung](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/blob/live/Teams/downloads/quality-of-experience-review-guide.docx?raw=true) <br/><br/>[Vorlagen für Qualität-Erfahrung überprüfen](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/blob/live/Teams/downloads/quality-of-experience-review-lite-templates-v-1-2.zip?raw=true) <br/><br/>[Einschalten und Aufrufen Qualitätsdashboard für Microsoft-Teams und Skype für Business Online](https://support.office.com/article/Turning-on-and-using-Call-Quality-Dashboard-for-Microsoft-Teams-and-Skype-for-Business-Online-553fa13c-92d2-4d5c-a3d5-41a073cb047c)<br><br>[Hochladen Sie Erstellen von Informationen](https://docs.microsoft.com/SkypeForBusiness/using-call-quality-in-your-organization/turning-on-and-using-call-quality-dashboard?#upload-building-information) |
| 10  | Überprüfen Sie, dass die Informationen zum Erstellen von verarbeitet ist, und rufen Sie Quality Dashboard (CQD) für Ihre Mandanten funktionsfähig ist. | | | [Rufen Sie die Qualitätsdashboard](https://cqd.lync.com) |