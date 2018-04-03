---
title: Wesentliche Sicherheitsfunktionen in Skype for Business Server 2015
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 2/17/2018
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: bf2a3b8f-73c6-47e1-8c9e-ca1dc1a502bf
description: Skype für Business Server 2015 enthält verschiedene Sicherheitsfunktionen, einschließlich Server-zu-Server-Authentifizierung, rollenbasierte Zugriffssteuerung und zentrale Speicherung von Konfigurationsdaten.
ms.openlocfilehash: 629444f4490022bb9f37f5c67f72f393345ec1a9
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="key-security-features-in-skype-for-business-server-2015"></a>Wesentliche Sicherheitsfunktionen in Skype for Business Server 2015
 
Skype für Business Server 2015 enthält verschiedene Sicherheitsfunktionen, einschließlich Server-zu-Server-Authentifizierung, rollenbasierte Zugriffssteuerung und zentrale Speicherung von Konfigurationsdaten. 
  
Dieser Artikel enthält eine allgemeine Übersicht der Skype Business Server 2015 Sicherheit. 
  
## <a name="key-security-features-in-skype-for-business-server-2015"></a>Wichtige Sicherheitsfeatures in Skype für Business Server 2015

Sicherheit ist ein äußerst umfangreiches Thema. Sicherheit erreicht über alle Features von Skype für Business Server 2015 sowie Datenbanken, Diensten und Hardware, die ein Skype für Business Server Ökosystems bilden. Dieser Artikel beschreibt einige der Features in Skype für Business Server 2015 insbesondere, die für die Sicherheit entwickelt wurden.
  
### <a name="planning-and-design-tools"></a>Planungs- und Entwurfstools

Skype für Business Server 2015 bietet zwei Tools zum Planen und entwerfen zu vereinfachen und das Konfigurieren von Skype falsch für Business Server-Komponenten gering. 
  
- **Planungstool Topologie** automatisiert einen großen den Entwurfsprozess Topologie. Sie können die Ergebnisse aus dem Planungstool zum Topologie-Generator exportieren und das Tool ist, das zum Installieren von jedem Server mit Skype für Business Server 2015 erforderlich ist.
    
- Der **Topologie-Generator** speichert alle Konfigurationsinformationen im zentralen Verwaltungsspeicher.
    
Ausführliche Informationen zu diesen Tools finden Sie unter [Skype für Business Server 2015-Verwaltungstools](../../management-tools/management-tools.md) und [Ihre Skype für Business Server 2015 Bereitstellung planen](../../plan-your-deployment/plan-your-deployment.md).
  
### <a name="central-management-store"></a>Zentraler Verwaltungsspeicher (Central Management Store, CMS)

In Skype für Business Server 2015 ist die Konfigurationsdaten zu Servern und Diensten Teil des zentralen Verwaltungsspeichers. Der zentralen Verwaltungsspeicher bietet eine robuste, Schematisierte Speicherung der Daten zu definieren, einrichten, verwalten, verwalten, beschreiben und Betrieb einer Skype für Business Server-Bereitstellung erforderlich. Darüber hinaus überprüft er die Daten, um eine konsistente Konfiguration zu gewährleisten. Alle Änderungen dieser Konfigurationsdaten erfolgen des zentralen Verwaltungsspeichers, Eliminierung "-synchronisierte" Probleme. 
  
Schreibgeschützte Kopien der Daten werden an alle Server in der Topologie repliziert, Edgeserver und Survivable Branch Appliances eingeschlossen. Die Replikation wird von einem Dienst verwaltet, der standardmäßig unter dem Kontext des Netzwerkdiensts ausgeführt wird, wodurch die Rechte und Berechtigungen auf die eines einfachen Benutzers auf dem Computer reduziert werden. 
  
### <a name="server-to-server-authentication"></a>Server-zu-Server-Authentifizierung

In Skype für Business Server 2015 kann die Authentifizierung zwischen Servern mithilfe des Protokolls Open Authorization (OAuth) konfiguriert werden. Beispielsweise können Sie konfigurieren, Skype für Business Server 2015 zur Authentifizierung mit einem Server, auf dem Microsoft Exchange Server 2016 ausgeführt wird. Das OAuth-Protokoll verwenden, kann die Skype für Business Server und dem Microsoft Exchange Server einander vertrauen. Auf diese Weise können die Produkte nahtlos integriert werden. Weitere Informationen hierzu finden Sie unter [Manage Server-zu-Server-Authentifizierung (OAuth) und partneranwendungen in Skype für Business Server 2015](../../manage/authentication/server-to-server-and-partner-applications.md).
  
### <a name="windows-powershell-based-management-and-web-based-management-interface"></a>Windows PowerShell-basierte und webbasierte Verwaltungsschnittstelle

Skype für Business Server 2015 bietet eine leistungsstarke Verwaltungsschnittstelle, basierend auf der Windows PowerShell-Befehlszeilenschnittstelle. Sie enthält Cmdlets für die Verwaltung der Sicherheit und Windows PowerShell-Sicherheitsfeatures sind standardmäßig aktiviert, sodass Skripts von Nutzern nicht versehentlich oder unwissentlich ausgeführt werden können. Dies bedeutet, dass die Softwarestandardeinstellungen so konfiguriert sind, dass die Sicherheit automatisch optimiert wird und Angriffsmöglichkeiten reduziert werden. Ausführliche Informationen zu Windows PowerShell-Management-Unterstützung in Skype für Business Server 2015 finden Sie unter [Skype für Business Server 2015-Verwaltungsshell](../../manage/management-shell.md). 
  
### <a name="role-based-access-control-rbac"></a>Rollenbasierte Zugriffssteuerung (RBAC)

Skype für Business Server 2015 bietet rollenbasierte Zugriffssteuerung (RBAC), damit Sie Verwaltungsaufgaben delegieren, während gleichzeitig eine hohe Sicherheit gewährleistet bleibt können. Mit der rollenbasierten Zugriffssteuerung können Sie dem Prinzip der geringsten Rechte folgen, bei dem Nutzer nur die administrativen Rechte erhalten, die sie für ihre Arbeit benötigen. Skype für Business Server 2015 bietet die Möglichkeit zum Erstellen einer neuen Rolle und auch die Möglichkeit zum Ändern einer vorhandenen Rolle. 
  
## <a name="network-address-translation-nat"></a>Netzwerkadressenübersetzung (Network Address Translation, NAT)

Skype für Business Server 2015 unterstützt nicht die Verwendung der Netzwerkadressübersetzung (NAT) für die interne Schnittstelle des Edgeservers, aber es unterstützt, platzieren die externe Schnittstelle des Zugriffs-edgedienst, Webkonferenz-edgedienst und A / V-Edgeserver Dienst hinter einem Router oder einer Firewall, die Netzwerkadressübersetzung (NAT) für die einzelnen und skalierte führt konsolidierte Edge-Server-Topologien. Mehrere Edgeserver hinter einem Hardwaregerät zum Lastenausgleich können keine NAT verwenden. Wenn mehrere Edgeserver NAT für die externen Schnittstellen verwenden, ist das Domain Name System (DNS) zum Lastenausgleich erforderlich. Wiederum ermöglicht bei Verwendung des DNS-Lastenausgleich Verringern der Anzahl öffentlicher IP-Adressen pro Edge-Server in einem Edge-Server-Pool. Weitere Informationen hierzu finden Sie unter [Edge-Server-Szenarien in Skype für Business Server 2015](../../plan-your-deployment/edge-server-deployments/scenarios.md).
  
> [!NOTE]
> Wenn Sie mit einem Verbundunternehmen zusammenarbeiten, das über eine Bereitstellung von Microsoft Office Communications Server 2007 verfügt, und wenn Audio-/Videofunktionen zwischen Ihrem Unternehmen und dem Verbundunternehmen unterstützt werden sollen, entsprechen die Portanforderungen denen für die bereitgestellten älteren Edgeserver. Beispielsweise erforderliche die Portbereiche für die ältere Versionen von beiden Unternehmen geöffnet werden müssen, bis der Verbundpartner seinen Edge-Servern zu Skype für Business Server 2015 aktualisiert. Dann können die Portanforderungen erneut überprüft und gemäß der neuen Konfiguration vermindert werden. 
  
## <a name="simplified-certificates-for-edge-servers"></a>Vereinfachte Zertifikate für Edgeserver

Der Bereitstellungs-Assistent kann Antragstellernamen (SNs) und alternative Antragstellernamen (SANs) automatisch ausfüllen. Dadurch reduziert sich das Risiko von unnötigen und potenziell unsicheren Einträgen.
  
## <a name="trustworthy-computing-security-development-lifecycle-sdl"></a>Trustworthy Computing Security Development Lifecycle (SDL)

Skype für Business Server 2015 wurde entwickelt und Übereinstimmung mit den [Microsoft Trustworthy Computing Security Development Lifecycle](https://go.microsoft.com/fwlink/p/?linkid=68761) (SDL) entwickelt.
  
- **Vertrauenswürdiger Aufbau** Der erste Schritt bei der Erstellung sicherer unified Communications-Systems Bestand Bedrohungsmodellen und Testen der einzelnen Features während des Entwurfs. Außerdem führt Microsoft Tests außerhalb des konzipierten Verhaltens durch, um Sicherheitsrisiken zu finden, die sich aus einem nicht erwarteten Produktverhalten ergeben. Viele sicherheitsrelevante Verbesserungen wurden während der Codephase getestet und integriert. Mit Buildzeittools werden Pufferüberläufe und andere potenzielle Sicherheitsbedrohungen erkannt, bevor der Code in das Endprodukt übernommen wird. Natürlich ist es nicht möglich, so zu entwerfen, dass alle unbekannten Sicherheitsbedrohungen beseitigt werden. Es gibt kein System, für das vollständige Sicherheit garantiert werden kann. Da die Produktentwicklung sichere Entwurfsprinzipien von Anfang standardsicherheitstechnologien, beinhaltet Skype für Business Server 2015 branchenüblichen jedoch als grundlegenden Teil seiner Architektur.
    
- **Vertrauenswürdig durch seine Standardeinstellungen** Netzwerkkommunikation in Skype für Business Server 2015 werden standardmäßig verschlüsselt. Da alle Server Zertifikate und Kerberos-Authentifizierung verwenden, einschließlich TLS, Secure Real-Time Transport Protocol (SRTP) und anderen Verschlüsselungstechniken Industriestandard-128-Bit-AES Advanced Encryption Standard () Verschlüsselung, nahezu alle Skype für Geschäftsdaten-Server ist im Netzwerk geschützt. Darüber hinaus ermöglicht rollenbasierte Zugriffssteuerung zum Bereitstellen von Servern mit Skype für Business Server 2015, sodass jede Serverrolle werden nur die Dienste ausgeführt, und verfügt über nur die Berechtigungen im Zusammenhang mit diesen Diensten, die für die Serverrolle geeignet sind.
    
- **Vertrauenswürdig durch die Bereitstellung** Alle Skype Business Server 2015 Dokumentation enthält bewährte Methoden und Empfehlungen zur ermitteln und die optimale Sicherheitsebenen für Ihre Bereitstellung konfigurieren und Bewerten von Sicherheitsrisiken nicht standardmäßigen Optionen aktivieren.
    
