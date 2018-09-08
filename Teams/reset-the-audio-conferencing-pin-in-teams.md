---
title: Zurücksetzen der Audiokonferenz PIN in Microsoft-Teams
mms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.topic: article
ms.assetid: 67866a47-89c1-4593-8766-3a68777e2be6
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
search.appverid: MET150
ms.collection:
- Adm_Skype4B_Online
- Strat_SB_PSTN
ms.audience: Admin
appliesto:
- Microsoft Teams
localization_priority: Priority
f1keywords: None
ms.custom:
- Audio Conferencing
description: 'Erfahren Sie, was Sie Drehbezugspunkten wissen sollten und wie Sie sie in der Microsoft-Teams, zurücksetzen. '
ms.openlocfilehash: 4570c96ab529c114f2d0bb8708eb145650de18b1
ms.sourcegitcommit: 2a6e499165424fe2d189ad140951e222c8ba9c81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2018
ms.locfileid: "23866467"
---
# <a name="reset-the-audio-conferencing-pin-in-microsoft-teams"></a>Zurücksetzen der Audiokonferenz PIN in Microsoft-Teams

Eine PIN ist ein Code bestehend aus Zahlen, die für jeden Benutzer von Microsoft-Teams erstellt werden, die für Audiokonferenzen aktiviert ist. Audiokonferenzen PINs von Besprechungsorganisatoren dienen zum Identifizieren, sie der Organisator der Besprechung sind und ermöglicht es ihnen, eine Besprechung über das Telefon zu starten. Wenn sie die Microsoft-Teams app verwenden, um die Besprechung beginnen, ist eine PIN nicht erforderlich. Wenn Benutzer ihre PIN vergessen, und sie können nicht gefunden werden in der e-Mail, die an sie gesendet wurde, wenn sie für die Audiokonferenz aktiviert wurden, ein Administrator kann ihre PIN zurücksetzen, oder sie können ihre eigenen PIN zurücksetzen.
  
Besprechungen können gestartet werden, wenn ein authentifizierter Benutzer Beitritt mithilfe der Anwendung Microsoft-Teams, oder wenn der Organisator mit seinem PIN über das Telefon Beitritt. Wenn die Besprechung zum Starten eine PIN erfordert, werden alle Benutzer, die sich per Telefon einwählen standardmäßig im Wartebereich platziert und hören Warteschleifenmusik, bis die Besprechung beginnt. Wenn der Organisator einer Besprechung keine PIN zum Starten der Besprechung per Telefon benötigt, werden Anrufer nicht nach einer PIN gefragt, wenn sie sich für die Besprechung einwählen.

## <a name="reset-a-users-pin"></a>Zurücksetzen der PIN eines Benutzers

1. Im linken Navigationsbereich klicken Sie auf **Benutzer**, und wählen Sie dann den Benutzer aus der Liste der verfügbaren Benutzer aus.

2. Klicken Sie am oberen Rand der Seite auf **Bearbeiten**.

3. Klicken Sie unter **Audiokonferenzen**klicken Sie auf **PIN zurücksetzen**.
 
> [!Note]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]
   
## <a name="have-a-user-reset-his-or-her-own-pin"></a>Ein Benutzer seine PIN zurücksetzen

1. Bitten Sie den Benutzer, wechseln Sie zur [https://admin0m.online.lync.com/lscp/usp/pstnconferencing](https://admin0m.online.lync.com/lscp/usp/pstnconferencing).
2. Klicken Sie auf **Zurücksetzen PIN**. 


## <a name="what-else-should-you-know-about-pins"></a>Was sollten Sie sonst über PINs wissen?

- Aus Sicherheitsgründen wird die PIN einem Administrator nur ein Mal gezeigt, wenn die PIN zurückgesetzt wird. Nachdem die PIN durch einen Administrator zurückgesetzt wird, werden die PIN-Nummer als aufgelistet ***.
    
- Automatisch Senden von e-Mails an Benutzer ist standardmäßig aktiviert, und Benutzer erhalten eine e-Mail mit ihrer PIN, wenn sie aktiviert sind, für Audiokonferenzen oder wenn die PIN zurückgesetzt wird. Aber wenn Sie automatisch deaktiviert haben Senden von e-Mails, eine PIN zurücksetzen-e-Mail wird nicht an einen Benutzer gesendet werden und Sie müssen die PIN-Informationen für den Benutzer manuell veranlassen.
    
- Beim Start einer Besprechung nehmen alle Benutzer im Wartebereich automatisch an dieser teil. Wenn beispielsweise 2 Teilnehmer versuchen, vor dem Start der Besprechung an dieser teilzunehmen, werden sie im Wartebereich platziert und hören Warteschleifenmusik. Sobald der Organisator der Besprechung mit seiner PIN per Telefon teilnimmt, beginnt die Besprechung und alle Teilnehmer im Wartebereich nehmen an der Besprechung teil.
    
- Die Standardeinstellung ist mit eine Besprechung gestartet werden, indem anonyme Anrufer nicht zu ermöglichen.
    
- Wenn Sie einen Benutzer für Audiokonferenzen aktivieren, werden standardmäßig sie-e-Mails gesendet, die Informationen zur Telefonkonferenz und ihre PIN enthalten. Der Benutzer muss ein Office 365-Postfach verfügen, da beim Zurücksetzen einer PIN ist eine neue PIN in e-Mails an ihre primäre SMTP-Adresse (Alias) an den Benutzer gesendet wird, die für den Benutzer festgelegt ist.
    
- Wenn Sie Audiokonferenzen eingerichtet haben, legen Sie die Ziffern, die für die PINs in Ihrer Organisation erforderlich sind. PINs können 4 bis 12 Ziffern enthalten, standardmäßig werden 5 Ziffern verwendet. Wenn Sie die PIN-Länge-Einstellung ändern, wird diese Einstellung gilt nur für neu generierte PINs und wird nicht angewendet, um die PIN-Einstellung für vorhandene Benutzer, die für Audiokonferenzen aktiviert sind. Finden Sie unter [Legen Sie die PIN für Audiokonferenzen Besprechungen](Set-the-PIN-length-for-Audio-Conferencing-meetings-in-teams.md).
    
- Die e-Mail standardmäßig wird auf die Office 365 primäre SMTP-Adresse des Benutzers festgelegt werden. Sie können eine e-Mail an eine nicht - Office 365-Adresse wie Hotmail oder MSN e-Mail-Adresse senden. Mithilfe von Windows PowerShell können Sie die Standard-e-Mail-Adresse außer Kraft setzen. Dies ist nützlich, wenn der Benutzer nicht über ein Exchange-Postfach in Office 365 verfügen.

    

## <a name="want-to-know-more-about-windows-powershell"></a>Möchten Sie mehr über Windows PowerShell erfahren?

Bei Windows PowerShell dreht sich alles um das Verwalten von Benutzern und Funktionen, die Benutzer verwenden oder nicht verwenden können. Mit Windows PowerShell können Sie Office 365 über einen zentralen Administrationspunkt verwalten und so Ihre tägliche Arbeit vereinfachen. Informieren Sie sich in den folgenden Artikeln über die Verwendung von Windows PowerShell:
    
  - [Warum Sie Office 365 PowerShell verwenden müssen](https://go.microsoft.com/fwlink/?LinkId=525041)
    
  - [Beste Möglichkeiten zum Verwalten von Office 365 mit der Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=525142)
    
Weitere Informationen zu Windows PowerShell finden Sie in der [Referenz zu Microsoft-Teams PowerShell](https://docs.microsoft.com/powershell/module/teams/?view=teams-ps) für Weitere Informationen.
  
## <a name="related-topics"></a>Verwandte Themen

[Zurücksetzen einer Konferenzkennung für einen Benutzer](reset-a-conference-id-for-a-user-in-teams.md)