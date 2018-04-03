---
title: Erstellen von QoE-Konfigurationseinstellungen in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 64f05569-07c7-4f76-a96b-ea4125a510d5
description: 'Zusammenfassung: Informationen Sie zu Quality of Experience (QoE)-Einstellungen in Skype für Business Server 2015.'
ms.openlocfilehash: a6ba2906b54ac5d963b0c8394c1fcf254cffd12d
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="create-quality-of-experience-configuration-settings-in-skype-for-business-server-2015"></a>Erstellen von QoE-Konfigurationseinstellungen in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zu Quality of Experience (QoE)-Einstellungen in Skype für Business Server 2015.
  
QoE (Quality of Experience)-Metriken dienen der Überwachung der Qualität von Audio- und Videoanrufen in Ihrer Organisation, z. B. der Anzahl der verloren gegangenen Netzwerkpakete, von Hintergrundgeräuschen und der Unterschiede bei Paketverzögerung (Jitter). Diese Metriken werden in einer Datenbank getrennt von anderen Daten (z. B. den Kommunikationsdatensätzen) gespeichert, sodass QoE unabhängig von anderen Datenaufzeichnungen aktiviert und deaktiviert werden kann.
  
Bei der Installation von Skype für Business Server 2015, ein einzelnes wird die globale Auflistung von QoE-Konfigurationseinstellungen für Sie erstellt. Administratoren haben auch die Möglichkeit, benutzerdefinierte Einstellungen für die Standortebene zu erstellen. Wenn diese standortspezifischen Einstellungen verwendet werden, haben sie Vorrang vor den globalen Einstellungen. Beispiel: Wenn Sie für den Standort Redmond standortspezifische Einstellungen erstellen, wird QoE in Redmond gemäß diesen Einstellungen (anstelle der globalen) verwaltet.
  
QoE-Konfigurationseinstellungen können unter Verwendung von entweder Skype für Business Server-Systemsteuerung oder das [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/new-csqoeconfiguration?view=skype-ps) -Cmdlet erstellt werden. Wenn Sie Skype Business Server-Systemsteuerung verwenden, erstellen Sie neue Einstellungen werden die folgenden Optionen zur Verfügung:
  
|**UI-Einstellung**|**PowerShell-parameter**|**Beschreibung**|
|:-----|:-----|:-----|
|Name  <br/> |Identität  <br/> |Eindeutiger Bezeichner für die zu erstellenden Einstellungen. QoE-Konfigurationseinstellungen können nur auf der Standortebene erstellt werden.  <br/> |
|Überwachung der QoE-Daten aktivieren  <br/> |EnableQoE  <br/> |Gibt an, ob QoE-Datensätze erfasst und in der Überwachungsdatenbank gespeichert werden.  <br/> |
|Löschvorgang für QoE-Daten aktivieren  <br/> |"Enablepurging"  <br/> |Gibt an, ob Datensätze nach Ablauf des in der Eigenschaft **QoE-Daten für maximal (Tage) aufbewahren** festgelegten Zeitraums gelöscht werden sollen. <br/> |
|QoE-Daten für maximal (Tage) aufbewahren  <br/> |"Keepqoedatafordays"  <br/> |Zeitdauer in Tagen, die QoE-Daten gespeichert bleiben sollen, bevor sie aus der Datenbank gelöscht werden. Bei deaktiviertem Löschvorgang wird dieser Wert ignoriert.  <br/> |
   
> [!NOTE]
> Das Cmdlet New-CsQoEConfiguration enthält zusätzliche Optionen für die Business Server-Systemsteuerung in Skype nicht verfügbar. Weitere Informationen finden Sie im Hilfethema [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/new-csqoeconfiguration?view=skype-ps) .
  
### <a name="to-create-qoe-configuration-settings-by-using-skype-for-business-server-control-panel"></a>Erstellen Sie QoE-Konfigurationseinstellungen mithilfe von Skype Business Server-Systemsteuerung

1. Melden Sie sich an dem Computer als Mitglied der Gruppe RTCUniversalServerAdmins oder als Mitglied der Rolle CsVoiceAdministrator, CsServerAdministrator oder csadministrator an. Weitere Informationen hierzu finden Sie unter **Delegate Setup Permissions**.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen.  
    
3. Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **QoE-Daten**.
    
4. Klicken Sie auf der Seite **QoE-Daten** auf **Neu**.
    
5. Klicken Sie unter **Standort auswählen** auf den Standort, auf den die Richtlinie angewendet werden soll und klicken Sie dann auf **OK**.
    
6. Tun Sie unter **Neue QoE-Einstellung** Folgendes:
    
   - Wählen Sie **Überwachung der QoE-Daten aktivieren** aus, um die Überwachung einzuschalten.
    
   - Wählen Sie **Löschvorgang für QoE-Daten aktivieren** aus, um den Löschvorgang einzuschalten.
    
   - Wählen Sie unter **QoE-Daten für maximal (Tage) aufbewahren** aus, wie viele Tage QoE-Datensätze maximal aufbewahrt werden sollen.
    
7. Klicken Sie auf **Commit ausführen**.
    
## <a name="creating-qoe-configuration-settings-by-using-windows-powershell-cmdlets"></a>Erstellen von QoE-Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets

Sie können QoE-Konfigurationseinstellungen mithilfe von Windows PowerShell und das New-CsQoEConfiguration-Cmdlet erstellen. Sie können dieses Cmdlet entweder von der Skype für Business Server-Verwaltungsshell oder aus einer Remotesitzung von Windows PowerShell ausführen. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-create-a-new-collection-of-qoe-configuration-settings"></a>So erstellen Sie eine neue Auflistung von QoE-Konfigurationseinstellungen

 Dieser Befehl erstellt eine neue Auflistung von QoE-Konfigurationseinstellungen, die für den Standort „Redmond“ gelten sollen:
    
  ```
  New-CsQoEConfiguration -Identity "site:Redmond"
  ```

### <a name="to-create-a-new-collection-of-qoe-configuration-settings-where-qoe-monitoring-is-disabled"></a>So erstellen Sie eine neue Auflistung von QoE-Konfigurationseinstellungen mit deaktivierter QoE-Überwachung

 Da in dem oben aufgeführten Befehl keine Parameter (außer dem obligatorischen Identity-Parameter) angegeben sind, werden in den neuen Konfigurationseinstellungen bei allen Eigenschaften die Standardwerte verwendet. Wenn Sie Einstellungen erstellen möchten, deren Eigenschaften andere Werte haben, fügen Sie in den Befehl einfach den entsprechenden Parameter mit dem gewünschten Wert ein. Beispiel: Zum Erstellen von QoE-Konfigurationseinstellungen, die es standardmäßig erlauben, die QoE-Aufzeichnung zu deaktivieren, verwenden Sie einen Befehl der folgenden Art:
    
  ```
  New-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $False
  ```

### <a name="to-specify-multiple-property-values-when-creating-a-new-collection-of-qoe-configuration-settings"></a>So geben Sie beim Erstellen einer neuen Auflistung von QoE-Konfigurationseinstellungen mehrere Eigenschaftswerte an:

 Sie können mehrere Eigenschaftswerte angeben, indem Sie mehrere Parameter in den Befehl einfügen. So konfiguriert zum Beispiel dieser Befehl die neuen Einstellungen so, dass QoE-Daten 30 Tage aufbewahrt und alte Daten um 03:00 Uhr bereinigt werden:
    
  ```
  New-CsQoEConfiguration -Identity "site:Redmond" -KeepQoEDataForDays 30 -PurgeHourOfDay 3
  ```

Weitere Informationen finden Sie im Hilfethema für das [New-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/new-csqoeconfiguration?view=skype-ps) -Cmdlet.
  
