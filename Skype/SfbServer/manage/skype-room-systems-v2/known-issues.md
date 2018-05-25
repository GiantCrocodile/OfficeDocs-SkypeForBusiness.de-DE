---
title: Bekannte Probleme
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 4/17/2018
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
description: In diesem Artikel werden bekannte Probleme bei Skype Raum Systemen v2 aktuellen Branch Versionen.
ms.openlocfilehash: 9214a1b198431decda70687d7e1dd3aa08069554
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="known-issues"></a>Bekannte Probleme 
 
In diesem Artikel werden die bekannten Probleme für Skype Raum Systemen v2 nach Funktionsbereich.
<!-- If we get word that one of these issues no longer applies, contact meerak@microsoft.com or msmets@microsoft.com and let them know to EoL the corresponding KB  -->

<a name="update"></a> ## Update 

| Problemtitel |  Verhalten \/ Symptom | Abhilfe | KB-Artikel |
|  ---        |      ---             |   ---            | --- |
|  App veraltete         |    Die Skype Raum Systemen v2-Konsole zeigt einen "veraltet System Config".                |   [Verwenden Sie das Skype Raum Systemen v2 Recovery-tool](recovery-tool.md)             |  Keine |


<a name="OS-conflicts"> </a>  
## <a name="user-interface"></a>Benutzeroberfläche 

| Problemtitel |  Verhalten \/ Symptom | Abhilfe | KB-Artikel |
|  ---        |      ---             |   ---            | --- |
|Fehlende virtuelle Tastatur   | Virtuelle Tastatur wird nicht angezeigt, wenn Sie Informationen in Skype Raum Systemen v2 eingeben müssen. Dieses Problem tritt auf, nachdem das Windows 10 Ersteller Update (Version 1703) unter Surface Pro 4 installiert ist, auf dem Skype Raum Systemen v2 ausgeführt wird. | Um dieses Problem zu umgehen, öffnen Sie manuell virtuelle Tastatur. Gehen Sie hierzu folgendermaßen vor:<br><br> **1.** Tippen Sie und halten Sie den Vorgangsbalken, und tippen Sie dann auf die Schaltfläche **Show Bildschirmtastatur** . Ein Tastatursymbol sollte auf der rechten Seite des Vorgangsbalkens angezeigt werden. <br><br> **2.** Tippen auf der Tastatursymbol, um die virtuelle Tastatur zu öffnen. | [KB4037694](https://support.microsoft.com/en-us/help/4037694/virtual-keyboard-missing-in-skype-room-systems-v2) | 
   

<a name="Hardware"> </a>  
## <a name="hardware"></a>Hardware

| Problemtitel |  Verhalten \/ Symptom | Abhilfe | KB-Artikel |
|  ---        |      ---             |   ---            |   --- |
| Monitore nicht erkannt | Wenn Sie Skype Raum Systemen v2 auf einem Gerät Surface Pro (Modell 2017) ausführen, werden die Monitore nicht erkannt. |  Halten Sie die Surface Pro Power mindestens 20 Sekunden lang. Wenn Sie dies tun, wird das Gerät neu gestartet, und löscht den Cache Grafiken. |[KB4055681](https://support.microsoft.com/en-us/help/4055681/monitors-are-not-detected-when-you-run-skype-room-systems-on-a-surface)       | 
          
<a name="Limits"> </a>
## <a name="limitations-and-expected-behaviors"></a>Einschränkungen und erwartetes Verhalten
***
Skype Raum Systemen v2 HDCP-Eingang festgestellten Probleme mit HDMI verursacht wurde, nicht unterstützt werden Aufnahme Funktionalität (Video, audio). Achten Sie darauf, dass Switches angeschlossen Skype Raum Systemen V2 HDCP-Optionen deaktiviert aufweisen. 
***
Ein Consumer TV als Front Raum Anzeige Anforderungen für den Support/HDMI das Consumer Electronics Steuerelement (CEC)-Feature aktivieren, damit er automatisch an eine aktive Bildquelle aus dem Standbymodus wechseln kann. Dieses Feature wird auf alle TV-Geräte nicht unterstützt. 
***
Verwenden Sie immer eine drahtgebundene 1 Gbit/s-Netzwerk-Verbindung, um sicherzustellen, dass Sie die erforderliche Bandbreite verfügen. 
***
Wenn Ihre Skype Raum Systemen v2-Gerät verliert Vertrauensstellung mit der Domäne (beispielsweise, wenn Sie die Skype Raum Systemen v2 aus der Domäne entfernen, nach der Domäne beigetreten ist), werden nicht Sie an das Gerät authentifizieren und Einstellungen zu öffnen. Zur Problemumgehung können Sie sich mit dem lokalen Administratorkonto anmelden. 
***
Die 64-Bit-Version von Windows 10 Enterprise Jahrestag Edition (englische, Version 1607) wird nicht mehr Skype Raum Systemen v2 Version 3.0.12.0 (Update 3) unterstützt. 
***

<a name="See"> </a>  
## <a name="see-also"></a>Waren diese Schritte hilfreich? Wenn ja, teilen Sie uns dies bitte unterhalb des Artikels mit. Wenn nicht, schreiben Sie uns, was für Sie unklar war, und wir verwenden Ihr Feedback, um unsere Schritte zu überprüfen.


#### 
[Skype Raum Systeme Version 2-Hilfe](https://support.office.com/en-us/article/Skype-Room-Systems-version-2-help-e667f40e-5aab-40c1-bd68-611fe0002ba2)

[Verwalten von Skype Raum Systemen v2](skype-room-systems-v2.md)