---
title: Problembehandlung und bekannte Probleme bei Audiokonferenzen
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.date: 01/22/2018
ms.topic: article
ms.assetid: 72979911-5319-4de2-a275-4dd9a0f44fe6
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
ms.collection: Adm_Skype4B_Online
ms.audience: Admin
appliesto:
- Skype for Business
- Microsoft Teams
localization_priority: Normal
f1keywords: None
ms.custom:
- Strat_SB_PSTN
- Audio Conferencing
description: 'Rufen Sie eine Liste bekannter Probleme bei Verwendung von Microsoft als Anbieternamens einwahlkonferenz, Status und umgangen. '
ms.openlocfilehash: 9e566d0ba9f07aeecca222ef586f301b1cd6cf5f
ms.sourcegitcommit: 94e32f776364b0aaefe2d2d72062ec1c249eaef3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2018
---
# <a name="audio-conferencing-troubleshooting-and-known-issues"></a>Problembehandlung und bekannte Probleme bei Audiokonferenzen

 **Dieser Artikel richtet sich an Skype for Business- und Microsoft Teams-Benutzer, die Microsoft als Audiokonferenzanbieter verwenden. Er ist nicht für Kunden gedacht, die einen Drittanbieter für Audiokonferenzen (Audio Conferencing Provider, Audiokonferenzanbieter (ACP)) verwenden.**
  
## <a name="troubleshooting-and-known-issues"></a>Problembehandlung und bekannte Probleme

Bei Audiokonferenzen mit Microsoft als Audiokonferenzanbieter sind aktuelle Probleme bekannt, die nachverfolgt, aktiv untersucht und potentiell gelöst werden, wenn die Funktion in zukünftigen Versionen von Office 365 aktualisiert wird.
  
Nutzen Sie diese Dokumentation für den Moment als Referenz bei der Behandlung potentieller Probleme bei der Konfiguration und Inbetriebnahme von Audiokonferenzen für die Benutzer der Skype for Business- oder Microsoft Teams-App in Ihrer Organisation.
  
### <a name="microsoft-teams-app"></a>Microsoft Teams-App

|**Problem**|**Verhalten/Symptome**|**Bekannte Problemumgehung**|**Datum der Erkennung**|
|:-----|:-----|:-----|:-----|
|PSTN-Anrufer mit der gleichen „Von"-Nummer werden in der Teilnehmerliste der Besprechung als derselbe Benutzer angezeigt.  <br/> |Wenn mehrere PSTN-Anrufer an einer Besprechung teilnehmen und ihre Anrufer-IDs als eine einzige Nummer gekennzeichnet sind, werden diese Anrufer in der Teilnehmerliste der Besprechung als ein einziger Anrufer angezeigt.  <br/> |Keine Problemumgehung  <br/> |25.9.2017  <br/> |
|Der Bereich mit den Besprechungsinformationen wird zeitweise nicht angezeigt.  <br/> |Der Bereich mit den Besprechungsinformationen wird im Teams-Client möglicherweise nicht angezeigt, wenn Benutzer versuchen, Telefonnummern einer Konferenzbrücke oder Konferenzkennungen nachzuschlagen.  <br/> |Sie können die Telefonnummern einer Konferenzbrücke oder Konferenzkennungen in den Besprechungsdetails oder im Outlook-Kalender anzeigen.  <br/> |25.9.2017  <br/> |
|Besprechungseinladungen über das Outlook-Add-In enthalten sinnlose Zeichen in PSTN-Koordinaten für Nicht-US-Gebietsschemas.  <br/> |Beim Planen von privaten Besprechungen mit dem Outlook-Add-In für Microsoft Teams auf einem Computer mit Nicht-US-Gebietsschemas enthalten PSTN-Koordinaten möglicherweise sinnlose Zeichen.  <br/> |Keine Problemumgehung  <br/> |25.9.2017  <br/> |
|Bei der Auswahl müssen mindestens fünf Ziffern verwendet werden.  <br/> |Benutzer, die aus einer Besprechung eine Nummer zu wählen versuchen, müssen mindestens fünf Ziffern eingeben, obwohl eine Wählplan-Normalisierungsregel verfügbar ist, durch die gewählte kurze Nummern in E.164 normalisiert werden.  <br/> |Geben Sie bei der Auswahl anstelle der internen Durchwahlnummer die Nummer im vollständigen Durchwahlnummernformat oder lokalen Nummernformat ein.  <br/> |25.9.2017  <br/> |
|Das Auswahlsteuerelement wird zeitweise nicht angezeigt.  <br/> |Das Auswahlsteuerelement ist möglicherweise im Bereich mit den Besprechungsinformationen nicht sichtbar.  <br/> |Keine Problemumgehung  <br/> |25.9.2017  <br/> |
|Statische Konferenzkennungen werden für Microsoft Teams-Besprechungen nicht unterstützt.  <br/> |Wenn der Administrator die Standardeinstellung außer Kraft setzt und sie von einer dynamischen Konferenzkennung in eine statische Konferenzkennung ändert, wird diese Einstellung für Microsoft Teams-Besprechungen nicht wirksam. Finden Sie unter [Audiokonferenzen mithilfe von dynamischen IDs in Ihrer Organisation](using-audio-conferencing-dynamic-ids-in-your-organization.md).  <br/> |Keine Problemumgehung  <br/> |25.9.2017  <br/> |
   
### <a name="skype-for-business-app"></a>Skype for Business-App

|**Problem**|**Verhalten/Symptome**|**Bekannte Problemumgehung**|**Datum der Erkennung**|
|:-----|:-----|:-----|:-----|
|Benachrichtigungen bei Zu- oder Abgang sind zu Beginn einer Besprechung aktiviert, werden aber kurz darauf deaktiviert.  <br/> |Die Benachrichtigungen bei Zu- oder Abgang sind für Besprechungen, an denen Teilnehmer sowohl über Skype for Business-Apps als auch per Einwahl teilnehmen, standardmäßig deaktiviert. Sie können die Ankündigungen in den **Skype-Besprechungsoptionen** in der Skype for Business-App aktivieren. Bei einer Besprechung, an der alle Teilnehmer durch Einwahl teilnehmen, sind die Benachrichtigungen bei Zu- oder Abgang standardmäßig aktiviert, da den Teilnehmern keine Teilnehmerliste zur Verfügung steht. Wenn eine Besprechung ausschließlich mit Teilnehmern begonnen hat, die durch Einwahl teilnehmen, werden die Benachrichtigungen bei Zu- oder Abgang aktiviert. Wenn jedoch ein Teilnehmer über eine Skype for Business-App teilnimmt, werden die Benachrichtigungen deaktiviert. Deaktivierte Benachrichtigungen können mithilfe der **Skype-Besprechungsoptionen** in der Skype for Business-App wieder aktiviert werden. <br/> |Keine Problemumgehung  <br/> |30.8.2017  <br/> |
|Wenn ein Benutzer durch Zuweisen einer E5-Lizenz erstmals bereitgestellt wird und das Postfach nicht aktiviert ist, wird die Begrüßungs-E-Mail für Audiokonferenzen möglicherweise nicht zugestellt.  <br/> |In diesem Fall können Sie die Informationen zur Audiokonferenz jederzeit mit der Option **Audio conferencing** (Audiokonferenz) im Skype for Business Admin Center oder mit PowerShell erneut an den Benutzer senden. Finden Sie unter [Aktivieren oder deaktivieren Sie e-Mails senden, wenn Audiokonferenzen Einstellungen ändern](enable-or-disable-sending-emails-when-their-settings-change.md).  <br/> **Hinweis:** Um dem Benutzer die Audiokonferenz PIN erneut zu senden, muss die PIN zurückgesetzt werden. Dies kann auch über die Option **Audio conferencing** (Audiokonferenz) im Skype for Business Admin Center oder mithilfe von PowerShell geschehen.          |Keine Problemumgehung  <br/> |30.8.2017  <br/> |
|Es kann bis zu 24 Stunden dauern, bis Audiokonferenzanrufe in den Nutzungsberichten angezeigt werden.  <br/> |Für diesen Bereich sind in zukünftigen Dienstupdates Verbesserungen geplant.  <br/> |Keine Problemumgehung  <br/> |30.8.2017  <br/> |
|Wenn sich ein Anrufer in eine Konferenzbrücke einwählt, nachdem die Besprechung von einem Skype for Business-Benutzer gesperrt wurde, wird in derSkype for Business-App keine Benachrichtigung dazu angezeigt, dass der Benutzer im Wartebereich wartet.  <br/> |Dies ist zurzeit entwurfsbedingt, wir werden jedoch Ihr Feedback hinsichtlich der Unterstützung dieser Funktion in zukünftigen Dienstupdates berücksichtigen.  <br/> |Keine Problemumgehung  <br/> |30.8.2017  <br/> |
   
## <a name="related-topics"></a>See Also

[Einrichten von Audiokonferenzen für Skype for Business und Microsoft Teams](set-up-audio-conferencing.md)
  
