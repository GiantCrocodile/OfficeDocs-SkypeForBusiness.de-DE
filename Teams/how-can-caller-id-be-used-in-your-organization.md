---
title: Verwendungsmöglichkeiten der Anrufer-ID in Ihrer Organisation
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.reviewer: mikedav, roykuntz
ms.topic: article
ms.assetid: 5a0bd8ba-3334-46ee-becf-1025597737f6
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
search.appverid: MET150
ms.collection:
- M365-voice
audience: Admin
appliesto:
- Skype for Business
- Microsoft Teams
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Calling Plans
- ms.teamsadmincenter.voice.callerid.overview
description: Die Rufnummernanzeige kann für eingehende und ausgehende Anrufe für Telefon System Benutzer unter Verwendung einer Richtlinie mit dem Namen CallingLineIdentity gesteuert werden.
ms.openlocfilehash: cd2074fec3027f1172b6ea681013f53994963cb5
ms.sourcegitcommit: 2874aec7768bb46ed4506c1a2d431841f47190bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "47255448"
---
# <a name="how-can-caller-id-be-used-in-your-organization"></a>Verwendungsmöglichkeiten der Anrufer-ID in Ihrer Organisation

Die Rufnummernanzeige kann für eingehende und ausgehende Anrufe für Telefon System Benutzer unter Verwendung einer Richtlinie mit dem Namen CallingLineIdentity gesteuert werden.
  
Die Rufnummernanzeige Funktion steht allen Telefon System Benutzern unabhängig von der PSTN-Konnektivität zur Verfügung:

- Microsoft-Anrufpläne 

- Direktes Routing für Telefonsysteme 
  
- Online-PSTN-Anbindung
    
- Lokale PSTN-Anbindung mit Skype for Business Cloud Connector Edition (erfordert Cloud Connector Edition 1.4.2 oder höher)
    
- Lokale PSTN-Anbindung mit Skype for Business Server (erfordert Skype for Business Server 2015 CU5 oder höher)
    
> [!NOTE]
> Diese Richtlinie ist in Skype for Business Server 2015 nicht verfügbar. 
  
## <a name="outbound-caller-id"></a>Ausgehende Anrufer-ID

Für ausgehende PSTN-Rufnummernanzeige stehen drei Optionen zur Verfügung:
  
- Die dem Benutzer zugewiesene Telefonnummer, die der Standardwert ist.
    
- Eine Telefonnummer, die als *Service* *-und gebührenfreie* Nummer in der Telefonnummern Inventur Ihres Anruf Plans eingestuft wird. Sie wird normalerweise einer automatischen Telefonzentrale oder einer Anruf-Warteschleife Ihrer Organisation zugewiesen.
    
- Auf „Anonym" festgelegt
    
Die folgenden Arten von Telefonnummern können Sie jedoch nicht als ausgehende Anrufer-ID nicht zuweisen:
  
- Alle Telefonnummern, die in ihren Anrufplänen als  *Benutzer*  klassifiziert sind Telefonnummern Inventar
    
- Lokale Skype for Business Server-Telefonnummern
    
Informationen zum Festlegen der ausgehenden Anrufer-ID finden Sie unter [Festlegen der Anrufer-ID für einen Benutzer](/microsoftteams/set-the-caller-id-for-a-user).
  
### <a name="end-user-control-of-outbound-caller-id"></a>Endbenutzer Steuerung der ausgehenden Anrufer-ID

Das EnableUserOverride-Attribut ermöglicht es einzelnen oder mehreren Benutzern, Ihre Einstellungen für die Rufnummernanzeige in **Anonymous**zu ändern. Dies gilt nur, wenn eine CallingLineIdentity -Richtlinie mit dem CallingIDSubstitute -Parameter LineURI oder Substitute konfiguriert ist. Der Standardwert von EnableUserOverride lautet False.
  
Ihre Endbenutzer können Ihre Anrufer-ID auf **Anonym** festlegen, indem Sie auf der Registerkarte **Einstellungen** im Skype for Business-Desktop Client die Option **Endbenutzer anrufen** (sofern vom Administrator aktiviert) auswählen und dann **meine Telefonnummer und Profilinformationen für alle Anrufe verbergen**auswählen. In Teams können Benutzer in der oberen rechten Ecke zu Ihrem Profilbild wechseln, **Einstellungen**  >  **anrufen**auswählen und dann unter **Rufnummern**Anzeige die Option **meine Telefonnummer und Profilinformationen für alle Anrufe verbergen**auswählen.
  
||||
|:-----|:-----|:-----|
|**Windows** <br/> |**Version** <br/> |**Unterstützt** <br/> |
|Klick-und-Los  <br/> |Aktueller Kanal, Veröffentlichung am 6. Dezember 2016 - Version 1611 (Build 7571.2072)  <br/> |Ja  <br/> |
|Klick-und-Los  <br/> |First Release für verzögerten Kanal, Veröffentlichung am 22. Februar 2017 - Version 1701 (Build 7766.2060)  <br/> |Ja  <br/> |
|Klick-und-Los  <br/> |Veröffentlichung im verzögerten Kanal am 13. Juni 2017 - Version 1701 (Build 7766.2092)  <br/> |Ja  <br/> |
|MSI  <br/> |Skype for Business  <br/> |Nein  <br/> |
|Mac  <br/> |Skype for Business  <br/> |Nein  <br/> |
   
## <a name="inbound-caller-id"></a>Eingehende Anrufer-ID

Das Telefon System zeigt die benannte ID für eine externe Telefonnummer an, wenn die Nummer einem Benutzer in Azure AD zugeordnet ist. Wenn sich die Telefonnummer nicht in Azure AD befindet, wird der von Telco bereitgestellte Anzeigename angezeigt, wenn er verfügbar ist.

Mit dem Attribut BlockIncomingCallerID können Sie die Anrufer-ID Für eingehende PSTN-Anrufe blockieren. Sie können dieses Attribut festlegen, das jedoch für Ihre Endbenutzer auf der Seite "Benutzereinstellungen" nicht verfügbar ist. Außerdem ist das Attribut zurzeit nur für Online-PSTN-Anbindung verfügbar.
  
Informationen zum Festlegen der ausgehenden Anrufer-ID finden Sie unter [Festlegen der Anrufer-ID für einen Benutzer](/microsoftteams/set-the-caller-id-for-a-user).
  
## <a name="related-topics"></a>Verwandte Themen
[Übertragen von Telefonnummern – häufig gestellte Fragen](/microsoftteams/transferring-phone-numbers-common-questions)

[Verschiedene Arten von Telefonnummern, die für Anrufpläne verwendet werden](/microsoftteams/different-kinds-of-phone-numbers-used-for-calling-plans)

[Verwalten von Telefonnummern für Ihre Organisation](/microsoftteams/manage-phone-numbers-for-your-organization)

[Nutzungsbedingungen für Notrufe](/microsoftteams/emergency-calling-terms-and-conditions)

[Skype for Business Online: Aufkleber mit Haftungsausschluss für Notrufe](https://github.com/MicrosoftDocs/OfficeDocs-SkypeForBusiness/blob/live/Teams/downloads/emergency-calling/emergency-calling-label-(en-us)-(v.1.0).zip?raw=true)

  
 
