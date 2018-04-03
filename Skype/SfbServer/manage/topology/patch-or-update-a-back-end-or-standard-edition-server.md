---
title: Patchen oder Aktualisieren eines Back-End-Servers oder Standard Edition-Servers in Skype for Business Server 2015
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: f95f8d3a-e039-484e-97bd-d727db21a12b
description: 'Zusammenfassung: Erfahren Sie, wie Sie ein Update oder Patch auf eine Back-End-Server in Skype für Business Server installieren.'
ms.openlocfilehash: 14acff1aea501bf47dff95053259187570d2f990
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="patch-or-update-a-back-end-server-or-standard-edition-server-in-skype-for-business-server-2015"></a>Patchen oder Aktualisieren eines Back-End-Servers oder Standard Edition-Servers in Skype for Business Server 2015
 
**Zusammenfassung:** Hier erfahren Sie, wie Sie ein Update oder Patch auf eine Back-End-Server in Skype für Business Server installieren.
  
In diesem Thema wird erläutert, wie Sie ein Update auf einen Enterprise Edition Back-End-Server oder Standard Edition-Server installieren.
  
Wenn eine Back-End-Server nach unten für mindestens 30 Minuten ist während der Aktualisierung werden, können Benutzer dann in ausfallsicherheitsmodus gehen. Wenn die Aktualisierung abgeschlossen ist und die Back-End-Server erneut mit den Front-End-Servern im Pool verbunden ist, werden Benutzer an voller Funktionsumfang zurückgegeben. Wenn das Upgrade weniger als 30 Minuten dauert, sind die Benutzer davon nicht betroffen.
  
### <a name="to-update-a-back-end-server-or-standard-edition-server"></a>Back-End-Server oder Standard Edition-Server aktualisieren

1. Melden Sie sich am Server, für den Sie das Upgrade vornehmen, als Mitglied der Rolle CsAdministrator an.
    
2. Laden Sie das Update herunter und extrahieren Sie es auf die lokale Festplatte.
    
3. Starten Sie die Skype für Business Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Skype für Business 2015**und klicken Sie dann auf **Skype für Business Server-Verwaltungsshell**.
    
4. Skype für Business Server-Dienste zu beenden. Geben Sie in der Befehlszeile Folgendes ein:
    
    ```
    Stop-CsWindowsService
    ```

5. Beenden Sie den WWW-Dienst (World Wide Web). Geben Sie in der Befehlszeile Folgendes ein:
    
    ```
    net stop w3svc
   ```

6. Schließen Sie alle Skype für Windows Business Server-Verwaltungsshell.
    
7. Installieren Sie das Update.
    
8. Starten Sie die Skype für Business Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Skype für Business 2015**und klicken Sie dann auf **Skype für Business Server-Verwaltungsshell**.
    
9. Skype für Business Server-Dienste erneut aus, um die globalen Assemblycache (GAC) – d Assemblys catch zu beenden. Geben Sie in der Befehlszeile Folgendes ein:
    
    ```
    Stop-CsWindowsService
    ```

10. Starten Sie den WWW-Dienst neu. Geben Sie in der Befehlszeile Folgendes ein:
    
    ```
    net start w3svc
    ```

11. Übernehmen Sie die vorgenommenen Änderungen für die SQL Server-Datenbanken, indem Sie einen der folgenden Schritte ausführen:
    
    - Wenn hierbei handelt es sich um einen Enterprise Edition Back-End-Server und keine verbundenen Datenbanken auf diesem Server, wie die Archivierung oder Überwachung Datenbanken vorhanden sind, geben Sie Folgendes an der Befehlszeile ein:
    
    ```
    Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>
    ```

    - Wenn hierbei handelt es sich um einen Enterprise Edition Back-End-Server und auf diesem Server gemeinsam ausgeführte Datenbanken vorhanden sind, geben Sie Folgendes an der Befehlszeile ein:
    
    ```
    Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>  -ExcludeCollocatedStores
    ```

    - Ist dies ein Standard Edition-Server, geben Sie Folgendes an der Befehlszeile ein:
    
    ```
    Install-CsDatabase -Update -LocalDatabases

    ```

