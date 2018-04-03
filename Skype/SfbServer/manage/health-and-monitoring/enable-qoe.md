---
title: Aktivieren von QoE (Quality of Experience) in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: c8bb3c67-b324-4d94-8158-00c792c7ac42
description: 'Zusammenfassung: erfahren Sie, wie Quality of Experience (QoE) in Skype für Business Server 2015 zu aktivieren.'
ms.openlocfilehash: 8c63a1bf493e601c4936b83cc9edfaa6e3727f26
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="enable-quality-of-experience-in-skype-for-business-server-2015"></a>Aktivieren von QoE (Quality of Experience) in Skype for Business Server 2015
 
**Zusammenfassung:** erfahren Sie, wie Quality of Experience (QoE) in Skype für Business Server 2015 zu aktivieren.
  
Bei der QoE-Datenerfassung (Quality of Experience) werden numerische Daten aufgezeichnet, die die Medienqualität sowie Informationen zu Teilnehmern, Gerätenamen, Treibern, IP-Adressen und Endpunkttypen im Zusammenhang mit Anrufen und Sitzungen angeben. Weitere Informationen hierzu finden Sie unter [Planning for Monitoring](http://technet.microsoft.com/library/26cead5a-183c-42f1-a4b0-0e8d61c6159d.aspx) in der Planungsdokumentation.
  
Verwenden Sie das folgende Verfahren, um QoE in der gesamten Organisation oder für jeden Standort in Ihrer Organisation zu aktivieren.
  
> [!NOTE]
> Zur Aktivierung von QoE müssen Sie zunächst die Überwachung und eine Monitoring-Back-End-Datenbank konfigurieren. Weitere Informationen hierzu finden Sie unter [Deploying Monitoring](http://technet.microsoft.com/library/117f4a3e-0670-4388-a553-b9854921145f.aspx). 
  
### <a name="to-enable-qoe-by-using-skype-for-business-server-control-panel"></a>So aktivieren Sie QoE mithilfe von Skype Business Server-Systemsteuerung

1.  Von einem Benutzerkonto, das Mitglied der Gruppe RTCUniversalServerAdmins (oder gleichwertige Benutzerrechte verfügt), oder der CsServerAdministrator oder CsAdministrator-Rolle, melden Sie sich an einem beliebigen Computer, die im Netzwerk ist in der Bereitstellung von Skype für Business Server zugeordnet ist 2015.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen.  
    
3. Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **QoE-Daten**. 
    
4. Klicken Sie auf der Seite **Quality of Experience-Daten** in der Tabelle auf die entsprechende Auflistung, klicken Sie auf **Aktion** und anschließend auf **QoE aktivieren**.
    
## <a name="enabling-qoe-by-using-windows-powershell-cmdlets"></a>Aktivieren QoE mithilfe von Windows PowerShell-Cmdlets

Sie können mithilfe von Windows PowerShell und das **Set-CsQoEConfiguration** -Cmdlet QoE aktivieren. Sie können dieses Cmdlet entweder von der Skype für Business Server-Verwaltungsshell oder aus einer Remotesitzung von Windows PowerShell ausführen. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-enable-qoe-for-a-single-location"></a>So aktivieren Sie QoE für einen einzelnen Standort

 Zum Aktivieren von QoE legen Sie den EnableQoE-Parameter auf „True“ ($True) fest.
    
  ```
  Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $True
  ```

### <a name="to-disable-qoe-for-a-single-location"></a>So deaktivieren Sie QoE für einen einzelnen Standort

 Zum Deaktivieren von QoE legen Sie den EnableQoE-Parameter auf „False“ ($False) fest. Die Überwachung wird dadurch nicht deinstalliert. Das Erfassen und Speichern von QoE-Daten wird unterbrochen.
    
  ```
  Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $False
  ```

### <a name="to-use-a-single-command-to-enable-qoe-in-multiple-locations"></a>So aktivieren Sie QoE mit einem einzelnen Befehl an mehreren Standorten

 Mit diesem Befehl wird QoE für alle derzeit in Ihrer Organisation verwendeten QoE-Konfigurationseinstellungen aktiviert.
    
  ```
  Get-CsQoEConfiguration | Set-CsQoEConfiguration "site:Redmond" -EnableQoE $True
  ```

Weitere Informationen hierzu finden Sie unter [Set-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csqoeconfiguration?view=skype-ps).
  
## <a name="see-also"></a>Siehe auch

[Planen der Überwachung](http://technet.microsoft.com/library/26cead5a-183c-42f1-a4b0-0e8d61c6159d.aspx)
  
[Bereitstellen des Monitoring](http://technet.microsoft.com/library/117f4a3e-0670-4388-a553-b9854921145f.aspx)
