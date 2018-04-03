---
title: Bereitstellen des Lync VDI-Plug-Ins in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 11d3bd5d-6dd3-471c-b842-b072fa197714
description: In diesem Thema wird die Bereitstellungsverfahren für die Verwendung von Skype für Unternehmen beim Herstellen einer Verbindung mit einem virtuellen Remotedesktop.
ms.openlocfilehash: a8f95903f3c06fd953b8d97ba829d4f23e8d72b6
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="deploy-the-lync-vdi-plug-in-with-skype-for-business-server-2015"></a>Bereitstellen des Lync VDI-Plug-Ins in Skype for Business Server 2015
 
In diesem Thema wird die Bereitstellungsverfahren für die Verwendung von Skype für Unternehmen beim Herstellen einer Verbindung mit einem virtuellen Remotedesktop. 
  
Eine VDI-Umgebung (Virtual Desktop Infrastructure) wird in einigen Organisationen verwendet, in denen Sicherheits- und Complianceprobleme besonders sensibel sind. Die Benutzer arbeiten mit lokalen Windows-Computern und verwenden Clients auf einem virtuellen Desktop. Verwendung von Skype für Unternehmen für eine Verbindung auf dem erfordert zusätzlichen VDI-Plug-in-Software.
  
Ihnen stehen zwei Methoden zur Verfügung, für die VDI-Plug-in-Komponente - eine Angeboten von Microsoft und eine von Citrix angeboten. Microsoft empfiehlt die Verwendung der neuen HDX-Echtzeit Optimization Pack-Lösung in neuen Bereitstellungen ist jedoch weiterhin die ursprünglichen Lync VDI-Plug-In für den Rest des Lebenszyklus zu unterstützen. 
  
Dieses Thema enthält Details zum Bereitstellen des Microsoft Lync VDI-Plug-in, wodurch wird nur unter Windows 7 und Windows 8 oder Windows Server 2008 unterstützt, und unterstützt nur Lync 2013 oder Skype für Business 2015 Clients. Es ist nicht geplant, dieses Plug-in aktualisieren, aber die [Citrix HDX-Echtzeit Optimization Pack](../../plan-your-deployment/clients-and-devices/vdi-environments.md#Citrix_RT) für Skype für Unternehmen wird aktualisiert werden, je nach Bedarf.
  
## <a name="prepare-your-environment-for-the-lync-vdi-plug-in"></a>Vorbereiten Ihrer Umgebung für das Lync VDI-Plug-In
<a name="Prepare_vdi"> </a>

1. Skype für Business Server 2015 sicher, dass für alle Lync-VDI-Plug-in-Benutzer EnableMediaRedirection auf TRUE festgelegt ist. Weitere Informationen hierzu finden Sie unter der Themen der Onlinehilfe für das Cmdlet [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/new-csclientpolicy?view=skype-ps) und [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/set-csclientpolicy?view=skype-ps) -Cmdlet.
    
2. Installieren Sie auf dem Data Center-Server der Skype für Business 2015-Client auf allen virtuellen Desktops.
    
3. Installieren Sie auf den lokalen Computern das Lync VDI-Plug-in.
    
    Die Benutzer sollten jetzt ein Gerät wie etwa ein Headset oder eine Webcam mit ihrem lokalen Computer verbinden.
    
## <a name="configure-remote-desktop-connection-settings"></a>Konfigurieren von Einstellungen der Remotedesktopverbindung
<a name="Prepare_vdi"> </a>

Zur Vorbereitung von Remotedesktopverbindung für das Lync VDI-Plug-in auf dem lokalen Computer folgendermaßen Sie vor:
  
1. Wenn auf der lokale Computer Windows 8 ausgeführt wird, überspringen Sie diesen Schritt. Wenn auf der lokale Computer Windows 7 mit SP1 ausgeführt wird, installieren Sie die neueste Version von Windows 8 des [Remote Desktop Services Client](https://go.microsoft.com/fwlink/p/?LinkId=268032).
    
2. Starten Sie den Remotedesktopdienste-Client, indem Sie auf **Start** und dann auf **Remotedesktopverbindung** klicken.
    
3. Klicken Sie auf **Optionen**.
    
4. Klicken Sie auf die Registerkarte **Lokale Ressourcen**. Klicken Sie unter **Remoteaudio** auf **Einstellungen**, und gehen Sie wie folgt vor:
    
  - Wählen Sie unter **Remoteaudiowiedergabe** die Option **Auf diesem Computer wiedergeben** aus.
    
  - Wählen Sie unter **Remoteaudioaufzeichnung** die Option **Nicht aufzeichnen** aus.
    
  - Klicken Sie anschließend auf **OK**.
    
5. Klicken Sie auf die Registerkarte **Erweitert**. Deaktivieren Sie unter **Leistung** das Kontrollkästchen **Dauerhafte Bitmapzwischenspeicherung**.
    
6. Klicken Sie auf die Registerkarte **Allgemein**. Geben Sie im Feld **Computer** den Namen des virtuellen Desktops ein, und klicken Sie dann auf **Verbinden**.  
    
## <a name="sign-in-and-use-skype-for-business-on-the-virtual-desktop"></a>Anmelden und Verwenden von Skype for Business auf dem virtuellen Desktop
<a name="SfB_signin"> </a>

Nachdem das Lync VDI-Plug-in aktiviert ist, gilt für den Benutzer folgende Schritte aus, wenn auf dem virtuellen Desktop Skype für Business 2015 anmelden.
  
1. Der Benutzer gibt seine Anmeldeinformationen für die Skype für Business 2015-Client auf dem virtuellen Desktop.
    
2. Nachdem das Lync VDI-Plug-in von Skype für Business 2015 erkannt hat, Skype für Business 2015 der Benutzer aufgefordert, die Anmeldeinformationen erneut eingeben. In diesem Dialogfeld sollten die Benutzer das Kontrollkästchen **Kennwort speichern** aktivieren, damit sie die Anmeldeinformationen bei folgenden Anmeldevorgängen nicht erneut eingeben müssen.
    
3. Skype für Business 2015 beginnt eine Kopplung mit der Lync-VDI-Plug-in. Während dies geschieht, zeigt der Client zwei Symbole an, in der Skype für Business 2015 Statusleiste. Das Symbol links unten zeigt an, dass keine Audiogeräte verfügbar sind, während das blinkende Symbol rechts unten signalisiert, dass die VDI-Kopplung gerade durchgeführt wird:
    4. Nach einer erfolgreichen VDI-Kopplung ändern sich die Symbole und zeigen nun das für Anrufe verwendete Audiogerät bzw. den Erfolg der VDI-Kopplung an:
    5. Der Benutzer kann jetzt seine Anwesenheit auf Skype für kompatible Geräte Business 2015 sehen, die mit dem lokalen Computer verbunden sind und Anrufe tätigen und entgegennehmen wie gewohnt.
    
## <a name="troubleshoot-the-lync-vdi-plug-in"></a>Problembehandlung für das Lync VDI-Plug-In
<a name="tshoot_VDI"> </a>

Lesen Sie die folgenden Abschnitte, wenn nach der Installation des Lync VDI-Plug-Ins Probleme auftreten.
  
### <a name="issues-with-installing-the-lync-vdi-plug-in"></a>Probleme beim Installieren des Lync VDI-Plug-Ins 

Wenn Probleme bei der Installation des Lync-VDI-Plug-in vorhanden sind, überprüfen Sie Folgendes:
  
- Stellen Sie sicher, dass in dem Ordner, den Sie in den Systemvariablen „TEMP“ und „TMP“ angegeben haben, ausreichend Speicherplatz vorhanden ist.
    
- Stellen Sie sicher, dass der Schreibschutz deaktiviert ist. Finden Sie in der Dokumentation des Herstellers.
    
### <a name="troubleshooting-issues-with-pairing"></a>Problembehandlung für die Kopplung

Wenn Lync-VDI-Plug-in eine Kopplung fehlschlägt, das paarungssymbol in der unteren rechten zeigt als rotes "X" als dargestellt: 
  
Nachfolgend finden Sie mögliche Gründe für Fehler und Maßnahmen, mit denen Sie das Problem korrigieren können.  
  
- **Die Benutzer haben bei der Anmeldung falsche Anmeldeinformationen eingegeben.**
    
    Der Benutzer sollte Abmelden bei Skype für Unternehmen und mit den richtigen Anmeldeinformationen erneut anmelden. Das Kopplungsdialogfeld wird erneut angezeigt und gibt an, ob die Kopplung erfolgreich war.
    
- **Eine andere Instanz des Remotedesktopclients wird bereits ausgeführt.**
    
    Wenn sie in Windows Remotedesktopverbindung verwenden, sollten die Benutzer Folgendes:
    
1. Starten Sie den Task-Manager: Drücken Sie **ALT+STRG+ENTF**, und klicken Sie dann auf **Task-Manager starten**.
    
2. Klicken Sie auf die Registerkarte **Prozesse**, und suchen Sie in der Liste nach allen Prozessen mit dem Namen **mstsc.exe**.
    
3. Markieren Sie alle **mstsc.exe**-Prozesse, und klicken Sie dann auf **Prozess beenden**.  
    
4. Starten Sie eine neue Remotedesktopsitzung, und versuchen Sie erneut, eine Verbindung herzustellen.  
    
- **Die erforderlichen Dateien wurden nicht ordnungsgemäß installiert.**
    
    Vergewissern Sie sich nach der Installation des Plug-Ins auf dem lokalen Computer, dass die folgenden Dateien in „C:\Programme\Microsoft Office\Office15“ (ändern Sie gegebenenfalls den Laufwerkbuchstaben) vorhanden sind:
    
  - LyncVdiPlugin.dll
    
  - UcVdi.dll
    
- **Die Skype für Business 2015-Client wird auf dem lokalen Computer ausgeführt.**
    
    Zum Verwenden des Lync-VDI-Plug-in, einen Skype für Business 2015 Client muss nicht auf dem lokalen Computer ausgeführt werden, schlägt fehl andernfalls eine Kopplung. Es empfiehlt sich sollte der Benutzer einen Skype für Business 2015 Client nicht auf dem lokalen Computer installieren.
    
## <a name="see-also"></a>Waren diese Schritte hilfreich? Wenn ja, teilen Sie uns dies bitte unterhalb des Artikels mit. Wenn nicht, schreiben Sie uns, was für Sie unklar war, und wir verwenden Ihr Feedback, um unsere Schritte zu überprüfen.
<a name="tshoot_VDI"> </a>

#### 

[Planen von Skype für Unternehmen in einer VDI-Umgebung](../../plan-your-deployment/clients-and-devices/vdi-environments.md)
