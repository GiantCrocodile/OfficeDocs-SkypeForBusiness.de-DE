---
title: Planen Sie für hohe Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server in Skype Business Server 2015
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 5/17/2016
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: d9aa622a-95a3-4d8e-8d49-cbfe183f25bf
description: 'Zusammenfassung: Lesen Sie in diesem Thema erfahren, wie für hohe Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server in Skype für Business Server 2015 planen.'
ms.openlocfilehash: 2730d72b47d02772bf2c5c59c819bbe23e8816db
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="plan-for-high-availability-and-disaster-recovery-for-persistent-chat-server-in-skype-for-business-server-2015"></a>Planen Sie für hohe Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server in Skype Business Server 2015
 
**Zusammenfassung:** Lesen Sie in diesem Thema erfahren, wie für hohe Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server in Skype für Business Server 2015 planen.
  
Hohe Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server erfordern zusätzliche Ressourcen über was in der Regel für vollständige Vorgang erforderlich ist. 
  
> [!NOTE]
> Die Verwendung von SQL AlwaysOn-Verfügbarkeitsgruppen wird für Datenbanken des Servers für beständigen Chat nicht unterstützt. 
  
## <a name="resource-requirements"></a>Ressourcenanforderungen

Vor dem Konfigurieren von Persistent Chat Server für hohe Verfügbarkeit und notfallwiederherstellung, stellen Sie sicher, dass Sie die folgenden zusätzlichen Ressourcen verfügen. 
  
- Eine dedizierte Datenbank-Instanz befindet sich im gleichen physischen Rechenzentrum in das sich die Startseite Front-End des Diensts Persistent Chat Server befindet. Diese Datenbank dient als SQL Server-Spiegel für die primäre Datenbank für beständigen Chat. Bestimmen Sie optional einen weiteren SQL Server als den spiegelungszeugen dienen, wenn Sie ein automatisches Failover auf die Spiegeldatenbank möchten.
    
- Eine dedizierte Datenbankinstanz in dem anderen physischen Rechenzentrum. Diese Datenbank dient als SQL Server-Protokollversand sekundäre Datenbank für die Datenbank im primären Rechenzentrum.
    
- Eine dedizierte Datenbank-Instanz, die als SQL Server-Spiegel für die sekundäre Datenbank dient. Optional können festlegen Sie einen weiteren Server SQL Server als den spiegelungszeugen. Beide Instanzen müssen sich im selben physischen Rechenzentrum wie die sekundäre Datenbank befinden.
    
- Wenn Persistent Chat Server-Kompatibilität aktiviert ist, sind eine zusätzliche Instanzen der drei dedizierte Datenbank erforderlich. Die Verteilung ist die gleichen, die zuvor beschriebene für die Datenbank für beständigen Chat. Es ist, zwar möglich für die Kompatibilitätsdatenbank derselben SQL Server-Instanz als Datenbank für beständigen Chat freigeben werden für eigenständige Instanzen für hohe Verfügbarkeit und Disaster Recovery empfohlen.
    
- Eine Dateifreigabe muss erstellt und für die SQL Server-Protokollversand Transaktionsprotokolle festgelegt. Alle SQL Server in beiden Rechenzentren, die beständigen Chat Datenbanken ausführen, benötigen Lese-/Schreibzugriff auf diese Dateifreigabe. Diese Freigabe wird nicht als Teil einer FileStore-Rolle definiert.
    
- Eine Dateifreigabe auf dem sekundären Datenbankserver, die als Zielordner für die SQL Server-Transaktionsprotokolle dient, die von der Dateifreigabe des primären Servers kopiert werden.
    
## <a name="disaster-recovery-and-high-availability-solutions"></a>Lösungen für Notfallwiederherstellung und hohe Verfügbarkeit

Skype für Business Server unterstützt mehrere Unterhaltungsmodi hohe Verfügbarkeit für die Back-End-Server, die einschließlich der datenbankspiegelung. Weitere Informationen finden Sie unter [Planen für hohe Verfügbarkeit und notfallwiederherstellung in Skype für Business Server 2015](../../plan-your-deployment/high-availability-and-disaster-recovery/high-availability-and-disaster-recovery.md). 
  
Die Lösung für die notfallwiederherstellung für Persistent Chat Server in diesem Thema beschriebenen basiert auf einer ausgedehnten Persistent Chat Server Pool. Es ist keine Voraussetzung für eine ausgedehnte virtuelles LAN (VLAN). Durch Strecken einen Persistent Chat Server Pool, Sie einem Pool logisch in der Topologie konfigurieren, aber physisch platzieren Sie die Server im Pool in zwei verschiedenen Rechenzentren. Sie SQL Server-Spiegelung für die Datenbank auf die gleiche Weise konfigurieren und Bereitstellen der Datenbank und die Spiegelung im gleichen Rechenzentrum. Sie müssen eine Sicherungskopie der Datenbank im sekundären Rechenzentrum (mit einer optionalen Spiegelung zur Bereitstellung von hoher Verfügbarkeit während der notfallwiederherstellung) konfigurieren. Dies ist die Sicherungskopie der Datenbank während der notfallwiederherstellung für Failover verwendet. 
  
Ausführliche Informationen zum Konfigurieren von hoher Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server finden Sie unter [Configure hohe Verfügbarkeit und notfallwiederherstellung für Persistent Chat Server in Skype für Business Server 2015](../../deploy/deploy-persistent-chat-server/configure-hadr-for-persistent-chat.md). 
  
In den folgenden Abbildungen wird gezeigt, wie der Persistent Chat Server Pool in zwei pooltopologien konfiguriert werden kann:
  
- Ausgedehnten Persistent Chat Server Pool Rechenzentren mit hoher Bandbreite/niedriger Latenz Geo gespeichert sind.
    
- Ausgedehnten Persistent Chat Server Pool Rechenzentren mit geringer Bandbreite/hoher Wartezeit Geo gespeichert sind.
    
Abbildung 1 zeigt einer gestreckten Persistent Chat Server Pool-Topologie, in dem Rechenzentren sind mit hoher Bandbreite/niedriger Latenz Geo befindet sich. Nehmen Sie für die logischen und physischen Topologien Folgendes an:
  
- Die logische Topologie beinhaltet die folgenden Komponenten:
    
  - Einen Pool für beständigen Chat über die Standorte 1 und 2 hinweg mit den Servern 1 bis einschließlich 8.
    
  - Ein Front-End-Server-Pool, eine Datenbank für beständigen Chat, eine gespiegelte Datenbank, und klicken Sie optional eine Zeugen-Datenbank (nicht im Diagramm dargestellt), die physisch auf Standort 1. 
    
  - Einen zweiten Front-End-Server-Pool und eine Sicherungsdatenbank, die physisch auf Standort 2 liegen.
    
- Die physische Topologie umfasst Websites 1 und 2 wie folgt:
    
  - Einen Pool für beständigen Chat mit den Servern 1 bis einschließlich 4, zwei aktiv und zwei im Leerlauf, an Standort 1.
    
  - Einen Pool für beständigen Chat mit den Servern 5 bis einschließlich 8, zwei aktiv und zwei im Leerlauf, an Standort 2.
    
  - Ein Front-End-Server-Pool, eine Datenbank für beständigen Chat, einer gespiegelten Datenbank und optional eine Zeugen Datenbank (nicht im Diagramm dargestellt) auf Website 1.
    
  - Einen Front-End-Server-Pool und eine Sicherungsdatenbank, die das SQL-Protokollversandziel ist, auf Standort 2.
    
**Ausgedehnten Persistent Chat Server Pool Rechenzentren mit hoher Bandbreite/niedriger Latenz Geo gespeichert sind.**

![Erweiterter Pool für beständigen Chat mit hoher Bandbreite/niedriger Latenz](../../media/55cf3d4b-5f51-4d2f-84ca-b4a13dc5eba3.png)
  
Abbildung 2 zeigt einer ausgedehnten Persistent Chat Server Pool-Topologie, wo Rechenzentren mit geringer Bandbreite/hoher Wartezeit Geo befindet sich befinden.
  
- Die logische Topologie beinhaltet die folgenden Komponenten:
    
  - Einen Pool für beständigen Chat über die Standorte 1 und 2 hinweg mit den Servern 1 bis einschließlich 8.
    
  - Ein Front-End-Server-Pool, eine Datenbank für beständigen Chat, eine gespiegelte Datenbank, und klicken Sie optional eine Zeugen-Datenbank (nicht im Diagramm dargestellt), die physisch auf Standort 1. 
    
  - Einen zweiten Front-End-Server-Pool und eine Sicherungsdatenbank, die physisch auf Standort 2 liegen.
    
- Die physische Topologie umfasst Websites 1 und 2 wie folgt:
    
  - Einen Pool für beständigen Chat mit den Servern 1 bis einschließlich 4, alle aktiv, an Standort 1.
    
  - Einen Pool für beständigen Chat mit den Servern 5 bis einschließlich 8, alle im Leerlauf, an Standort 2.
    
  - Ein Front-End-Server-Pool, eine Datenbank für beständigen Chat, einer gespiegelten Datenbank und optional eine Zeugen Datenbank (nicht im Diagramm dargestellt) auf Website 1.
    
  - Einen Front-End-Server-Pool und eine Sicherungsdatenbank, das SQL-Protokollversandziel ist, an Standort 2.
    
**Ausgedehnten Persistent Chat Server Pool, wenn Rechenzentren mit geringer Bandbreite/hoher Wartezeit Geo gespeichert sind**

![Erweiterter Pool für beständigen Chat mit niedriger Bandbreite/hoher Latenz](../../media/40cbd902-57b8-4d57-a61c-cde4e0bd47f0.png)
  
