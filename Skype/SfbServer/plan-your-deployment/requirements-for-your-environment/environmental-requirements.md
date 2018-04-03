---
title: Anforderungen an die Umgebung für Skype for Business Server 2015
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 2/15/2018
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Admin
ms.assetid: 4812c444-2546-48d7-9ca7-b71fce508ed8
description: 'Zusammenfassung: Konfigurieren der nicht-Server-Anforderungen für Skype für Business Server 2015. Es gibt verschiedene Dinge, die Sie konfigurierten sollten vor Ihrer Bereitstellung, einschließlich Active Directory, DNS, Zertifikate und Dateifreigaben.'
ms.openlocfilehash: 0d71140678654442caef112f6132695c76d3ea6c
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="environmental-requirements-for-skype-for-business-server-2015"></a>Anforderungen an die Umgebung für Skype for Business Server 2015
 
**Zusammenfassung:** Konfigurieren Sie Ihre nicht-Server-Anforderungen für Skype für Business Server 2015. Es gibt verschiedene Dinge, die Sie konfigurierten sollten vor Ihrer Bereitstellung, einschließlich Active Directory, DNS, Zertifikate und Dateifreigaben.
  
Was ist eine Umwelt Anforderung für Skype für Business Server 2015? Nun, haben wir alles erstellt, die nicht direkt in diesem Thema verknüpft, damit Sie nicht als viel klicken, um Aktionen Server ist. Wenn Sie für Server erforderlichen Komponenten, suchen Sie können die [Anforderungen für Skype für Business Server 2015](server-requirements.md) abstimmen Auschecken ist[Networking Planung](../../plan-your-deployment/network-requirements/network-requirements.md) auch separat dokumentiert. Dies ist anders, was in diesem Artikel haben wir:
  
- [Active Directory](environmental-requirements.md#AD)
  
- [Domain Name System (DNS)](environmental-requirements.md#DNS)
  
- [Zertifikate](environmental-requirements.md#Certs)
  
- [Dateifreigabe](environmental-requirements.md#Fileshare)
  
## <a name="active-directory"></a>Active Directory
<a name="AD"> </a>

Während ein Großteil der Konfigurationsdaten für Server und Dienste in Skype für den zentralen Verwaltungsspeicher von Business Server 2015 gespeichert ist, sind einige Punkte, die noch in Active Directory gespeichert:
  
|**Active Directory-Objekte**|**Objekttypen**|
|:-----|:-----|
|Schemaerweiterungen  <br/> |Benutzerobjekterweiterungen  <br/> |
||Erweiterungen für Lync Server 2013 und Lync Server 2010 zum Aufrechterhalten der Abwärtskompatibilität mit der zuvor unterstützten Versionen.  <br/> |
|Daten  <br/> |Der Benutzer-SIP-URI und andere Einstellungen  <br/> |
||Contact-Objekte für Anwendungen (wie die reaktionsgruppenanwendung und die Anwendung Konferenzzentrale).  <br/> |
||Für die Abwärtskompatibilität veröffentlichte Daten.  <br/> |
||Einen Dienststeuerungspunkt (SCP) für den zentralen Verwaltungsspeicher.  <br/> |
||Das Kerberos-Authentifizierungskonto (ein optionales Computerobjekt).  <br/> |
   
### <a name="os-for-domain-controllers"></a>Betriebssysteme für Domänencontroller

Welches Betriebssystem für Domänencontroller kann verwendet werden? Hier die Liste:
  
- Windows Server 2016
    
- Windows Server 2012 R2
    
- Windows Server 2012
    
- Windows Server 2008 R2
    
- Windows Server 2008
    
Nun müssen die Domänenfunktionsebene von jeder Domäne, die Sie zum Business Server 2015 in Skype bereitstellen und die Gesamtstrukturfunktionsebene von einer beliebigen Gesamtstruktur Ihnen Skype für Business Server 2015 in bereitgestellte eine der folgenden sein:
  
- Windows Server 2016
    
- Windows Server 2012 R2
    
- Windows Server 2012
    
- Windows Server 2008 R2
    
- Windows Server 2008
    
- WindowsServer 2003
    
Dürfen in diesen Umgebungen schreibgeschützte Domänencontroller vorhanden sein? Sicher, solange auch nicht schreibgeschützte Domänencontroller verfügbar sind.
  
Jetzt ist es wichtig zu wissen, dass Skype für Business Server 2015 Domänen mit einfacher Bezeichnung unterstützt. Was ist das? Wenn Sie eine mit der Bezeichnung contoso.local Stammdomäne verfügen, geht, die kein Problem sein. Wenn Sie über eine Stammdomäne, die nur lokale heißt verfügen, nicht dadurch arbeiten, und nicht dementsprechend unterstützt. Weitere wurde zu diesem [in dieser Knowledge Base-Artikel](https://support.microsoft.com/kb/300684/en-us)geschrieben.
  
Skype für Business Server 2015 unterstützt keine auch Umbenennen von Domänen. Wenn Sie wirklich haben dafür, müssen klicken Sie dann Sie So deinstallieren Sie Skype für Business Server 2015, führen Sie die Umbenennung, und Neuinstallieren von Skype für Business Server 2015.
  
Schließlich Sie möglicherweise eine Domäne, in einer gesperrten AD DS-Umgebung zuständig sein, und das ist gut. Wir haben Weitere Informationen zum Bereitstellen von Skype für Business Server 2015 in dieser Art von Umgebung in der Bereitstellung Dokumente.
  
### <a name="ad-topologies"></a>AD-Topologien

Skype für Business Server 2015 unterstützten Topologien sind:
  
- Einzelne Gesamtstruktur mit einzelner Domäne
    
- Einzelne Gesamtstruktur mit einer Struktur und mehreren Domänen
    
- Einzelne Gesamtstruktur mit mehreren Strukturen und nicht zusammenhängenden Namespaces
    
- Mehrere Gesamtstrukturen in einer Topologie mit zentraler Gesamtstruktur
    
- Mehrere Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur
    
- Mehrere Gesamtstrukturen in einer Skype for Business-Ressourcengesamtstruktur-Topologie mit Exchange Online
    
- Mehrere Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur mit Skype for Business Online und Azure Active Directory Connect
    
Wir haben Diagramme und eine Beschreibung können Sie bestimmen, welche Topologie Sie in Ihrer Umgebung oder um benötigen Sie möglicherweise vor der Installation von Skype für Business Server 2015 eingerichtet haben. Wenn Sie um einfach zu halten, sind wir auch einen Schlüssel einschließlich:
  
![Schlüssel zu den Symbolen, die für Skype for Business-Topologiediagramme verwendet werden](../../media/cc0dbc17-cf81-4b79-bf99-4614cc6828a0.png)
  
#### <a name="single-forest-with-single-domain"></a>Einzelne Gesamtstruktur mit einzelner Domäne

![Diagramm einer einzelnen Active-Directory-Gesamtstruktur mit einer einzigen Domäne](../../media/24921a0b-3a3e-4bad-8427-49300e2e3f7a.png)
  
Es nicht einfacher, als dies abrufen, es ist eine Gesamtstruktur mit einer einzelnen Domäne, dies ist eine häufig verwendete Topologie.
  
#### <a name="single-forest-with-a-single-tree-and-multiple-domains"></a>Einzelne Gesamtstruktur mit einer Struktur und mehreren Domänen

![Diagramm mit einer einzigen Gesamtstruktur, einer einzelnen Struktur und mehreren Domänen](../../media/63b9f0dd-6bac-4ba9-ae68-8be032d09dcb.png)
  
Dieses Diagramm zeigt eine einzelne Gesamtstruktur, erneut, besitzt jedoch eine oder mehrere untergeordnete Domänen sowie (stehen drei in diesem Beispiel). Damit die Domäne, der die Benutzer in erstellt werden von der Skype-Domäne unterscheiden kann für Business Server 2015 bereitgestellt wird. Warum sorgen halten Sie davon? Es ist wichtig, die merken, wenn Sie einen Skype für Business Server-Front-End-Pool bereitstellen, müssen alle Server in diesem Pool in einer einzelnen Domäne sein. Sie können die domänenübergreifende Verwaltung über Skype für Business Server Unterstützung von universellen Windows-Administratorgruppen haben.
  
Wieder in der Abbildung sehen Sie sich, dass Benutzer von einer Domäne Skype für Business Server-Pools aus derselben Domäne oder aus verschiedenen Domänen zugreifen können, auch wenn diese Benutzer in einer untergeordneten Domäne befinden.
  
#### <a name="single-forest-with-multiple-trees-and-disjoint-namespaces"></a>Einzelne Gesamtstruktur mit mehreren Strukturen und nicht zusammenhängenden Namespaces

![Diagramm mit einer einzigen Gesamtstruktur, mehreren Strukturen und getrennten Namespaces](../../media/5ede77a1-f5d2-499c-a2c8-d02f3c2f7cd7.png)
  
Es kann sein, dass Sie eine Topologie ähnelt diesem Diagramm haben, in denen Sie über eine Gesamtstruktur, aber in der Gesamtstruktur, mehrere Domänen mit separaten Active Directory-Namespaces. Wenn dies der Fall ist,'s dieses Diagramm ein gutes Beispiel, wie es Benutzer in drei unterschiedlichen Domänen, die Zugriff auf Skype für Business Server 2015 verwendet werden. Einfarbige Linien geben Sie an, dass sie einen Skype für Business Server Pool in ihrer eigenen Domäne zugreifen sind, während eine gestrichelte Linie gibt an, dass der Kunde in einen Pool in einer anderen Struktur vollständig sind.
  
Wie Sie sehen können, können Benutzer derselben Domäne, derselben Struktur, aber auch einer anderen Struktur erfolgreich auf Pools zugreifen.
  
#### <a name="multiple-forests-in-a-central-forest-topology"></a>Mehrere Gesamtstrukturen in einer Topologie mit zentraler Gesamtstruktur

![Diagramm mit mehreren Gesamtstrukturen in einer Topologie mit zentraler Gesamtstruktur](../../media/fec40746-4254-4c84-86b9-aad4a616ea2f.png)
  
Skype für Business Server 2015 unterstützt mehrere Gesamtstrukturen in einer Topologie mit zentraler Gesamtstruktur konfiguriert sind. Wenn Sie nicht sicher sind, was Ihnen ist, verwendet die zentrale Gesamtstruktur in der Topologie Objekte im es zur Darstellung von Benutzern in anderen Gesamtstrukturen und Hosts von Benutzerkonten für alle Benutzer in der Gesamtstruktur an.
  
Wie funktioniert das? Ein verzeichnissynchronisierungsprogramm (wie Forefront Identity Manager oder FIM) verwaltet, Benutzerkonten in der gesamten auf das Vorhandensein eines Unternehmens. Wenn ein Konto erstellt oder in der Gesamtstruktur gelöscht wird, wird diese Änderung im entsprechenden Kontakt in der zentralen Gesamtstruktur synchronisiert.
  
Natürlich ist der Active Directory-Infrastruktur in-Place verschieben für diese Topologie ist möglicherweise nicht einfach, aber wenn Sie bereits vorhanden, oder weiterhin Planung Ihrer Gesamtstruktur Infrastruktur sind, kann dies eine gute Wahl sein. Sie können Ihre Skype für die Bereitstellung in einer einzelnen Gesamtstruktur, Business Server 2015 zentralisieren, während Benutzer kommunizieren, suchen und die Anwesenheit von anderen Benutzern in einer beliebigen Gesamtstruktur anzeigen können. Alle Benutzer, Kontakt Updates werden automatisch mit Synchronisierungssoftware behandelt.
  
#### <a name="multiple-forests-in-a-skype-for-business-resource-forest-topology"></a>Mehrere Gesamtstrukturen in einer Skype for Business-Ressourcengesamtstruktur-Topologie
<a name="BKMK_multipleforestopology"> </a>

![Diagramm mit mehreren Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur](../../media/41efa3b6-d9e6-47df-992b-fefcfc39a80d.png)
  
Eine Topologie mit Ressourcengesamtstruktur wird ebenfalls unterstützt. Es ist, in eine Gesamtstruktur für die Ausführung von Server-Anwendungen wie Microsoft Exchange Server und Skype für Business Server 2015 vorgesehen ist. Diese Ressourcengesamtstrukturen auch hostet, eine synchronisierte Darstellung des aktiven User-Objekte, jedoch keine bei der Anmeldung aktivierten Benutzerkonten. Damit die Ressourcengesamtstruktur eine Umgebung mit gemeinsamen Diensten für die anderen Gesamtstrukturen, ist in dem sich Benutzerobjekte befinden und auf Gesamtstrukturebene Vertrauensstellung mit der Ressourcengesamtstruktur lassen.
  
Beachten Sie, dass Exchange Server in der gleichen Gesamtstruktur als Skype für Business Server oder in einer anderen Gesamtstruktur bereitgestellt werden kann.
  
Um Skype für Business Server 2015 bei dieser Art von Topologie bereitstellen, würden Sie ein deaktiviertes Benutzerobjekt erstellen, in der Ressourcengesamtstruktur für jedes Benutzerkonto in den Benutzergesamtstrukturen (wenn Microsoft Exchange Server bereits in der Umgebung vorhanden ist, kann dies für Sie). Ein verzeichnissynchronisierungstool (wie Forefront Identity Manager oder FIM) benötigen Sie dann Benutzerkonten mit über ihres gesamten Lebenszyklus zu verwalten.
  
#### <a name="multiple-forests-in-a-skype-for-business-resource-forest-topology-with-exchange-online"></a>Mehrere Gesamtstrukturen in einer Skype for Business-Ressourcengesamtstruktur-Topologie mit Exchange Online
<a name="BKMK_multipleforestopology"> </a>

Diese Topologie ähnelt der Topologie, die unter [Mehrere Gesamtstrukturen in einer Skype for Business-Ressourcengesamtstruktur-Topologie](environmental-requirements.md#BKMK_multipleforestopology) beschrieben wird.
  
In dieser Topologie sind eine oder mehrere Benutzergesamtstrukturen und Skype für Business Server in einer dedizierten Ressourcengesamtstruktur bereitgestellt wird. Exchange Server lokal bereitgestellt in der gleichen Gesamtstruktur oder einer anderen Gesamtstruktur werden können und für die hybridbereitstellung mit Exchange Online konfiguriert sind, oder e-Mail-Dienste können ausschließlich von Exchange Online bereitgestellt werden, für die lokalen Konten. Es ist kein Diagramm für diese Topologie verfügbar.
  
#### <a name="multiple-forests-in-a-resource-forest-topology-with-skype-for-business-online-and-azure-active-directory-connect"></a>Mehrere Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur mit Skype for Business Online und Azure Active Directory Connect
<a name="BKMK_multipleforestopology"> </a>

![Zeigt zwei AD-Gesamtstrukturen, eine Benutzergesamtstruktur und eine Ressourcengesamtstruktur an. Die beiden Gesamtstrukturen haben eine Vertrauensstellung und sind mit Office 365 unter Verwendung von Azure AD Connect synchronisiert. Alle Benutzer sind für Skype for Business über Office 365 aktiviert.](../../media/6d54558d-8786-4ebf-90f6-55ae3fdb5ae7.jpg)
  
Bei diesem Szenario sind mehrere lokale Gesamtstrukturen mit einer Topologie mit Ressourcengesamtstruktur vorhanden. Zwischen den Active Directory-Gesamtstrukturen besteht eine vollständige Vertrauensstellung. Das Tool „Azure Active Directory Connect“ wird zur Synchronisierung von Konten zwischen den lokalen Benutzergesamtstrukturen und Office 365 verwendet.
  
 Die Organisation auch Office 365 und [Azure Active Directory verbinden](https://go.microsoft.com/fwlink/p/?LinkId=614836) ihrer lokalen Konten mit Office 365 synchronisiert. Für Skype für Unternehmen aktivierte Benutzer werden über Office 365 und Skype für Business Online aktiviert. Skype für Business Server ist nicht lokal bereitgestellt.
  
Authentifizierung für einmaliges Anmelden wird von einer Active Directory Federation Services-Farm befindet sich in der benutzergesamtstruktur bereitgestellt.
  
In diesem Szenario wird es zum Bereitstellen von Exchange lokal, Exchange Online eine hybride Exchange-Lösung oder nicht in allen Bereitstellung von Exchange werden unterstützt. (Das Diagramm zeigt nur lokale Exchange-Organisation, aber die anderen Exchange-Lösungen sind auch vollständig unterstützt.)
  
#### <a name="multiple-forests-in-a-resource-forest-topology-with-hybrid-skype-for-business"></a>Mehrere Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur mit Skype for Business-Hybridbereitstellung
<a name="BKMK_multipleforestopology"> </a>

In diesem Szenario vorhanden sind oder mehr lokalen Benutzergesamtstrukturen und Skype für Unternehmen in einer dedizierten Ressourcengesamtstruktur bereitgestellt wird und mit Skype für Hybridmodus für Business Online konfiguriert. Exchange Server lokal bereitgestellt in der gleichen Gesamtstruktur oder einer anderen Gesamtstruktur werden können und für die hybridbereitstellung mit Exchange Online konfiguriert werden kann. Alternativ können e-Mail-Dienste für die lokalen Konten ausschließlich von Exchange Online bereitgestellt werden.
  
Weitere Informationen finden Sie unter [Konfigurieren einer Umgebung mit mehreren Gesamtstrukturen für hybride Skype für Unternehmen](../../skype-for-business-hybrid-solutions/deploy-hybrid-connectivity/configure-a-multi-forest-environment-for-hybrid.md).
  
## <a name="domain-name-system-dns"></a>DNS (Domain Name System)
<a name="DNS"> </a>

Skype für Business Server 2015 erfordert DNS, aus den folgenden Gründen:
  
- DNS ermöglicht Skype für Business Server 2015 erkennen interner Server oder Pools, für die Server-zu-Server-Kommunikation ermöglicht.
    
- DNS ermöglicht Computern ermitteln können, die Front-End-Pool oder Standard Edition-Server für die SIP-Transaktionen verwendet wird.
    
- Es ordnet einfache URLs für Konferenzen den Servern zu, auf denen diese Konferenzen gehostet werden.
    
- DNS ermöglicht externen Benutzern und Clientcomputern Verbindung mit Ihrer Edge-Server oder dem HTTP-Reverseproxy für instant messaging (IM) oder für Konferenzen.
    
- Sie können die unified Communications (UC) Geräte, die in protokolliert werden nicht erkennen, den Front-End-Pool oder Standard Edition-Server mit der geräteaktualisierungswebdienst zum Abrufen von Updates und Protokolle senden können.
    
- Die Verwendung von DNS ermöglicht mobilen Clients die automatische Ermittlung von Webdienstressourcen, ohne dass Benutzer in den Geräteeinstellungen manuell URLs eingeben müssen.
    
- Außerdem wird es im DNS-Lastenausgleich verwendet.
    
Es ist wichtig, beachten Sie, dass Skype für Business Server 2015 internationalisierten Domänennamen (IDNs) nicht unterstützt.
  
Und es ist sehr wichtig, denken Sie daran, dass ein Name im DNS identisch mit den Namen des Computers, auf einem beliebigen Server für Business Server 2015 von Skype verwendeten konfiguriert werden. Insbesondere wir keinen Short-Namen in der Umgebung, und die FQDNs für Topologie-Generator.
  
Dies scheint, als wäre es logische für jeden Computer, der bereits Mitglied einer Domäne, doch wenn Sie einen Edge-Server, der nicht an Ihre Domäne verbunden ist verfügen, es kann Standardwert einen kurzen Namen, wobei keine Domänensuffix. Stellen Sie sicher, dass dies nicht der Fall, in DNS oder auf dem Edge-Server oder eine beliebige Skype für Business Server 2015 Server oder Pool, darum geht ist.
  
Und definitiv nicht verwenden, Unicode-Zeichen oder Unterstriche. Standard Zeichen (A – Z, a – Z, 0-9 und Bindestriche) entsprechen denen, die von externen DNS- und öffentlichen Zertifizierungsstellen unterstützt werden (Sie müssen dem SN im Zertifikat FQDNs zuweisen vergessen Sie nicht), sodass Sie sich selbst viel Kummer Wenn Ersatzteile werden Benennen Sie dabei beachten.
  
Weitere Informationen zu den DNS-Anforderungen für Networking entnehmen Sie dem Abschnitt [Networking](../../plan-your-deployment/network-requirements/network-requirements.md) unserer Planungsdokumentation.
  
## <a name="certificates"></a>Zertifikate
<a name="Certs"> </a>

Stellen Sie vor der Bereitstellung unbedingt sicher, dass Ihre Zertifikate in Ordnung sind. Skype für Business Server 2015 benötigt eine public Key-Infrastruktur (PKI) für den Transport layer Security (TLS) und mutual Transport Layer Security (MTLS) Verbindungen. Im Grunde verwendet Skype für Business Server sicher in eine standardisierte Methode für die Kommunikation von Zertifizierungsstellen (CAs) ausgestellte Zertifikate.
  
Dies sind einige Aspekte, die für Business Server 2015 Skype-Zertifikaten für verwendet:
  
- TLS-Verbindungen zwischen Client und Server
    
- MTLS-Verbindungen zwischen Servern
    
- Partnerverbund mit automatischer DNS-Ermittlung von Partnern
    
- Zugriff von Remotebenutzern auf Sofortnachrichten
    
- Zugriff externer Benutzer auf AV-Sitzungen, Anwendungsfreigabe und Konferenzen
    
- Kommunizieren mit dem Webanwendungen und Outlook Web Access (OWA)
    
Zertifikatsplanung's also ein muss. Nun, sehen wir uns eine Liste der einige Aufgaben Sie beim Anfordern von Zertifikaten bedenken müssen:
  
- Alle Serverzertifikate müssen die Serverautorisierung (Enhanced Key Usage [EKU], erweiterte Schlüsselverwendung für Server) unterstützen.
    
- Alle Serverzertifikate müssen einen Zertifikatsperrlisten-Verteilungspunkt unterstützen.
    
- Alle Zertifikate müssen mithilfe eines Signaturalgorithmus signiert werden, der vom Betriebssystem unterstützt wird. Skype für Business Server 2015 unterstützt die SHA-1 und SHA-2-Programmsuite Digest (224, 256, 384 und 512-Bit), wird die Größe und erfüllt oder überschreitet die betriebssystemanforderungen.
    
- Die automatische Registrierung wird für interne Server mit Skype für Business Server 2015 unterstützt.
    
- Die automatische Registrierung wird für Skype für Business Server 2015 Edge-Server nicht unterstützt.
    
- Wenn Sie eine webbasierte zertifikatanforderung an eine Windows Server 2003-Zertifizierungsstelle übermitteln, müssen Sie diese von einem Computer mit entweder Windows Server 2003 mit SP2 oder Windows XP einreichen.
    
> [!NOTE]
> Obwohl mit Update KB922706 Probleme beim Registrieren von Webzertifikaten für eine Windows Server 2003-Zertifikatdienste-Webregistrierung behoben werden können, ist es mit diesem Update nicht möglich, unter Windows Server 2008, Windows Vista oder Windows 7 ein Zertifikat bei einer Windows Server 2003-Zertifizierungsstelle anzufordern. 
  
> [!NOTE]
> Die Verwendung des Signaturalgorithmus RSASSA-PSS wird nicht unterstützt und kann unter anderem zu Fehlern bei der Anmeldung und Problemen mit der Anrufweiterleitung führen.  
  
- Es werden Verschlüsselungsschlüssellängen von 1.024, 2.048 und 4.096 Bit unterstützt. Empfohlen werden Schlüssellängen ab 2.048 Bit.
    
- Der standardmäßige Digest- bzw. Hashsignaturalgorithmus ist RSA. Die Algorithmen ECDH_P256, ECDH_P384 und ECDH_P521 werden ebenfalls unterstützt.
    
Das ist also eine Menge überlegen und definitiv, eine Vielzahl von Komfort Ebenen mit Anfordern von Zertifikaten von einer Zertifizierungsstelle vorhanden ist. Wir geben Sie einige weitere Leitlinien unten um Ihrer Planung so einfach wie möglich zu machen.
  
### <a name="certificates-for-your-internal-servers"></a>Zertifikate für Ihre internen Server

Sie benötigen Zertifikate für die meisten der von internen Servern und in den meisten Fällen erhalten Sie diese von einer internen Zertifizierungsstelle (, die ein befindet sich in Ihrer Domäne ist). Wahlweise können Sie diese Zertifikate von einer externen Zertifizierungsstelle (aus dem Internet) erhalten. Wenn Sie, welche öffentlichen Zertifizierungsstelle wissen möchten sollte navigieren Sie zu, Sie können die [Unified Communications-Partner Zertifikats](https://support.microsoft.com/kb/929395/en-us) Liste Auschecken.
  
Sie nun auch Zertifikate benötigen, wenn Skype für Business Server 2015 mit anderen Anwendungen und Server, wie beispielsweise Microsoft Exchange Server kommuniziert. Dies muss offensichtlich ein Zertifikat sein, das von den anderen Anwendungen und Servern unterstützt wird. Skype für Business Server 2015 und andere Microsoft-Produkte unterstützen das Protokoll Open Authorization (OAuth) für Server-zu-Server-Authentifizierung und Autorisierung. Wenn Sie dies interessiert sind, haben wir eine zusätzliche Planungsartikel für OAuth und Skype für Business Server 2015.
  
Skype für Business Server 2015 umfasst auch Unterstützung für (ohne) mithilfe der kryptografischen Hash-Funktion SHA-256 signierte Zertifikate. Um den externen Zugriff mithilfe von SHA-256 zu unterstützen, muss das externe Zertifikat von einer öffentlichen Zertifizierungsstelle unter Verwendung von SHA-256 ausgestellt werden.
  
Um testen und Dinge recht einfach, haben wir die Anforderungen an Zertifikate für Standard Edition-Server, Front-End-Pools und andere Rollen in den folgenden Tabellen mit speichern die fiktive "contoso.com" verwendeten Beispiele (Sie wahrscheinlich etwas verwenden für Ihre Umgebung Else). Dies sind alle standard-Web-Serverzertifikate mit privaten Schlüsseln, die nicht exportiert werden können. Zusätzliche beachtet werden:
  
- Die erweiterte Schlüsselverwendung (Enhanced Key Usage, EKU) für Server wird automatisch konfiguriert, wenn Sie den Zertifikat-Assistenten zum Anfordern von Zertifikaten verwenden.
    
- Der Anzeigename jedes Zertifikats muss im Computerspeicher eindeutig sein.
    
- Gemäß den Anweisungen in den Beispielnamen unten Wenn Sie sipinternal.contoso.com oder sipexternal.contoso.com in Ihrem DNS konfiguriert haben müssen sie auf das Zertifikat Subject Alternative Name (SAN) hinzugefügt werden.
    
Zertifikate für Standard Edition-Server:
  
|**Zertifikat**|**Name/gemeinsamen Antragstellername**|**Alternativer Antragstellername**|**Beispiel**|**Anmerkungen**|
|:-----|:-----|:-----|:-----|:-----|
|Standard  <br/> |FQDN des Pools  <br/> |FQDN des Pools und FQDN des Servers  <br/> Wenn mehrere SIP-Domänen vorhanden sind und die automatische Clientkonfiguration aktiviert wurde, erkennt der Zertifikat-Assistent die unterstützten FQDNs für SIP-Domänen und fügt diese hinzu.  <br/> Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich (Domain Name System) festgelegt ist, benötigen Sie auch Einträge für „sip.sipDomäne“ (für jede vorhandene SIP-Domäne).  <br/> |Sn=se01.contoso.com; SAN=se01.contoso.com  <br/> Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich festgelegt ist, benötigen Sie auch „SAN=sip.contoso.com; SAN=sip.fabrikam.com“.  <br/> |Auf Standard Edition-Server Standard Edition-Server ist der FQDN des Servers identisch mit den vollqualifizierten Domänennamen des Pools.  <br/> Der Assistent erkennt alle SIP-Domänen, die Sie während der Installation angegeben haben, und fügt sie automatisch zum alternativen Antragstellernamen (SAN) hinzu.  <br/> Sie können dieses Zertifikat auch für die Server-zu-Server-Authentifizierung verwenden.  <br/> |
|Web, intern  <br/> |FQDN des Servers  <br/> |Jeder der folgenden:  <br/> • Interne Web-FQDN (Dies entspricht dem FQDN des Servers ist)  <br/> UND  <br/> • Meet einfache URLs  <br/> • DFÜ-einfache URL  <br/> • Einfache Admin-URL  <br/> ODER  <br/> • Ein Platzhaltereintrag für einfache URLs  <br/> |Sn=se01.contoso.com; SAN=se01.contoso.com; SAN=Meet.contoso.com; SAN=Meet.Fabrikam.com; SAN=Dialin.contoso.com; SAN=Admin.contoso.com  <br/> Mit einem Platzhalterzertifikat:  <br/> Sn=se01.contoso.com; SAN=se01.contoso.com; SAN =\*. "contoso.com"  <br/> |Das interne Web-FQDN im Topologie-Generator kann nicht überschrieben werden.  <br/> Wenn Sie über mehrere einfache Besprechungs-URLs verfügen, müssen Sie alle als alternative Antragstellernamen einbeziehen.  <br/> Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.  <br/> |
|Web, extern  <br/> |FQDN des Servers  <br/> |Jeder der folgenden:  <br/> • Externen Web-FQDN  <br/> UND  <br/> • DFÜ-einfache URL  <br/> • Meet einfache URLs pro SIP-Domäne  <br/> ODER  <br/> • Ein Platzhaltereintrag für einfache URLs  <br/> |Sn=se01.contoso.com; SAN=webcon01.contoso.com; SAN=Meet.contoso.com; SAN=Meet.Fabrikam.com; SAN=Dialin.contoso.com  <br/> Mit einem Platzhalterzertifikat:  <br/> Sn=se01.contoso.com; SAN=webcon01.contoso.com; SAN =\*. "contoso.com"  <br/> |Wenn Sie mehrere einfache Meet-URLs haben, haben Sie alle als alternative Antragstellernamen enthalten.  <br/> Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.  <br/> |
   
Zertifikate für Front-End-Server in einem Front-End-Pool:
  
|**Zertifikat**|**Name/gemeinsamen Antragstellername**|**Alternativer Antragstellername**|**Beispiel**|**Anmerkungen**|
|:-----|:-----|:-----|:-----|:-----|
|Standard  <br/> |FQDN des Pools  <br/> |FQDN des Pools und FQDN des Servers  <br/> Wenn mehrere SIP-Domänen vorhanden sind und die automatische Clientkonfiguration aktiviert wurde, erkennt der Zertifikat-Assistent die unterstützten FQDNs für SIP-Domänen und fügt diese hinzu.  <br/> Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich (Domain Name System) festgelegt ist, benötigen Sie auch Einträge für „sip.sipDomäne“ (für jede vorhandene SIP-Domäne).  <br/> |Sn=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com  <br/> Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich festgelegt ist, benötigen Sie auch „SAN=sip.contoso.com; SAN=sip.fabrikam.com“.  <br/> |Der Assistent erkennt alle SIP-Domänen, die Sie während der Installation angegeben haben, und fügt sie automatisch zum alternativen Antragstellernamen (SAN) hinzu.  <br/> Sie können dieses Zertifikat auch für die Server-zu-Server-Authentifizierung verwenden.  <br/> |
|Web, intern  <br/> |FQDN des Pools  <br/> |Jeder der folgenden:  <br/> • Interne Web-FQDN (der nicht identisch mit den FQDN des Servers ist)  <br/> • FQDN des Servers  <br/> • Skype für Business Pool-FQDN  <br/> UND  <br/> • Meet einfache URLs  <br/> • DFÜ-einfache URL  <br/> • Einfache Admin-URL  <br/> ODER  <br/> • Ein Platzhaltereintrag für einfache URLs  <br/> |Sn=ee01.contoso.com; SAN=ee01.contoso.com; SAN=Meet.contoso.com; SAN=Meet.Fabrikam.com; SAN=Dialin.contoso.com; SAN=Admin.contoso.com  <br/> Mit einem Platzhalterzertifikat:  <br/> Sn=ee01.contoso.com; SAN=ee01.contoso.com; SAN =\*. "contoso.com"  <br/> |Wenn Sie mehrere einfache Meet-URLs haben, haben Sie alle als alternative Antragstellernamen enthalten.  <br/> Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.  <br/> |
|Web, extern  <br/> |FQDN des Pools  <br/> |Jeder der folgenden:  <br/> • Externen Web-FQDN  <br/> UND  <br/> • DFÜ-einfache URL  <br/> • Einfache Admin-URL  <br/> ODER  <br/> • Ein Platzhaltereintrag für einfache URLs  <br/> |Sn=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=Meet.contoso.com; SAN=Meet.Fabrikam.com; SAN=Dialin.contoso.com  <br/> Mit einem Platzhalterzertifikat:  <br/> Sn=ee01.contoso.com; SAN=webcon01.contoso.com; SAN =\*. "contoso.com"  <br/> |Wenn Sie mehrere einfache Meet-URLs haben, haben Sie alle als alternative Antragstellernamen enthalten.  <br/> Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.  <br/> |
   
Zertifikate für den Director:
  
|**Zertifikat**|**Name/gemeinsamen Antragstellername**|**Alternativer Antragstellername**|**Beispiel**|
|:-----|:-----|:-----|:-----|
|Standard  <br/> |Directorpool  <br/> |FQDN des Directors, des FQDN des Director-Pools.  <br/> Wenn dieser Pool der Server für die automatische Anmeldung für Clients ist und exakte DNS-Abgleich der in den Gruppenrichtlinien, benötigen Sie auch den Einträge für sip.sipdomain (für jede SIP-Domäne).  <br/> |Pool.contoso.com; SAN=dir01.contoso.com  <br/> Wenn dieser Director-Pool der Server für die automatische Anmeldung für Clients ist und exakte DNS-Abgleich in den Gruppenrichtlinien erforderlich ist, benötigen Sie auch festgelegt; SAN=SIP.Fabrikam.com  <br/> |
|Web, intern  <br/> |FQDN des Servers  <br/> |Jeder der folgenden:  <br/> • Interne Web-FQDN (Dies entspricht dem FQDN des Servers ist)  <br/> • FQDN des Servers  <br/> • Skype für Business Pool-FQDN  <br/> UND  <br/> • Meet einfache URLs  <br/> • DFÜ-einfache URL  <br/> • Einfache Admin-URL  <br/> ODER  <br/> • Ein Platzhaltereintrag für einfache URLs  <br/> |Sn=dir01.contoso.com; SAN=dir01.contoso.com; SAN=Meet.contoso.com; SAN=Meet.Fabrikam.com; SAN=Dialin.contoso.com; SAN=Admin.contoso.com  <br/> Mit einem Platzhalterzertifikat:  <br/> Sn=dir01.contoso.com; SAN=dir01.contoso.com SAN =\*. "contoso.com"  <br/> |
|Web, extern  <br/> |FQDN des Servers  <br/> |Jeder der folgenden:  <br/> • Externen Web-FQDN  <br/> UND  <br/> • Meet einfache URLs pro SIP-Domäne  <br/> • DFÜ-einfache URL  <br/> ODER  <br/> • Ein Platzhaltereintrag für einfache URLs  <br/> |Director externe Web-FQDN muss sich von den Front-End-Pool oder Front-End-Server unterscheiden.  <br/> Sn=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=Meet.Fabrikam.com; SAN=Dialin.contoso.com  <br/> Mit einem Platzhalterzertifikat:  <br/> Sn=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN =\*. "contoso.com"  <br/> |
   
Zertifikate für eigenständige Vermittlungsserver:
  
|**Zertifikat**|**Name/gemeinsamen Antragstellername**|**Alternativer Antragstellername**|**Beispiel**|
|:-----|:-----|:-----|:-----|
|Standard  <br/> |FQDN des Pools  <br/> |FQDN des Pools  <br/> FQDN des Poolmitgliedsservers  <br/> |SN = Medsvr-pool.contoso.net; SAN = Medsvr-pool.contoso.net; SAN=medsvr01.contoso .net  <br/> |
   
Zertifikate für Survivable Branch Appliance:
  
|**Zertifikat**|**Name/gemeinsamen Antragstellername**|**Alternativer Antragstellername**|**Beispiel**|
|:-----|:-----|:-----|:-----|
|Standard  <br/> |FQDN der Anwendung  <br/> |SIP. \<Sipdomain\> (Sie benötigen nur ein Eintrag pro SIP-Domäne)  <br/> |Sn=sba01.contoso .net; Festgelegt; SAN=SIP.Fabrikam.com  <br/> |
   
### <a name="certificates-for-your-persistent-chat-server"></a>Zertifikate für Ihren Server für beständigen Chat

Wenn Sie Ihre Persistent Chat Server zu installieren, können Sie ihm ein Zertifikat erforderlich, das das von derselben Zertifizierungsstelle, die von Ihrer Skype für interne Server Business Server 2015 verwendet ausgestellt wurde. Dies soll für jeden Server mit der Persistent Chat-Webdienste für das Hoch-/Herunterladen ausgeführt werden. Es wird dringend empfohlen, Sie die erforderlichen Zertifikate haben, bevor Sie Ihre Installation beständigen Chat beginnen, und wenn die Zertifizierungsstelle extern ist, sogar noch dies der Fall ist (diese Aspekte können dauern etwas Zeit, um ausgestellt werden).
  
### <a name="certificates-for-external-user-access-edge"></a>Zertifikate für den Zugriff externer Benutzer (Edge)

Skype für Business Server 2015 unterstützt die Verwendung von ein **einzelnes öffentliches Zertifikat** für Zugriff und Konferenzen externe edgeschnittstellen plus der A / V-Authentifizierungsdienst, die alle über die Edgeserver bereitgestellt wird. Die interne Schnittstelle des Edgeservers wird in der Regel verwenden Sie ein privates Zertifikat von Ihrem internen Zertifizierungsstelle ausgestellt, aber wenn Sie es vorziehen, können ein öffentliches Zertifikat für diese ebenfalls, wenn sie von einer vertrauenswürdigen Zertifizierungsstelle stammt.
  
Ihr Reverseproxy (RP) wird ebenfalls ein öffentliches Zertifikat verwenden und es verschlüsselt die Kommunikation zwischen Ihrem Reverseproxy und den Clients sowie zwischen dem Reverseproxy und den internen Servern mithilfe von HTTP (oder präziser: TLS über HTTP).
  
### <a name="certificates-for-mobility"></a>Zertifikate für Mobilität

Wenn Sie Mobilität bereitstellen, und Sie sind automatische Ermittlung für mobile Clients unterstützen, können Sie ihm müssen einige zusätzliche Subject alternative Namenseinträge Zertifikate die sichere Verbindung von mobilen Clients zu unterstützen.
  
Welche Zertifikate? Sie benötigen alternative Antragstellernamen für die automatische Erkennung auf Zertifikaten:
  
- Directorpool
    
- Front-End-Pool
    
- Reverseproxy
    
Die Besonderheiten sind in allen Tabellen unten aufgelistet.
  
Dies ist nun, wobei vorab etwas Planung ist gut, aber manchmal Sie Skype für Business Server 2015 ohne zum Bereitstellen von Mobilität bereitgestellt haben und, die erscheint, um die Zeile nach unten Wenn Sie Zertifikate bereits in Ihrer Umgebung haben. Neu sie über eine interne Zertifizierungsstelle ausgestellt wird in der Regel recht einfach, aber mit öffentliche Zertifikate von einer öffentlichen Zertifizierungsstelle, sind, die ein wenig mehr pricy.
  
Ist, die sich ansehen und viele SIP-Domänen vorhanden sind (die stellen würde hinzufügen teurer SANS), können Sie konfigurieren Ihren Reverseproxy aufrufen, um HTTP für die erste Autodiscover Service-Anforderung, anstatt über HTTPS (Dies ist die Standardeinstellung verwenden Konfiguration). Im Abschnitt „Planen der Mobilität“ finden Sie ausführlichere Informationen dazu.
  
Director-Pool und Front-End-Pool-Zertifikats Anforderungen:
  
|**Beschreibung**|**SAN-Eintrag**|
|:-----|:-----|
|Interne URL des AutoErmittlungsdiensts  <br/> |SAN = Lyncdiscoverinternal. \<Sipdomain\>  <br/> |
|URL des externen AutoErmittlungsdiensts  <br/> |SAN = Lyncdiscover. \<Sipdomain\>  <br/> |
   
Alternativ können Sie SAN =\*. \<Sipdomain\>
  
Reverseproxy-Zertifikatsanforderungen (öffentliche ZS):
  
|**Beschreibung**|**SAN-Eintrag**|
|:-----|:-----|
|URL des externen AutoErmittlungsdiensts  <br/> |SAN = Lyncdiscover. \<Sipdomain\>  <br/> |
   
Dieser SAN muss dem Zertifikat zugewiesen werden, das dem SSL-Listener (Secure Sockets Layer) auf dem Reverseproxy zugewiesen ist.
  
> [!NOTE]
> Der Reverseproxy Listener Wechsel zu SANs für Ihre externe Web Services URL(s) verfügen. Beispiele umfassen SAN=skypewebextpool01.contoso.com und dirwebexternal.contoso.com, wenn Sie den Director bereitgestellt haben (dies optional ist). 
  
## <a name="file-share"></a>Dateifreigabe
<a name="Fileshare"> </a>

Skype für Business Server 2015 kann die gleiche Dateifreigabe für alle Dateispeicher zu verwenden. Beachten Sie bitte Folgendes:
  
- Eine Dateifreigabe muss sich entweder auf DAS (Direct Attached Storage) oder auf einem SAN (Storage Area Network) befinden, einschließlich des DFS (Distributed File System) sowie von RAID-Komponenten (Redundant Array of Independent Disks) für Dateispeicher. Für Weitere DFS für Windows Server 2012 lesen, sollten checken Sie [Diese Seite DFS aus](https://technet.microsoft.com/en-us/library/jj127250.aspx).
    
- Es wird empfohlen, einen freigegebenen Cluster für die Dateifreigabe. Wenn Sie eine verwenden, sollten Sie Windows Server 2012 oder Windows Server 2012 R2 Cluster bilden. Windows Server 2008 R2 ist ebenfalls zulässig. Warum die neuesten Windows? Ältere Versionen möglicherweise nicht die richtigen Berechtigungen für alle Features zu aktivieren. Sie können Clusterverwaltung verwenden, um die Dateifreigaben erstellen, und dieser [Erstellen eines Clusters](https://support.microsoft.com/kb/284838) KB-Artikel helfen Ihnen mit diesen Details.
    
> [!CAUTION]
> Beachten Sie, dass Network Attached Storage (NAS) als Dateifreigabe nicht unterstützt wird. Verwenden Sie daher eine der oben genannten Optionen. 
  
