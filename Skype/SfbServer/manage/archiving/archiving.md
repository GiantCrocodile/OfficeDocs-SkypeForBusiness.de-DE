---
title: Verwalten der Archivierung in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 63fd56cf-6d40-4db5-96fc-32d813930bcf
description: 'Zusammenfassung: Informationen Sie zum Verwalten der Archivierung für Skype für Business Server 2015.'
ms.openlocfilehash: fb8359d47b1933e2575685bc532d69e6b9bb6c45
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="manage-archiving-in-skype-for-business-server-2015"></a>Verwalten der Archivierung in Skype for Business Server 2015

**Zusammenfassung:** Informationen Sie zum Verwalten der Archivierung für Skype für Business Server 2015.
  
Die ursprüngliche Konfiguration wird beim Bereitstellen der Archivierung in Ihrer Organisation vorgenommen. Zu einem späteren Zeitpunkt kann es jedoch wünschenswert oder notwendig sein, die Implementierung der Archivierungsunterstützung an alltägliche Verwaltungsvorgänge oder neue Herausforderungen anzupassen. Beispielsweise kann es sein, dass Sie die Archivierungsunterstützung für einen bestimmten Standort, einen bestimmten Pool oder bestimmte Benutzer in Ihrer Organisation verändern müssen. Für Benutzer in Skype für Business Server verwaltet werden, Sie zu diesem Zweck erstellen und Anpassen von Archivierungsoptionen für Konfiguration und Benutzerrichtlinien. 
  
Bevor Sie dieses Thema lesen, sollten Sie darauf achten Sie, dass Sie mit den Informationen im [für die Archivierung in Skype für Business Server 2015 planen](../../plan-your-deployment/archiving/archiving.md) und [Bereitstellen Archivierung für Skype für Business Server 2015](../../deploy/deploy-archiving/deploy-archiving.md)vertraut sind.
  
> [!NOTE]
> Wenn Sie für Ihre Bereitstellung die Microsoft Exchange-Integration aktiviert haben, wird mithilfe von Exchange-Richtlinien gesteuert, ob die Archivierung für die Benutzer aktiviert ist, die Exchange zugeordnet sind und deren Postfächer im Compliance-Archiv platziert sind. Weitere Informationen hierzu finden Sie unter [Planen für die Archivierung in Skype für Business Server 2015](../../plan-your-deployment/archiving/archiving.md) und [Integration mit Exchange-Speicher für Skype für Business Server 2015 konfigurieren](../../deploy/deploy-archiving/configure-integration-with-exchange-storage.md). 
  
## <a name="archiving-configuration-options"></a>Optionen für die Archivierungskonfiguration

Mit den Optionen für die Archivierungskonfiguration können Sie Folgendes festlegen:
  
- Archivierung aktivieren oder deaktivieren
    
- Chatsitzungen archivieren
    
- Webkonferenzsitzungen archivieren
    
- Aktivitäten blockieren, wenn keine Archivierung verfügbar ist
    
- Exchange-Integration verwenden
    
- Löschen und Exportieren von Daten einrichten
    
Diese Optionen können auf globaler, Standort- oder Poolebene festgelegt werden. Weitere Informationen finden Sie unter [Manage Archivierungsoptionen in Skype für Business Server 2015](options.md).
  
## <a name="archiving-policies"></a>Archivierungsrichtlinien

Archivierungsrichtlinien bestimmen, ob die folgenden archiviert:
  
- Interne Kommunikation
    
- Externe Kommunikation
    
Diese Richtlinien können auf globaler, Standort- oder Poolebene festgelegt werden. Weitere Informationen finden Sie unter [Verwalten von Archivierungsrichtlinien in Skype für Business Server 2015](policies.md).
  
## <a name="manage-archiving-by-using-the-control-panel-or-by-using-windows-powershell"></a>Archivierungsverwaltung mithilfe der Systemsteuerung oder von Windows-PowerShell

Sie können die Archivierung mit der Systemsteuerung oder Windows-PowerShell verwalten. In der folgenden Tabelle finden Sie einen Überblick über die zur Archivierungsverwaltung verfügbaren Cmdlets. Ausführliche Informationen zur Syntax, einschließlich aller verfügbaren Parameter finden Sie unter [Skype für Business Server 2015-Verwaltungsshell](../management-shell.md). 


|**Cmdlet**|**Beschreibung**|
|:-----|:-----|
|Export-CsArchivingData  <br/> |Exportiert die Datensätze, die in der Skype für Business Server-Archivierungsdatenbank gespeichert wurden.  <br/> |
|Get-CsArchivingConfiguration  <br/> |Gibt Informationen zu den in Ihrer Organisation verwendeten Konfigurationseinstellungen zurück.  <br/> |
|Get-CsArchivingPolicy  <br/> |Gibt Informationen zu den in Ihrer Organisation verwendeten Archivierungsrichtlinien für interne und externe Kommunikationen zurück.  <br/> |
|GRANT-CsArchivingPolicy  <br/> |Instant messaging (IM) Sitzung Archivierungsrichtlinien für Benutzer oder Gruppen von Benutzern zugewiesen. Mithilfe dieser Archivierungsrichtlinien können Sie alle Chatsitzungen archivieren, die zwischen internen Benutzern und/oder zwischen internen und externen Benutzern stattfinden.  <br/> |
|"Invoke-csarchivingdatabasepurge"  <br/> |Dient zum manuellen Löschen von Einträgen aus der Archivierungsdatenbank.  <br/> |
|Mit New-CsArchivingConfiguration  <br/> |Erstellt einen neuen Satz mit Chatnachrichteneinstellungen. Diese Einstellungen dienen zum Aktivieren bzw. Deaktivieren der automatischen Speicherung von Chatsitzungen. Sie ermöglichen ferner das Blockieren von Chatnachrichten, die nicht archiviert werden können.  <br/> |
|Mit New-CsArchivingPolicy  <br/> |Erstellt neue Archivierungsrichtlinien für Chatsitzungen. Mithilfe dieser Archivierungsrichtlinien können Sie alle Chatsitzungen archivieren, die zwischen internen Benutzern und/oder zwischen internen und externen Benutzern stattfinden.  <br/> |
|Remove-CsArchivingConfiguration  <br/> |Entfernt die angegebene Auflistung von Archivierungseinstellungen. Archivierungseinstellungen dienen zum Aktivieren und Deaktivieren des automatischen Speicherns von Chatsitzungen sowie zum optionalen Sperren aller Chatnachrichten, die nicht archiviert werden können.  <br/> |
|Remove-CsArchivingPolicy  <br/> |Entfernt die angegebene Sofortnachrichten (Instant messaging) Archivierungsrichtlinie, der bestimmt, ob Skype für Business Server automatisch alle Sofortnachrichtensitzungen gespeichert, die zwischen internen Benutzern und/oder alle Sofortnachrichtensitzungen zwischen internen Benutzern und Verbundpartner stattfinden.  <br/> |
|Set-CsArchivingConfiguration  <br/> |Ändert eine bestehende Auflistung von Archivierungseinstellungen für Chatnachrichten.  <br/> |
|Set-CsArchivingPolicy  <br/> |Ändert eine vorhandene Sofortnachrichten (Instant messaging) Archivierungsrichtlinie. Eine Archivierungsrichtlinie bietet die Möglichkeit, alle IM-Sitzungen und Konferenzen, die stattfinden zwischen internen Benutzern archivieren. Sie können auch Sitzungen archivieren, die zwischen internen Benutzern und Verbundpartner stattfinden.  <br/> |
|Set-CsArchivingServer  <br/> |Ermöglicht Ihnen die Angabe eines neuen Datenbankpfads für einen oder mehrere Archivierungsserver.  <br/> |
   
