---
title: Zurücksetzen einer Konferenzkennung für einen Benutzer in Microsoft Teams
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.topic: article
ms.assetid: 6e12242c-55f7-4bf4-90d7-0f36c0326b8e
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
- M365-collaboration
audience: Admin
appliesto:
- Microsoft Teams
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Audio Conferencing
- seo-marvel-mar2020
description: Hier finden Sie die Schritte zum Zurücksetzen der Konferenzkennung eines Benutzers in Microsoft Teams sowie Links zu Tools, mit denen Sie Besprechungen aktualisieren und migrieren können.
ms.openlocfilehash: 52b547fee5bf027bcef21914e3ba3aa79b0e4e08
ms.sourcegitcommit: 7a9c63ee790108eaa61950ce28ae8027311039d9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "46662125"
---
# <a name="reset-a-conference-id-for-a-user-in-microsoft-teams"></a>Zurücksetzen einer Konferenzkennung für einen Benutzer in Microsoft Teams

Eine dynamische Konferenzkennung befindet sich unten in Besprechungseinladungen zusammen mit den Dial-in-Telefonnummern, über die sich Anrufer in die Besprechung einwählen können. Wenn Benutzer diese Telefonnummer wählen, werden sie von der automatischen Telefonzentrale aufgefordert, diese Konferenzkennung einzugeben, damit sie an der Besprechung teilnehmen können.
  
> [!NOTE]
> Konferenz-IDs werden automatisch generiert, liegen zwischen 7-9-Ziffern und werden beim Aktivieren von Audiokonferenzen für einen Benutzer eingestellt. **Statische Konferenz-IDs werden nicht unterstützt.** 

## <a name="resetting-the-conference-id-for-a-user"></a>Zurücksetzen der Konferenz-ID für einen Benutzer

![Ein Symbol mit dem Microsoft Teams-Logo](media/teams-logo-30x30.png) **Verwenden des Microsoft Teams Admin Centers**

1. Klicken Sie in der linken Navigationsleiste auf **Benutzer**, und wählen Sie dann den Benutzer in der Liste der verfügbaren Benutzer aus.

2. Klicken Sie auf **Bearbeiten**.

3. Klicken Sie unter **Audiokonferenz** auf **Konferenz-ID zurücksetzen**.

2. Klicken Sie im Fenster **Konferenz-ID zurücksetzen** auf **Zurücksetzen**. Daraufhin wird automatisch eine neue Konferenzkennung erstellt und per E-Mail an den Benutzer gesendet. E-Mails werden standardmäßig an Benutzer gesendet. Dies kann jedoch deaktiviert werden.   

    
> [!NOTE]
> Wenn Sie die Konferenzkennung zurückgesetzt haben, wird eine E-Mail mit der neuen Konferenzkennung an den Benutzer gesendet. Diese e-Mail wird in vielen Fällen an die primäre e-Mail-Adresse gesendet, deren Microsoft 365-oder Office 365-Postfach. Die E-Mail enthält die neue Konferenzkennung, die standardmäßigen Dial-in-Telefonnummern und Anweisungen zum Aktualisieren vorhandener Besprechungen. 
  
> [!Note]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]

## <a name="what-else-should-i-know"></a>Was sollte ich noch wissen?

- Sie können dem Benutzer eine E-Mail mit sämtlichen Konferenzinformationen senden, unter anderem mit der Konferenzkennung und den Dial-in-Telefonnummern. Klicken Sie dazu im Abschnitt **Audiokonferenz** für den Benutzer auf **Send conference info in email** (Konferenzinformationen per E-Mail senden). Die PIN wird nicht gesendet.
    
- Eine 7-9-stellige Konferenz-ID wird vom Teams-Dienst erstellt. Sie können deren Länge nicht ändern.
    
- Nach dem Zurücksetzen wird die neue Konferenz-ID unter **Konferenz-ID** aufgeführt.
    
- Nachdem eine neue Konferenz-ID generiert wurde, können Anrufer die alte Konferenz-ID nicht mehr verwenden. Sie sollten Benutzer benachrichtigen, dass sie ihre angesetzten Besprechungseinladungen neu planen, damit die neue Konferenz-ID den Einladungen hinzugefügt wird. 

## <a name="want-to-know-more-about-windows-powershell"></a>Möchten Sie mehr über Windows PowerShell erfahren?

Bei Windows PowerShell dreht sich alles um das Verwalten von Benutzern und Funktionen, die Benutzer verwenden oder nicht verwenden können. Mit Windows PowerShell können Sie Microsoft 365 oder Office 365 mit einem zentralen Verwaltungspunkt verwalten, der Ihre tägliche Arbeit vereinfachen kann, wenn mehrere Aufgaben ausgeführt werden müssen. Informieren Sie sich in den folgenden Themen über die Verwendung von Windows PowerShell:
    
  - [Warum Sie Office 365 PowerShell verwenden müssen](https://go.microsoft.com/fwlink/?LinkId=525041)
    
  - [Beste Möglichkeiten zum Verwalten von Microsoft 365 oder Office 365 mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=525142)
    
Weitere Informationen zu Windows PowerShell finden Sie in der [PowerShell-Referenz für Microsoft Teams](https://docs.microsoft.com/powershell/module/teams/?view=teams-ps).
    
## <a name="related-topics"></a>Verwandte Themen

[Zurücksetzen der Audiokonferenz-PIN](reset-the-audio-conferencing-pin-in-teams.md)
