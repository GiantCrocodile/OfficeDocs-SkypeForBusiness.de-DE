---
title: Entfernen der SQL Server-Datenbank für einen Monitoring server
ms.author: kenwith
author: kenwith
manager: serdars
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
description: Nachdem Sie einen Monitoring Server entfernt haben, können Sie die SQL Server-Datenbanken entfernen, die die Server-Daten gehostet. Gehen Sie folgendermaßen vor, um die Definitionen Topologie-Generator zu entfernen, und entfernen Sie die Datenbank- und Protokolldateien Dateien vom Datenbankserver.
ms.openlocfilehash: 85999f1bbb3fc443edcab9d1f1354f26187c6a75
ms.sourcegitcommit: dd37c12a0312270955755ab2826adcfbae813790
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25373357"
---
# <a name="remove-the-sql-server-database-for-a-monitoring-server"></a>Entfernen der SQL Server-Datenbank für einen Monitoring server

Nachdem Sie einen Monitoring Server entfernt haben, können Sie die SQL Server-Datenbanken entfernen, die die Server-Daten gehostet. Gehen Sie folgendermaßen vor, um die Definitionen Topologie-Generator zu entfernen, und entfernen Sie die Datenbank- und Protokolldateien Dateien vom Datenbankserver.
  
## <a name="to-remove-the-sql-server-database-using-topology-builder"></a>Entfernen die SQL Server-Datenbank mithilfe des Topologie-Generators

1. Öffnen Sie auf der Skype für Business Server 2019 Front-End-Server Topologie-Generator.
    
2. Navigieren Sie im Topologie-Generator zu **Freigegebene Komponenten** und klicken Sie dann auf **SQL Server-Speicher**, mit der rechten Maustaste in der SQL Server-Instanz verknüpft ist, zu dem entfernten oder neu konfiguriert Monitoring Server, und klicken Sie dann auf **Löschen**.
    
3. Veröffentlichen Sie die Topologie, und überprüfen Sie dann den Replikationsstatus.
    
## <a name="to-remove-the-database-files-from-the-sql-server"></a>Entfernen Sie die Datenbankdateien vom SQL Server

1. Zum Entfernen der Datenbanken auf dem SQL Server-basierten Server müssen Sie Mitglied der Gruppe der SQL Server-Sysadmins für den SQL Server sein, von dem die Datenbankdateien entfernt werden.
    
2. Öffnen Sie die Skype für Business Server-Verwaltungsshell.
    
3. Geben Sie an der Befehlszeile Folgendes ein:
    
   ```
   Uninstall-CsDataBase -DatabaseType Monitoring -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
   ```

    Wobei _ \<FQDN\> _ wird der vollqualifizierten Domänennamen (FQDN) des Datenbankservers, und _ \<Instanz\> _ ist die optionale benannte Datenbankinstanz. 
    
4. Wenn das Cmdlet **Uninstall-CsDataBase** aufgefordert werden, bestätigen Sie Aktionen, lesen Sie die Informationen, und drücken Sie dann Y (oder EINGABETASTE), um fortzufahren, oder drücken N und dann die EINGABETASTE, wenn Sie das Cmdlet (falls Fehler aufgetreten sind) beenden möchten. 
    
