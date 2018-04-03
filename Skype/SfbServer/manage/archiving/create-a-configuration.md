---
title: Erstellen einer Archivierungskonfiguration in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: dc574afa-0b7d-404f-99b3-c812430b7c70
description: 'Zusammenfassung: Informationen Sie zum Erstellen einer Archivierungskonfiguration für Skype für Business Server 2015.'
ms.openlocfilehash: 5675117d14d35e0055c7e494ce9476d421dda443
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="create-an-archiving-configuration-in-skype-for-business-server-2015"></a>Erstellen einer Archivierungskonfiguration in Skype for Business Server 2015

**Zusammenfassung:** Informationen Sie zum Erstellen einer Archivierungskonfiguration für Skype für Business Server 2015.
  
## <a name="configure-archiving-options-by-using-the-control-panel"></a>Konfigurieren von Archivierungsoptionen mithilfe der Systemsteuerung

So konfigurieren Sie Archivierungsoptionen für einen bestimmten Standort oder einen bestimmten Pool: 
  
1. Melden Sie sich mit einem Benutzerkonto, dem die Rolle „CsArchivingAdministrator“ oder „CsAdministrator“ zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an. 
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen. 
    
3. Klicken Sie auf der linken Navigationsleiste auf **Überwachung und Archivierung** und anschließend auf **Archivierungskonfiguration**.
    
4. Klicken Sie auf der Seite **Archivierungskonfiguration** auf **Neu** und führen Sie eine der folgenden Aktionen aus: 
    
   - Um eine Standortarchivierungskonfiguration zu erstellen, klicken Sie auf **Standortkonfiguration** und wählen Sie anschließend in **Standort auswählen** den Standort aus, der für die Archivierung konfiguriert werden soll.
    
   - Um eine Poolarchivierungskonfiguration zu erstellen, klicken Sie auf **Poolkonfiguration** und wählen Sie anschließend in **Pool auswählen** den Pool aus, der für die Archivierung konfiguriert werden soll.
    
5. Führen Sie unter **Neue Archivierungseinstellung** im Dropdown-Listenfeld **Archivierungseinstellung** eine der folgenden Aktionen aus:
    
   - Klicken Sie auf **Chatsitzungen archivieren**, um die Archivierung ausschließlich für Chatsitzungen zu aktivieren.
    
   - Klicken Sie auf **Chat- und Webkonferenzsitzungen archivieren**, um sowohl Chatsitzungen als auch Konferenzen zu archivieren.
    
   - Klicken Sie auf **Archivierung deaktivieren**, um die Archivierung für diese Konfiguration zu deaktivieren.
    
6. Führen Sie außerdem in **Neue Archivierungseinstellung** die folgenden Aktionen aus:
    
   - Aktivieren Sie das Kontrollkästchen **Bei Archivierungsfehler Chat- oder Webkonferenzsitzungen blockieren**, um Aktivitäten zu blockieren, wenn die Archivierung nicht verfügbar ist.
    
   - Klicken Sie auf das Kontrollkästchen **Microsoft Exchange-Integration** , um die Verwendung von Microsoft Exchange Server zum Speichern von archivierten Daten.
    
   - Zum Aktivieren des Löschvorgangs für Daten aktivieren Sie das Kontrollkästchen **Bereinigungsfunktion für alle Archivierungsdaten aktivieren** und führen Sie einen der folgenden Schritte aus:
    
     - Klicken Sie auf **Löschen von exportierten und gespeicherten Archivierungsdaten nach einer Höchstdauer von (Tage)** und geben Sie eine Anzahl von Tagen an, um die archivierten Inhalte nach einer bestimmten Anzahl von Tagen zu löschen.
    
     - Klicken Sie auf **Nur exportierte Archivierungsdaten löschen**, um nur die exportierten Daten zu löschen.
    
7. Klicken Sie auf **Commit ausführen**.
    
## <a name="configure-archiving-options-by-using-windows-powershell"></a>Konfigurieren von Archivierungsoptionen mit Windows PowerShell

Mithilfe des Cmdlets **New-CsArchivingConfiguration** können Sie ebenfalls Archivierungsoptionen für einen bestimmten Standort oder einen bestimmten Pool konfigurieren.
  
Mit dem folgenden Befehl wird eine neue Auflistung von Archivierungskonfigurationseinstellungen für den Standort „Redmond“ erstellt:
  
```
New-CsArchivingConfiguration -Identity "site:Redmond"
```

Da im vorherigen Befehl keine weiteren Parameter außer dem obligatorischen Identity-Parameter angegeben wurden, werden in der neuen Auflistung von Konfigurationseinstellungen für alle Eigenschaften die Standardwerte verwendet. 
  
Zum Erstellen von Einstellungen, die verschiedene Eigenschaftswerte verwenden, geben Sie einfach den entsprechenden Parameter und den Parameterwert an. Im folgenden Beispiel wird eine Auflistung von Konfigurationseinstellungen erstellt, die standardmäßig nur die Archivierung von Chatsitzungen zulassen:
  
```
New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly"
```

Mehrere Eigenschaftswerte können geändert werden, indem Sie mehrere Parameter angeben. Beispielsweise werden mit dem folgenden Befehl die neuen Einstellungen so konfiguriert, dass Chatsitzungen archiviert werden und Chats blockiert werden, falls der Archivierungsdienst nicht verfügbar ist:
  
```
New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly" -BlockOnArchiveFailure $True
```

Weitere Informationen finden Sie im Hilfethema für das [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/new-csarchivingconfiguration?view=skype-ps) -Cmdlet.