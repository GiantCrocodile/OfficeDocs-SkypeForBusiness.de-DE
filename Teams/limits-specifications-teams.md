---
title: Grenzwerte und Spezifikationen für Microsoft-Teams
author: LolaJacobsen
ms.author: lolaj
manager: serdars
ms.date: 04/09/2018
ms.topic: article
ms.service: msteams
ms.reviewer: ninadara
description: Lernen Sie die Grenzwerte für die Spezifikationen und anderen Anforderungen für Microsoft-Teams.
MS.collection: Strat_MT_TeamsAdmin
appliesto:
- Microsoft Teams
ms.openlocfilehash: dff28cb59dabbf3d9d43dbde00cba73541280b39
ms.sourcegitcommit: dea27df69d948b7b9cc017b7023c4013cee8e4d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
<a name="limits-and-specifications-for-microsoft-teams"></a>Grenzwerte und Spezifikationen für Microsoft-Teams
=============================================

Dieser Artikel beschreibt einige der die Grenzwerte für die Spezifikationen und anderen Anforderungen für Microsoft-Teams. 

<a name="teams-and-channels"></a>Teams und Kanäle 
------------------

|Funktion    | Maximale Grenzwert |
|-----------|---------------|
|Anzahl der Teams, die ein Benutzer erstellen kann | 250         |
|Anzahl der Elemente in einem team | 2.500       |
|Anzahl der Teams, die ein globaler Administrator erstellen können        | Unbegrenzt   |
|Anzahl der Teams, die ein Office 365-Mandanten enthalten kann    | 500.000     |
|Anzahl der Kanäle pro team    | 200         |

<a name="meetings-and-calls"></a>Besprechungen und Telefonkonferenzen 
------------------

|Funktion     | Maximale Grenzwert |
|------------|---------------|
|Anzahl der Personen in einer Besprechung  | 80    |
|Anzahl der Personen in einem privaten chat  | 20    |

<a name="storage"></a>Speicher
-------

Jedes Team in Microsoft Teams verfügt über eine Teamsite in SharePoint Online, und jeder Kanal in einem Team erhält einen Ordner innerhalb der Dokumentbibliothek der Standardteamsite. In einer Unterhaltung freigegebene Dateien werden automatisch zur Dokumentbibliothek hinzugefügt, und in SharePoint festgelegte Berechtigungen und Dateisicherheitsoptionen werden automatisch in Teams übernommen.

Wenn Sie SharePoint Online in Ihrem Mandanten aktiviert ist, können nicht Microsoft-Teams, Benutzer immer Dateien in Teams freigeben. Benutzer im privaten Chat können nicht auch Dateien freigeben, da OneDrive für Unternehmen (die SharePoint-Benutzerlizenz verbunden ist) der Funktionalität erforderlich ist.

Beim Speichern der Dateien in der SharePoint Online-Dokumentbibliothek und OneDrive for Business werden alle auf der Mandantenebene konfigurierten Complianceregeln eingehalten. (Weitere finden Sie unter [wie SharePoint Online und OneDrive für Unternehmen interagieren mit Microsoft-Teams,](sharepoint-onedrive-interact.md).)

Da Teams, die auf einer SharePoint Online-Back-End für die Dateifreigabe ausgeführt wird, gelten SharePoint Einschränkungen in den Abschnitt Dateien innerhalb eines Teams. Hier sind die entsprechenden Speichergrenzwerte für SharePoint Online.

|Funktion                 |Office 365 Business Essentials  |Office 365 Business Premium   |Office 365 Enterprise E1  |Office 365 Enterprise E3  |Office 365 Enterprise E5  |Office 365 Enterprise F1  |
|------------------------|---------|---------|---------|---------|---------|---------|
|Speicher                 |1 TB pro Organisation plus 0,5 GB pro erworbene Lizenz  |1 TB pro Organisation plus 0,5 GB pro erworbene Lizenz  |1 TB pro Organisation plus 0,5 GB pro erworbene Lizenz   |1 TB pro Organisation plus 0,5 GB pro erworbene Lizenz |1 TB pro Organisation plus 0,5 GB pro erworbene Lizenz  |1 TB pro Organisation           |
|Speicher für Teams Dateien |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |Bis zu 25 TB pro Websitesammlung oder Gruppe |
|Maximale Dateigröße beim upload       |15 GB    |15 GB    |15 GB    |15 GB    |15 GB    |15 GB    |

Jede Registerkarte Dateien in Teams führt auf einer SharePoint Online Back-End, gilt die oben genannten Speichergrenzwerte für jeden Kanal innerhalb eines Teams.

Weitere Informationen finden Sie unter [SharePoint Online-Begrenzungen](https://support.office.com/en-us/article/SharePoint-Online-limits-8f34ff47-b749-408b-abc0-b605e1f6d498).

<a name="messaging"></a>Messaging
---------

Benutzer, die Unterhaltungen teilnehmen, die Teil der Liste der Chat in Microsoft-Teams sind benötigen ein Exchange Online (Cloud-basierten) Postfach für ein Administrator Chat Unterhaltungen suchen. Dies liegt daran Unterhaltungen, die Teil der Liste der Chat sind in der Cloud-basierten Postfächern Chat Teilnehmer gespeichert sind. Wenn ein Teilnehmer Chat ein Exchange Online-Postfach besitzt, werden nicht der Administrator suchen oder einen Haltestatus auf Chat Unterhaltungen setzen. Beispielsweise können in einer Exchange-hybridbereitstellung Benutzer mit lokalen Postfächern möglicherweise zur Teilnahme an Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams sind. Jedoch in diesem Fall Inhalte aus dieser Unterhaltungen nicht durchsuchbaren und kann nicht in der Warteschleife platziert werden, da der Benutzer nicht über cloudbasierten Postfächer verfügen. (Weitere finden Sie unter [wie Exchange- und Microsoft-Produktteams interagieren](exchange-teams-interact.md).)

Microsoft-Teams, Chat Funktion arbeitet auf einem Microsoft Exchange Back-End-Exchange-messaging-Grenzwerten in Microsoft-Teams, die Chat-Funktion angewendet werden kann. Wenn Benutzer eine e-Mail in einem Kanal Teams senden möchten, verwenden sie die e-Mail-Adresse des DDE-Kanal. Nachdem eine e-Mail-Nachricht einen Kanal gehört, kann alle Benutzer auf, um eine Unterhaltung zu beginnen Antworten. Hier sind einige der entsprechenden Grenzwerte für das Senden von e-Mails an einen Kanal. 

|Funktion  |Office 365 Enterprise E1  |Office 365 Enterprise E3  |Office 365 Enterprise E5  |Office 365 Enterprise F1  |
|---------|---------|---------|---------|---------|
|Die Nachrichtengröße&dagger;  |25 KB   |25 KB   |25 KB   |25 KB   |
|Grenzwert für Dateianlagen&Dagger;  |20     |20     |20     |20    |
|Beschränken der Bilder&Dagger; |50   |50   |50   |50   |

&dagger;Wenn die Nachricht diesen Grenzwert überschreitet, wird eine Vorschau der Nachricht wird generiert, und der Benutzer wird aufgefordert, Ansicht/die ursprüngliche e-Mail aus den angezeigten Link herunterladen.

&Dagger;Wenn die Anzahl der Anlagen oder Bilder diesen Grenzwert überschreitet, die Nachricht nicht verarbeitet werden, und eine Unzustellbarkeitsbericht E-mail an den Absender benachrichtigen des Fehlers gesendet.

Weitere Informationen finden Sie unter [Exchange Online-Begrenzungen](https://technet.microsoft.com/library/exchange-online-limits.aspx).

<a name="browsers"></a>Browser 
--------

[!INCLUDE [browser-support](includes/browser-support.md)]

<a name="operating-systems"></a>Betriebssysteme
-----------------

Informationen zu betriebssystemanforderungen finden Sie unter [Get-Clients für Microsoft-Teams](get-clients.md).

