---
title: Skype für Unternehmen auf Mac-Clientanforderungen
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 2/16/2018
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.custom: Strat_SB_Admin
ms.assetid: 790d3e89-2b68-411b-b282-38de5d34dd10
description: Dieses Thema bietet Informationen zu Hardware-, Software- und infrastrukturanforderungen für die Ausführung von Skype für Unternehmen auf einem Mac
ms.openlocfilehash: 1b5fa68a9618126ab69f4ca78f13e65f1ab3ee4b
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="skype-for-business-on-mac-client-requirements"></a>Skype für Unternehmen auf Mac-Clientanforderungen
 
Dieses Thema bietet Informationen zu Hardware-, Software- und infrastrukturanforderungen für die Ausführung von Skype für Unternehmen auf einem Mac
  
Die [Skype für Unternehmen auf dem Mac-Client](https://products.office.com/en-us/skype-for-business/download-app?tab=tabs-3#Mac) ist zum Download zur Verfügung.
  
## <a name="hardware-and-software-requirements-for-skype-for-business-on-the-mac"></a>Hardware- und Softwareanforderungen für Skype for Business auf dem Mac

Die Skype für Unternehmen auf dem Mac-Client erfordert Mac OS X El Capitan und höher und mindestens 100MB freier Speicherplatz verwendet. Die Verwendung aller integrierten Audio- und Videogeräte wird unterstützt. Externe Geräte müssen in der [Liste der qualifizierten Geräte für die Verwendung mit Lync](https://go.microsoft.com/fwlink/p/?LinkId=798223)sein. 
  
> [!NOTE]
> Diese Liste ist vorläufig und einige Geräte möglicherweise für Lync qualifizierte, jedoch nicht unterstützt Skype für Unternehmen unter Mac. > Finden Sie in den [Systemanforderungen](https://products.office.com/en-us/office-system-requirements) für die Mindestanforderungen an die Hardware erforderlich.
  
### <a name="legacy-mac-clients"></a>Mac-Legacyclients

Skype für Business Server 2015 unterstützt die folgenden Clients von Vorversionen auch auf Computern, die ausgeführt werden, Mac OS 10.5.8 oder neuestes Servicepack oder release (Intel-basiert) Betriebssysteme (Mac OS 10.9 Betriebssystem wird derzeit nicht unterstützt). Ausführliche Informationen zu unterstützten Funktionen finden Sie unter [Desktopclient Featurevergleich für Skype für Unternehmen](desktop-feature-comparison.md).
  
- Microsoft Lync für Mac 2011 (siehe [Lync für Mac 2011 – Bereitstellungshandbuch](https://go.microsoft.com/fwlink/p/?LinkId=268786))
    
- Microsoft Communicator für Mac 2011 (siehe [Communicator für Mac 2011 – Bereitstellungshandbuch](https://go.microsoft.com/fwlink/p/?LinkId=268787))
    
## <a name="infrastructure-requirements-for-skype-for-business-on-the-mac"></a>Infrastrukturanforderungen für Skype for Business auf dem Mac
<a name="Infrastructure"> </a>

Die Skype für Unternehmen auf dem Mac-Client nutzt sowohl die Unified Communications-Management-Plattform (UCMP) als auch die Unified Communications Web-API (UCWA), die unsere Mobilität Clients verwenden.
  
Für den Client gelten die gleichen Anforderungen wie bei unseren Mobilitätsclients in der Hinsicht, dass Sie einen Zugriffs-Edgeserver und Reverseproxy in einer unterstützten Konfiguration bereitstellen müssen. Darüber hinaus muss Ihr Konto für Mobilität aktiviert werden.
  
### <a name="authentication"></a>Authentifizierung

Die Skype für Unternehmen auf dem Mac-Client unterstützt die NTLM-Authentifizierung. Darüber hinaus unterstützt der Client moderne Authentifizierung von Microsoft und mehrstufige Authentifizierung, sofern sie bereitgestellt und aktiviert sind.
  
> [!NOTE]
> Aufgrund der aktuellen Beschränkung müssen die Anmeldeinformationen des Benutzers Exchange die ihre Skype Business Anmeldeinformationen für identisch sein. 
  
### <a name="certificates"></a>Zertifikate

Zertifikate, die auf den Zugriffs-Edge-, Reverseproxy- und Front-End-Servern verwendet werden, dürfen nicht den SHA-512-Hashalgorithmus verwenden.
  
Die HTTP-Zertifikatsperrliste muss definiert und für den Client zugänglich sein. Beispielsweise unterstützen nicht wir einen LDAP-Eintrag in das Zertifikat als Ihrer Certificate Revocation List.
  
### <a name="dns"></a>DNS

Mobilität muss auf dem Client Mac ordnungsgemäß funktioniert ordnungsgemäß für die Skype für Unternehmen bereitgestellt werden. Ein typisches Fehlerszenario wäre es, wenn im internen Netzwerk die folgenden beiden DNS-Einträge aufgelöst werden können:
  
- Lyncdiscoverinternal. \<Sipdomain\>
    
- Lyncdiscover. \<Sipdomain\>
    
Weitere Informationen finden Sie unter: [Bereitstellen von Mobilität in Lync Server 2013](https://go.microsoft.com/fwlink/p/?LinkId=798224)und [Microsoft Lync Server 2010-Mobilitätshandbuch](https://go.microsoft.com/fwlink//p/?LinkId=798226).
  
## <a name="see-also"></a>Waren diese Schritte hilfreich? Wenn ja, teilen Sie uns dies bitte unterhalb des Artikels mit. Wenn nicht, schreiben Sie uns, was für Sie unklar war, und wir verwenden Ihr Feedback, um unsere Schritte zu überprüfen.
<a name="Infrastructure"> </a>

#### 

[DNS-Anforderungen für Skype für Business Server 2015](../../plan-your-deployment/network-requirements/dns.md)
#### 

[Häufig gestellte Fragen](https://go.microsoft.com/fwlink/p/?LinkId=798227)
  
[Bekannte Probleme](https://go.microsoft.com/fwlink/p/?LinkId=798228)
