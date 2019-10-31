---
title: Kommunizieren mit Benutzern aus anderen Organisationen in Microsoft Teams
author: LolaJacobsen
ms.author: lolaj
manager: serdars
ms.topic: article
ms.service: msteams
audience: admin
ms.collection:
- Teams_ITAdmin_Help
- M365-collaboration
ms.reviewer: vinbel
search.appverid: MET150
description: Erfahren Sie, wie Sie mit Benutzern aus anderen Organisationen in Microsoft Teams über externen Zugriff (Partnerverbund) und Gastzugriff kommunizieren können.
appliesto:
- Microsoft Teams
localization_priority: Priority
ms.openlocfilehash: a777baed1d5cc35788b2c4f63741317e34eb7905
ms.sourcegitcommit: 09e719ead5c02b3cfa96828841c4905748d192a3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2019
ms.locfileid: "37754371"
---
<a name="communicate-with-users-from-other-organizations-in-microsoft-teams"></a>Kommunizieren mit Benutzern aus anderen Organisationen in Microsoft Teams
======================================================

Wenn Sie mit Personen außerhalb Ihrer Organisation kommunizieren und zusammenarbeiten müssen, bietet Ihnen Microsoft Teams zwei verschiedene Möglichkeiten, dies zu bewerkstelligen. Die erste Möglichkeit ist der **externe Zugriff** (Partnerverbund), mit dem Sie Benutzer in anderen Domänen (z.B. contoso.com) finden, anrufen und mit ihnen chatten können. Die zweite Möglichkeit ist der **Gastzugriff**, mit dem Sie Personen über ihre E-Mail-Adresse zu Ihren Teams als Gäste hinzufügen können. Sie können mit Gästen wie mit allen anderen Benutzern in Ihrer Organisation zusammenarbeiten.

Auf einer hohen Ebene ist hier die Auswahl (für einen detaillierten Vergleich scrollen Sie nach unten, zu [Externer Zugriff und Gastzugriff vergleichen](#compare-external-and-guest-access)):

## <a name="external-access"></a>Externer Zugriff

Verwenden Sie den **externen Zugriff** (Partnerverbund), wenn Sie eine Lösung benötigen, die es externen Benutzern in anderen Domänen ermöglicht, Sie zu finden, anzurufen, mit Ihnen zu chatten und Meetings zu organisieren. Externe Benutzer haben keinen Zugriff auf die Teams oder Teamressourcen Ihrer Organisation. Wählen Sie einen externen Zugang, wenn Sie mit externen Benutzern kommunizieren möchten, die noch auf Skype for Business (online oder vor Ort) oder Skype (verfügbar Anfang 2020) arbeiten. 

Der externe Zugriff ist in Teams standardmäßig aktiviert. Das bedeutet, dass Ihre Organisation mit allen externen Domänen kommunizieren kann. Der Team-Administrator kann es deaktivieren oder angeben, welche Domänen ein- oder ausgeschlossen werden sollen. Weitere Informationen hierzu finden Sie unter [Verwalten des externen Zugriffs](manage-external-access.md). 

Wenn Sie externen Benutzern hingegen den Zugriff auf Teams und Kanäle gewähren möchten, ist der [Gastzugriff](#guest-access) möglicherweise besser geeignet. 


## <a name="guest-access"></a>Gastzugriff

Verwenden Sie den **Gastzugriff**, um einen einzelnen Benutzer (unabhängig von der Domäne) zu einem Team hinzuzufügen, wo er chatten, anrufen, sich mit anderen treffen und an Unternehmensdateien (gespeichert in SharePoint oder OneDrive for Business) mit Office 365-Anwendungen wie Word, Excel oder PowerPoint zusammenarbeiten kann. Einem Gastbenutzer können fast alle Funktionen des Teams wie einem nativen Teammitglied zur Verfügung gestellt werden. Weitere Informationen finden Sie unter [Gastzugriff in Teams](guest-access.md).

- Gäste werden der Active Directory Ihrer Organisation hinzugefügt.
- Um mit einem Gast zu kommunizieren, muss der Gast mit seinem Gastkonto bei Teams angemeldet sein. Das bedeutet, dass sich ein Gast möglicherweise von seinem eigenen Team-Konto abmelden muss, um sich bei Ihrem Team-Konto anzumelden.
- Gastbenutzer haben Zugriff auf mehr Ressourcen in Teams, wie Dateien, Teams und Kanäle, als Benutzer mit externem Zugriff (Partnerverbund).
- Der Team-Administrator steuert alles, was ein Gast im Team-Admin Center tun kann (oder nicht kann). Weitere Informationen hierzu finden Sie unter [Verwalten des Gastzugriffs](manage-guests.md).

Wenn Sie bereit sind, den Gastzugriff in Ihrer Organisation zu aktivieren, starten Sie mit der [Checkliste für den Gastzugriff](guest-access-checklist.md).


## <a name="compare-external-and-guest-access"></a>Vergleich zwischen externem Zugriff und Gastzugriff

| Feature | Benutzer mit externem Zugriff | Benutzer mit Gastzugriff |
|---------|-----------------------|--------------------|
| Der Benutzer kann mit jemandem in einem anderen Unternehmen chatten. | Ja |Ja |
| Der Benutzer kann jemanden in einem anderen Unternehmen anrufen | Ja | Ja |
| Der Benutzer kann sehen, ob jemand aus einem anderen Unternehmen für Anrufe oder Chats verfügbar ist | Ja | Ja<sup>1</sup> |
| Der Benutzer kann auf externen Mandanten nach Benutzern suchen | Ja<sup>2</sup> | Nein |
| Der Benutzer kann Dateien freigeben | Nein | Ja |
| Der Benutzer kann auf Microsoft Teams-Ressourcen zugreifen | Nein | Ja |
| Der Benutzer kann zu einem Gruppenchat hinzugefügt werden | Nein | Ja |
| Der Benutzer kann zu einer Besprechung hinzugefügt werden | Ja | Ja |
| Weitere Benutzer können zu einem Chat mit einem externen Benutzer hinzugefügt werden | No<sup>3</sup> | Nicht zutreffend |
| Der Benutzer wird als externer Partner gekennzeichnet | Ja | Ja |
| Anwesenheit wird angezeigt | Ja | Ja |
| Abwesenheitsnachricht wird angezeigt | Nein | Ja |
| Ein einzelner Benutzer kann blockiert werden | Nein | Ja |
| @Mentions werden unterstützt | Ja<sup>4</sup> | Ja |
| Private Anrufe führen | Ja | Ja |
| IP-Video zulassen | Ja | Ja |
| Bildschirmübertragungsmodus | Ja<sup>4</sup> | Ja |
| Sofortbesprechungen zulassen | Nein | Ja |
| Gesendete Nachrichten bearbeiten | Ja<sup>4</sup> | Ja |
| Löschen gesendeter Nachrichten möglich | Ja<sup>4</sup> | Ja |
| Giphy in Unterhaltung verwenden | Ja<sup>4</sup> | Ja |
| Memes in Unterhaltung verwenden | Ja<sup>4</sup> | Ja |
| Sticker in Unterhaltung verwenden | Ja<sup>4</sup> | Ja |
||||

<sup>1</sup> Vorausgesetzt, der Benutzer wurde als Gast hinzugefügt und hat sich als Gast beim Gastmandanten angemeldet.<br>
<sup>2</sup> Nur per E-Mail- oder SIP-Adresse (Session Initiation Protocol).<br>
<sup>3</sup> Externer Chat (Verbundchat) nur 1:1.<br>
<sup>4</sup> Unterstützt für 1:1-Chat nur für Teams zu Teams Benutzer aus zwei verschiedenen Organisation. *Dies ist eine Vorschauversion oder eine Vorabfunktion.*

## <a name="related-topics"></a>Verwandte Themen

[Externer Zugriff in Teams](manage-external-access.md)

[Gastzugriff in Teams](guest-access.md)
