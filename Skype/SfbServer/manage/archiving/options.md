---
title: Verwalten von Archivierungsoptionen in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 50399f26-58a3-4ce2-8229-32a8cafc7733
description: 'Zusammenfassung: Informationen Sie zum Konfigurieren von Archivierungsoptionen für Skype für Business Server 2015.'
ms.openlocfilehash: 29800fef7054cd0e82f203d2ad6ec1ed53251ca4
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="manage-archiving-options-in-skype-for-business-server-2015"></a>Verwalten von Archivierungsoptionen in Skype for Business Server 2015

**Zusammenfassung:** Informationen Sie zum Konfigurieren von Archivierungsoptionen für Skype für Business Server 2015.
  
Erstkonfiguration Archivierung bei der Bereitstellung, aber Sie können ändern, hinzufügen und Löschen von Konfigurationen nach der Bereitstellung. Archivierungsoptionen zu bestimmen, ob: 
  
- Archivierung aktivieren oder deaktivieren
    
- Chatsitzungen archivieren
    
- Webkonferenzsitzungen archivieren
    
- Aktivitäten blockieren, wenn keine Archivierung verfügbar ist
    
- Exchange-Integration verwenden
    
- Löschen und Exportieren von Daten einrichten
    
Sie können Konfigurationsoptionen auf den folgenden Ebenen festlegen:
  
- Konfiguration auf globaler Ebene, die standardmäßig erstellt wird, bei der Bereitstellung von Skype für Business Server
    
- Optionale Konfigurationen auf Standortebene, um anzugeben, wie die Archivierung für einen bestimmten Standort implementiert wird
    
- Optionale Konfigurationen auf Poolebene, die angeben, wie die Archivierung für einen bestimmten Pool implementiert wird
    
Standort- oder Poolkonfigurationen können gelöscht werden, nicht aber die globale Konfiguration. Wenn Sie die globale Konfiguration löschen, wird sie automatisch auf die Standardwerte zurückgesetzt. Weitere Informationen dazu, wie Sie die Archivierung Konfigurationen implementiert werden und die Hierarchie der Archivierungskonfigurationen, finden Sie unter [Planen für die Archivierung in Skype für Business Server 2015](../../plan-your-deployment/archiving/archiving.md).
  
## <a name="configure-archiving-options-by-using-the-control-panel"></a>Konfigurieren von Archivierungsoptionen mit der Systemsteuerung

Sie können die Archivierungsoptionen wie folgt mit der Systemsteuerung konfigurieren:
  
1. Melden Sie sich mit einem Benutzerkonto, dem die Rolle „CsArchivingAdministrator“ oder „CsAdministrator“ zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an. 
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen. 
    
3. Klicken Sie in der linken Navigationsleiste auf **Archivierungskonfiguration**.
    
## <a name="configure-archiving-options-by-using-windows-powershell"></a>Konfigurieren von Archivierungsoptionen mit Windows PowerShell

Sie können die Archivierungsoptionen auch mithilfe der in der folgenden Tabelle aufgeführten Windows PowerShell-Cmdlets konfigurieren. Ausführliche Informationen zur Syntax, einschließlich aller verfügbaren Parameter finden Sie unter [Skype für Business Server 2015-Verwaltungsshell](../management-shell.md).
  

|**Cmdlet**|**Beschreibung**|
|:-----|:-----|
|Get-CsArchivingConfiguration  <br/> |Gibt Informationen zu den in Ihrer Organisation verwendeten Konfigurationseinstellungen zurück.  <br/> |
|Mit New-CsArchivingConfiguration  <br/> |Erstellt einen neuen Satz mit Chatnachrichteneinstellungen. Diese Einstellungen dienen zum Aktivieren bzw. Deaktivieren der automatischen Speicherung von Chatsitzungen. Sie ermöglichen ferner das Blockieren von Chatnachrichten, die nicht archiviert werden können.  <br/> |
|Remove-CsArchivingConfiguration  <br/> |Entfernt die angegebene Auflistung von Archivierungseinstellungen. Archivierungseinstellungen dienen zum Aktivieren und Deaktivieren des automatischen Speicherns von Chatsitzungen sowie zum optionalen Sperren aller Chatnachrichten, die nicht archiviert werden können.  <br/> |
|Set-CsArchivingConfiguration  <br/> |Ändert eine bestehende Auflistung von Optionen zur Archivierungskonfiguration für Chatnachrichten.  <br/> |