---
title: Erstellen der Datenbank
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
ms.date: 3/26/2015
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.tb.PublishTopologyCreateDatabasePage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 4d391619-1cab-4265-ae8a-2519993705bc
description: Der Topologie-Generator bietet eine Möglichkeit zum Installieren von Datenbanken in einem SQL Server Speicher. Wenn Sie Datenbanken mithilfe des Topologie-Generators installieren, liest die Anwendung Informationen aus der Topologie und installiert dann die erforderlichen Datenbanken auf dem angegebenen SQL Server Computer oder SQL Server Cluster. Dies ist die einzige Art von Datenbankinstallation, die bei Verwendung des Topologie-Generators verfügbar ist. Wenn Sie eine bestimmte Datenbank auf einem bestimmten Computer installieren oder eine zusammenhängende Datenbank installieren müssen, müssen Sie stattdessen Windows PowerShell Befehlszeilenschnittstelle und das Cmdlet Install-CsDatabase verwenden.
ms.openlocfilehash: ea7daab44c6075e40e3f8a1b900fe43b84048ed5
ms.sourcegitcommit: c69ab11b701a4833179b8479bc3204dfd4412096
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "48219506"
---
# <a name="create-database"></a>Datenbank erstellen
 
Der Topologie-Generator bietet eine Möglichkeit zum Installieren von Datenbanken in einem SQL Server Speicher. Wenn Sie Datenbanken mithilfe des Topologie-Generators installieren, liest die Anwendung Informationen aus der Topologie und installiert dann die erforderlichen Datenbanken auf dem angegebenen SQL Server Computer oder SQL Server Cluster. Dies ist die einzige Art von Datenbankinstallation, die bei Verwendung des Topologie-Generators verfügbar ist. Wenn Sie eine bestimmte Datenbank auf einem bestimmten Computer installieren oder eine zusammenhängende Datenbank installieren müssen, müssen Sie stattdessen Windows PowerShell Befehlszeilenschnittstelle und das Cmdlet [install-CsDatabase](https://docs.microsoft.com/powershell/module/skype/install-csdatabase?view=skype-ps) verwenden.
  
### <a name="creating-a-database"></a>Erstellen einer Datenbank

1. Klicken Sie auf den Knoten Skype for Business Server 2015, und klicken Sie dann auf **Datenbank installieren**.
    
2. Wählen Sie im Dialogfeld **Datenbanken installieren** auf der Seite **Datenbank erstellen** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des SQL Server Speichers aus, in dem die neuen Datenbanken erstellt werden sollen.
    
3. Klicken Sie auf **Erweitert**. Wählen Sie im Dialogfeld **Speicherort für Datenbankdateien auswählen** eine der folgenden Optionen aus:
    
   - **Speicherort für Datenbankdateien automatisch bestimmen**. Bei Auswahl dieser Option verwendet der Topologie-Generator einen integrierten Algorithmus, um den Speicherort für die Datenbankprotokolle und Datendateien auszuwählen.
    
   - **Standardpfade der SQL Server-Instanz verwenden**. Wenn Sie diese Option auswählen, wird der integrierte Algorithmus nicht verwendet, um die Speicherorte für die Datenbankprotokolle und Datendateien auszuwählen. Stattdessen werden Protokoll-und Datendateien an den Speicherorten gespeichert, die durch den Pfad der SQL Server Standardeinstellungen angegeben werden (diese Pfade müssen von einem SQL Server Administrator in erweitert konfiguriert werden). Datendateien werden im standardmäßigen SQL Server Datendateispeicherort gespeichert, während Protokolldateien am Speicherort der Standard SQL Server Protokolldatei gespeichert werden.
    
4. Klicken Sie auf **OK**.
    
5. Klicken Sie auf der Seite **Datenbank erstellen** auf **Weiter**.
    
6. Klicken Sie auf der Seite **Datenbankerstellung abgeschlossen** auf **Fertig stellen**.
    

