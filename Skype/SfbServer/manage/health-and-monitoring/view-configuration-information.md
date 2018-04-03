---
title: Anzeigen von KDS-Konfigurationsinformationen in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 77bd553f-da89-4c84-a5d0-2f7e91d04383
description: 'Zusammenfassung: Erfahren Sie, wie Aufzeichnung von Kommunikationsdatensätzen (KDS) in Skype für Business Server 2015 verwenden.'
ms.openlocfilehash: 6eacc6c300cfc1faae843a1dc610b17b45ae9c88
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="view-cdr-configuration-information-in-skype-for-business-server-2015"></a>Anzeigen von KDS-Konfigurationsinformationen in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zur Verwendung von Kommunikationsdatensätzen (KDS) in Skype für Business Server 2015.
  
Die Funktion zum Aufzeichnen von Kommunikationsdatensätzen (KDS) ermöglicht das Nachverfolgen von Peer-to-Peer-, VoIP- und Konferenzanrufen. Diese Nutzungsdaten umfassen Informationen wie z. B. Anrufer, Angerufener, Anrufzeitpunkt und Anrufdauer.
  
Bei der Installation von Skype für Business Server 2015, ein einzelnes wird die globale Auflistung von KDS-Konfigurationseinstellungen für Sie erstellt. Administratoren können darüber hinaus Auflistungen mit benutzerdefinierten Einstellungen erstellen, die auf die einzelnen Standorte angewendet werden können. Sie können mithilfe von Skype für Business Server-Systemsteuerung oder [Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/get-cscdrconfiguration?view=skype-ps) -Cmdlet KDS-Konfigurationseinstellungen derzeit in Ihrer Organisation anzeigen.
  
### <a name="to-view-cdr-configuration-information-by-using-skype-for-business-server-control-panel"></a>So zeigen Sie KDS-Konfigurationsinformationen mithilfe von Skype Business Server-Systemsteuerung an

1. Klicken Sie in Skype Business Server-Systemsteuerung auf **Überwachung und Archivierung**.
    
2. Auf der Registerkarte **Aufzeichnung von Kommunikationsdatensätzen** wird eine Liste mit allen KDS-Konfigurationseinstellungen angezeigt; für jede Einstellungsauflistung wird der **Name** der Auflistung angezeigt; ob KDS aktiviert wurde oder nicht (die Eigenschaft **KDS**); und ob der Löschvorgang (die Eigenschaft **KDS-Löschvorgang**) aktiviert wurde oder nicht. Sie können detaillierte Informationen zu einer Auflistung anzeigen, indem Sie doppelt auf diese Auflistung klicken. Alternativ können Sie die gewünschte Auflistung auswählen und auf **Bearbeiten** und **Details anzeigen** klicken. Beachten Sie Folgendes: Es können jeweils nur detaillierte Informationen zu einer Auflistung mit KDS-Konfigurationseinstellungen angezeigt werden.
    
## <a name="viewing-cdr-configuration-information-by-using-windows-powershell-cmdlets"></a>Anzeigen von KDS-Konfigurationsinformationen mithilfe von Windows PowerShell-cmdlets

Sie können KDS-Konfigurationseinstellungen mithilfe von Windows PowerShell und das Cmdlet Get-CsCdrConfiguration anzeigen. Sie können dieses Cmdlet entweder von der Skype für Business Server-Verwaltungsshell oder aus einer Remotesitzung von Windows PowerShell ausführen. Weitere Informationen zur Verwendung von remote Windows PowerShell zum Skype für Business Server herstellen finden Sie im Blog-Artikel ["Quick Start: Verwalten von Microsoft Lync Server 2010 Using Remote PowerShell"](https://go.microsoft.com/fwlink/p/?linkId=255876). Der Vorgang ist in Skype für Business Server identisch.
  
### <a name="to-view-cdr-configuration-information"></a>So zeigen Sie KDS-Konfigurationsinformationen an

- Anzeigen von Informationen zu allen KDS-Konfigurationseinstellungen, geben Sie den folgenden Befehl in der Skype für Business Server-Verwaltungsshell, und drücken Sie die EINGABETASTE:
    
  ```
  Get-CsCdrConfiguration
  ```

    Es werden etwa folgende Informationen zurückgegeben:
    
  ```
  Identity               : Global
EnableCDR              : True
EnablePurging          : True
KeepCallDetailForDays  : 90
KeepErrorReportForDays : 60
PurgeHourOfDay         : 2

  ```

Weitere Informationen finden Sie im Hilfethema zum [Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/get-cscdrconfiguration?view=skype-ps) -Cmdlet.
  
