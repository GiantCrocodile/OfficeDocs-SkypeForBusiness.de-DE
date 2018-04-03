---
title: Registrierungseinstellungen – Erweiterung
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.tb.RegistrarSettingsExpander
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: c7486ab3-61fd-45c6-9edc-a15535f273ff
description: Resiliency bietet hohe Verfügbarkeit und Disaster Recovery für den registrierungspool an. Durch die Bereitstellung einer Sicherung Registrierung bei einem Ausfall der primären Registrierung, die Sicherung, die Registrierung für die fehlerhafte Registrierung übernehmen kann, können Benutzer anmelden und kommunizieren. Benutzer können potenziell mit eingeschränkter Funktionalität bemerken, je nachdem, welches Systeme mit die primäre Registrierungsstelle ausgefallen.
ms.openlocfilehash: 9d8460f0a883dfabc55153744ba4f3f886b34898
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="registrar-settings-expander"></a>Registrierungseinstellungen – Erweiterung
 
Resiliency bietet hohe Verfügbarkeit und Disaster Recovery für den registrierungspool an. Durch die Bereitstellung einer Sicherung Registrierung bei einem Ausfall der primären Registrierung, die Sicherung, die Registrierung für die fehlerhafte Registrierung übernehmen kann, können Benutzer anmelden und kommunizieren. Benutzer können potenziell mit eingeschränkter Funktionalität bemerken, je nachdem, welches Systeme mit die primäre Registrierungsstelle ausgefallen.
  
Im Abschnitt **Ausfallsicherheit** des Dialogfelds **Eigenschaften bearbeiten** für den Survivable Branch Appliance oder einen Survivable Branch Server können Sie die folgenden Einstellungen ändern:
  
- **Zugeordneter Benutzerdienst und Sicherungsregistrierungsstellen-pool** Wählen Sie in der Dropdownliste den Enterprise Edition-Front-End-Pool oder Standard Edition-Front-End-Server, der als sicherungsregistrierung für die Survivable Branch Appliance oder einen Survivable Branch Server fungieren.
    
- **Aktivieren von Failover und Failback** Wählen Sie diese Einstellung, um für die automatische Erkennung von einem fehlgeschlagenen zulassen, Registrierung und die automatische Ermittlung, der die primäre Registrierung sichern und Fortsetzen des Prozesses Registrierung bereit ist.
    
- **Fehler bei Erkennung Intervall (s)** Geben Sie die Anzahl der Sekunden an, die vergehen soll, bevor er bestimmt wird, dass die primäre Registrierungsstelle ausgefallen ist. Der Standardwert ist 120 Sekunden. Dieses Feld ist erforderlich, wenn Sie **Aktivieren Failover und Failback**auswählen.
    
- **Fallback Erkennung Intervall (s)** Geben Sie die Anzahl der Sekunden an, die vergehen soll, bevor festgestellt wird, das die primäre Registrierungsstelle gesichert wird. Der Standardwert ist 240 Sekunden. Dieses Feld ist erforderlich, wenn Sie **Failover aktivieren und Fallback**auswählen.
    
> [!IMPORTANT]
> Wenn Sie das Intervall der Ausfall Erkennung und das Intervall fallback Erkennung definieren, werden Sie nicht, die ein Intervall angeben, der bewirkt das Failover und fallback eintritt, wenn die Registrierung nicht für ein kurzer Zeit reagiert. Es ist möglich, dass die primäre Registrierung für einen kurzen Zeitraum basierend auf das Laden des Pools oder Servern nicht reagieren kann. 
  
