---
title: Mobiler Client Pushbenachrichtigungskonfiguration
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.lscp.ClientPushNotificationCfgMain
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: b7a85d75-9d36-4980-b669-2a009799d905
description: Um die Microsoft-Pushbenachrichtigungen und Apple-Pushbenachrichtigungen zu konfigurieren, müssen Sie eine Richtlinie definieren, welche Arten von Pushbenachrichtigungen Sie benötigen, um erstellen.
ms.openlocfilehash: 946e083ab9f3f4dbc2b59f7f3026ec3a6dd5ed19
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="mobile-client-push-notification-configuration"></a>Mobiler Client: Konfiguration für Pushbenachrichtigung
 
Um die **Microsoft-Pushbenachrichtigungen** und **Apple-Pushbenachrichtigungen**zu konfigurieren, müssen Sie eine Richtlinie definieren, welche Arten von Pushbenachrichtigungen benötigten erstellen.
  
Klicken Sie auf dem Bildschirm Hauptelemente der Konfiguration **zu aktualisieren** , um zu aktualisieren und erneutes Auffüllen die Liste der Richtlinien. Ein Suchfeld wird zum Einschränken der Liste der angezeigten Richtlinien bereitgestellt. Während der Eingabe des Namens, dem Sie für Durchsuchen wird automatisch die Liste der Richtlinien eingeschränkt.
  
> [!IMPORTANT]
> Richtlinieneinstellungen, die auf einer bestimmten Richtlinienebene angewendet werden, können durch Einstellungen überschrieben werden, die auf einer anderen Richtlinienebene angewendet werden. Dabei gilt folgende Rangfolge: Benutzerrichtlinien (größter Einfluss) überschreiben Standortrichtlinien und diese überschreiben wiederum globale Richtlinien (geringster Einfluss). Mit anderen Worten: Je geringer der Abstand zwischen Richtlinieneinstellung und betroffenem Objekt, desto stärker der Einfluss auf das Objekt. 
  
Es sind zwei Auswahlmöglichkeiten für die Richtlinie für die Erstellung und Bearbeitung zur Verfügung:
  
1. **Neu**: Klicken Sie zum Erstellen einer neuen Richtlinie. Geben Sie eine Website für die Richtlinie zuweisen. Sie konfigurieren, klicken Sie dann die Einstellungen für die Pushbenachrichtigung. **Pushbenachrichtigungskonfiguration**können Sie nur Richtlinien für Websites erstellen, die Sie bereits erstellt haben.
    
2. **Bearbeiten**: Wählen Sie eine Richtlinie aus, und klicken Sie auf Bearbeiten, um eine Aktion in einem Dropdown-Liste auswählen. Sie können Websites nur, dass Sie bereits erstellt haben, oder bearbeiten die globale Richtlinie bearbeiten:
    
  - **Details anzeigen**: Zeigt Informationen über die aktuell ausgewählten Richtlinie. Sie werden können so ändern Sie die vorhandene Richtlinie.
    
  - **Wählen Sie alle**: Wenn Sie eine von Richtlinien Anzahl und alle Richtlinien auswählen möchten, klicken Sie auf Alles markieren
    
  - **Löschen**: die ausgewählte Richtlinie entfernt. Mithilfe von **Alles markieren** und **Löschen** werden alle Richtlinien entfernt.
    
    > [!NOTE]
    > Die Standardrichtlinie **Global** kann nicht gelöscht werden. Wenn Sie versuchen, ihn zu löschen, werden Sie benachrichtigt, dass die globale Richtlinie auf die Standardwerte zurückgegeben wurde (d. h., alle Einstellungen werden deaktiviert), aber die Richtlinie kann nicht entfernt werden.
  
Eine neue Richtlinie erstellen oder Bearbeiten einer vorhandenen Richtlinie gibt es zwei Aktionen:
  
- **Commit ausführen** Dieser Aktion erstellt oder aktualisiert die Richtlinie und speichert die Änderungen
    
- **Abbrechen** Die Aktion abbrechen verwirft alle Änderungen, die seit der letzten Commit-Aktion vorgenommen wurden. Wenn Sie abbrechen möchten, gehen alle vorgenommenen Änderungen verloren.
    
Es sind zwei Einstellungen für **Pushbenachrichtigungskonfiguration**möglich. Die Einstellungen sind der Push-Notification-Services für Microsoft und Apple zugeordnet. Aktivieren Sie Pushbenachrichtigungen für einen der Dienste, indem Sie das Kontrollkästchen neben dem Namen des Diensts auswählen. Sie können das Kontrollkästchen deaktivieren, indem Sie ihn deaktivieren sie die Option auswählen. Nachdem Sie Ihre Auswahl getroffen haben, Sie entweder einen commit oder abzubrechen. Klicken Sie dann auf Commit wird die Änderungen an der Richtlinie zu speichern.
  
