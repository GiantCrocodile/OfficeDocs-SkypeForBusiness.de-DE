---
title: Geräteprotokollkonfiguration
ms.author: laurawi
author: LauraWi
manager: serdars
ms.date: 3/23/2015
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.lscp.ClientDeviceCfgMain
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: c9b81f20-ce8c-40f1-8bed-50775cc35e58
description: Der Geräteaktualisierungs-Webdienst erstellt automatisch Protokolldateien, mit denen die Aktivität bei der Geräteaktualisierung aufgezeichnet wird. Im Rahmen Ihres Unternehmens Data Management-Strategie sollten Sie die Grenzwerte zu Protokollgröße Daten-Cache, Größe der Protokolldatei oder die Zeitdauer, die eine Protokolldatei gespeichert wird, bevor es gelöscht wird. Sie können diese Einstellungen entsprechend den Anforderungen der Organisation ändern. Falls Sie nicht möchten, dass der Geräteaktualisierungs-Webdienst die Protokolldateien automatisch löscht, können Sie diese je nach Bedarf manuell löschen. Protokolleinstellungen können global oder auf Standortebene geändert werden.
ms.openlocfilehash: e5a88c7437b654846fd464133b953465cd5d3e2a
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="device-log-configuration"></a>Geräteprotokollkonfiguration
 
Der Geräteaktualisierungs-Webdienst erstellt automatisch Protokolldateien, mit denen die Aktivität bei der Geräteaktualisierung aufgezeichnet wird. Im Rahmen Ihres Unternehmens Data Management-Strategie sollten Sie die Grenzwerte zu Protokollgröße Daten-Cache, Größe der Protokolldatei oder die Zeitdauer, die eine Protokolldatei gespeichert wird, bevor es gelöscht wird. Sie können diese Einstellungen entsprechend den Anforderungen der Organisation ändern. Falls Sie nicht möchten, dass der Geräteaktualisierungs-Webdienst die Protokolldateien automatisch löscht, können Sie diese je nach Bedarf manuell löschen. Protokolleinstellungen können global oder auf Standortebene geändert werden.
  
> [!NOTE]
> Sie können auch eine Uhrzeit konfigurieren, zu der der Geräteaktualisierungs-Webdienst automatisch Protokolldateien löscht, die älter sind als die angegebene Anzahl von Tagen für die Speicherung der Protokolldateien durch den Dienst (in der Standardeinstellung sind dies Protokolldateien, die älter als 10 Tage sind). Diese Einstellung kann nicht mit Skype Business Server-Systemsteuerung geändert werden. Stattdessen müssen Sie Skype für Business Server-Verwaltungsshell verwenden. Um die Uhrzeit für das Löschen von abgelaufenen Protokolldateien anzugeben, verwenden Sie das Cmdlet " **New-CsDeviceUpdateConfiguration** " mit dem LogCleanUpTimeOfDay - Parameter. Weitere Informationen hierzu finden Sie unter [New-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/new-csdeviceupdateconfiguration?view=skype-ps). 
  
> [!CAUTION]
> Durch das dauerhafte Löschen von Dateien werden diese aus dem Dateisystem entfernt. Nach dem Löschen einer Datei kann diese nicht mehr wiederhergestellt werden. 
  
## <a name="tasks-you-can-perform"></a>Mögliche Aufgaben

Auf der Seite **Geräteprotokollkonfiguration** können Sie die folgenden Aufgaben ausführen:
  
- Hinzufügen einer Geräteprotokollkonfiguration auf globaler Ebene oder für einen bestimmten Standort oder Pool
    
- Ändern der Optionen für eine vorhandene Geräteprotokollkonfiguration
    
## <a name="ui-reference"></a>Referenz zur Benutzeroberfläche

In den folgenden Listen werden die Menüs, Befehle, Felder und Eigenschaften der Seite beschrieben.
  
- **Neue** Sie können eine neue geräteprotokollkonfiguration mit dem folgenden Bereich hinzufügen:
    
  - Global
    
  - Standort
    
- **Bearbeiten** Sie können die Optionen in der Liste eine geräteprotokollkonfiguration ändern. Mit dieser Option haben Sie folgende Möglichkeiten:
    
  - **Details anzeigen** Diese Option öffnet ein Dialogfeld, in dem Sie die Optionen für eine geräteprotokollkonfiguration ändern können.
    
  - **Wählen Sie alle** Diese Option werden alle geräteprotokollkonfigurationen der Liste ausgewählt.
    
  - **Löschen** Diese Option werden alle ausgewählten geräteprotokollkonfigurationen gelöscht.
    
- **Aktualisieren** Sie können Log Liste mit den Gerätekonfigurationen zum Überprüfen des Status der Optionen aller geräteprotokollkonfigurationen aktualisieren.
    
## <a name="see-also"></a>Siehe auch

#### 

[Ändern der Einstellungen für die Protokolldateien von Geräteupdates](http://technet.microsoft.com/library/9b57f126-1853-43b3-bbd4-06401e6498bd.aspx)
