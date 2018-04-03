---
title: Ändern von QoE-Einstellungen (Quality of Experience) in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: a6b41de2-1466-4240-8a70-14ce6f0f3ddc
description: 'Zusammenfassung: Erfahren Sie, wie Beibehaltungsdauer für QoE-Daten in Skype für Business Server 2015 angeben.'
ms.openlocfilehash: 99a85a389b225d57b48b52b3f6f1d5b66e93f122
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="modify-quality-of-experience-settings-in-skype-for-business-server-2015"></a>Ändern von QoE-Einstellungen (Quality of Experience) in Skype for Business Server 2015
 
**Zusammenfassung:** Erfahren Sie, wie Beibehaltungsdauer für QoE-Daten in Skype für Business Server 2015 angeben.
  
In der Standardeinstellung werden QoE-Daten (Quality of Experience, Erlebnisqualität) nach 60 Tagen gelöscht. Sie können die Einstellungen auf der Seite **QoE-Daten** verwenden, um die Daten für einen längeren oder kürzeren Zeitraum zu speichern. Wenn Sie QoE deaktivieren, werden auch Daten gelöscht, die bei aktivierter QoE-Datenerfassung aufgezeichnet wurden.
  
> [!NOTE]
> Sie sollten die Aufzeichnung von Kommunikationsdatensätzen (KDS) und QoE-Daten so konfigurieren, dass Daten für die gleiche Anzahl von Tagen gespeichert werden. Die Berichte zu den aufgezeichneten Kommunikationsdatensätzen (KDS), verfügbar auf der Webseite für Überwachungsberichte, umfassen KDS- und QoE-Informationen zu jedem Anruf. Wenn die Zeit bis zum Löschen für KDS und QoE abweicht, umfassen einige Anrufe möglicherweise nur KDS-Daten, während andere ausschließlich QoE-Daten aufweisen. 
  
Das nachfolgende Verfahren beschreibt, wie Sie die Löscheinstellungen für QoE-Daten konfigurieren. 
  
### <a name="to-specify-retention-of-qoe-data-by-using-skype-for-business-server-control-panel"></a>Zum Angeben der Beibehaltungsdauer von QoE-Daten mithilfe von Skype Business Server-Systemsteuerung

1.  Melden Sie sich an dem Computer als Mitglied der Gruppe RTCUniversalServerAdmins oder als Mitglied der Rolle CsVoiceAdministrator, CsServerAdministrator oder csadministrator an. Weitere Informationen hierzu finden Sie unter **Delegate Setup Permissions**.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen.  
    
3. Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **QoE-Daten**.
    
4. Klicken Sie auf der Seite **QoE-Daten** in der Tabelle auf den geeigneten Standort, klicken Sie auf **Bearbeiten** und anschließend auf **Details anzeigen**.
    
5. Wählen Sie die Option **Löschen für QoE aktivieren** aus, um die Löschung zu aktivieren.
    
6. Wählen Sie unter **Maximale Speicherdauer für die QuE-Aufzeichnung (Tage)** die maximale Anzahl von Tagen aus, für die QoE-Daten gespeichert werden sollen.
    
7. Klicken Sie auf **Commit ausführen**.
    
## <a name="specifying-qoe-retention-by-using-windows-powershell-cmdlets"></a>Angeben der Beibehaltungsdauer für QoE mithilfe von Windows PowerShell-Cmdlets

Sie können QoE-beibehaltungseinstellungen mithilfe von Windows PowerShell und das **Set-CsQoEConfiguration** -Cmdlet erstellen. Sie können dieses Cmdlet entweder von der Skype für Business Server-Verwaltungsshell oder aus einer Remotesitzung von Windows PowerShell ausführen. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-specify-qoe-retention-for-a-specific-location"></a>So geben Sie die QoE-Aufbewahrung für einen speziellen Standort an

- Dieser Befehl ermöglicht das Löschen von QoE-Daten für den Standort Redmond. Zudem wird damit für die QoE-Daten eine Aufbewahrungsdauer von 20 Tagen konfiguriert.
    
  ```
  Set-CsQoeConfiguration -Identity "site:Redmond" -EnablePurging -KeepQoEDataForDays 20
  ```

### <a name="to-specify-qoe-retention-for-multiple-locations"></a>So geben Sie die QoE-Aufbewahrung für mehrere Standorte an

- Mit diesem Befehl wird die Beibehaltung von QoE-Daten für alle in einer Organisation verwendeten QoE-Konfigurationseinstellungen konfiguriert.
    
  ```
  Get-CsQoEConfiguration | Set-CsQoEConfiguration-EnablePurging -KeepQoEDataForDays 20 
  ```

Weitere Informationen finden Sie im Hilfethema zum [Set-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csqoeconfiguration?view=skype-ps) -Cmdlet.
  
## <a name="see-also"></a>Siehe auch

#### 

[Bereitstellen des Monitoring](http://technet.microsoft.com/library/117f4a3e-0670-4388-a553-b9854921145f.aspx)
