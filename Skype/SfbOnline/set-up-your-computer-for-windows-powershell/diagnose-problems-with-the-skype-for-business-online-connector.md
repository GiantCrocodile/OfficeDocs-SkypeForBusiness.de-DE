---
title: Diagnostizieren von Verbindungsproblemen mit dem Skype for Business Online-Connector
ms.reviewer: ''
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.topic: article
ms.assetid: 866fadfd-16e2-4134-95db-c6aed7678416
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
search.appverid: MET150
ms.collection: Adm_Skype4B_Online
audience: Admin
appliesto:
- Skype for Business
localization_priority: Normal
f1.keywords:
- NOCSH
ms.custom:
- PowerShell
description: Problembehandlung beim Erstellen einer Remote-PowerShell-Sitzung zum Herstellen einer Verbindung mit Skype for Business Online, einschließlich Import Modul, paralleler Shell, Live-ID und Berechtigungsfehlern.
ms.openlocfilehash: 019ef023b325227be046aae1e855573449453864
ms.sourcegitcommit: 693205da865111380b55c514955ac264031eb2fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2020
ms.locfileid: "44204876"
---
# <a name="diagnose-connection-problems-with-the-skype-for-business-online-connector"></a>Diagnostizieren von Verbindungsproblemen mit dem Skype for Business Online-Connector

Dieses Thema enthält Informationen, die Ihnen helfen sollen, Probleme zu diagnostizieren und zu beheben, die beim Versuch auftreten können, eine Microsoft PowerShell-Remotesitzung zu erstellen, die eine Verbindung mit Skype for Business Online herstellt. Lesen Sie die folgenden Abschnitte:
  
- [„Import-Module"-Fehler aufgrund der Windows PowerShell-Ausführungsrichtlinie](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKPowerShellExecutionPolicy)
    
- [„Import-Module"-Fehler aufgrund einer falschen Version von Windows PowerShell](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKIncorrectVersion)
    
- [Die moderne Authentifizierung schlägt fehl, wenn die WinRM-Standardauthentifizierung deaktiviert wurde.](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKWinRMBasicAuth)
    
- [Fehler beim Herstellen der Verbindung mit dem Live ID-Server](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKFailedConnect)
    
- [Fehler beim Laden des Live ID-Moduls](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKFailedLoad)
    
- [Fehler bei der Anmeldung des Benutzers](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKLogonFailed)
    
- [Der Benutzer verfügt nicht über die Berechtigung zum Verwalten dieses Mandanten](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKUserPermission)
    
- [Die Möglichkeit, Verbindungen mit dem Mandanten herzustellen, wurde in Skype for Business Online deaktiviert](diagnose-problems-with-the-skype-for-business-online-connector.md#BKMKAbilityConnect)
    
- [Die maximale Anzahl von gleichzeitigen Shells für diesen Benutzer in Skype for Business Online wurde überschritten](#the-maximum-number-of-concurrent-shells-for-this-user-in-skype-for-business-online-has-been-exceeded)

- [Die maximale Anzahl von gleichzeitigen Shells für diesen Mandanten in Skype for Business Online wurde überschritten](#the-maximum-number-of-concurrent-shells-for-this-tenant-in-skype-for-business-online-has-been-exceeded)
    

> [!IMPORTANT]
> Standardmäßig sind PowerShell-Sitzungen nach 60 Minuten Timeout. Um die Verbindung wiederherzustellen, müssen Sie die Sitzung schließen und eine neue PowerShell-Sitzung starten. Eine neue Version von [Skype for Business Online, dem Windows PowerShell-Modul (2046,123-veröffentlicht 10/2/2019)](https://www.microsoft.com/download/details.aspx?id=39366), wurde kürzlich gestartet, das ein neues Cmdlet namens **enable-CsOnlineSessionForReconnection** enthält, das das Timeout Problem von 60 Minuten verringert.
> Die PowerShell-Sitzung wird erneut verbunden und authentifiziert, sodass Sie wieder verwendet werden kann, ohne dass eine neue Instanz gestartet werden muss, um erneut eine Verbindung herzustellen.



## <a name="import-module-error-caused-by-windows-powershell-execution-policy"></a>„Import-Module"-Fehler aufgrund der Windows PowerShell-Ausführungsrichtlinie
<a name="BKMKPowerShellExecutionPolicy"> </a>

Mithilfe der PowerShell-Ausführungsrichtlinie kann ermittelt werden, welche Konfigurationsdateien in der PowerShell-Konsole geladen werden können und welche Skripts ein Benutzer über diese Konsole ausführen kann. Dabei gilt mindestens, dass das Skype for Business Online-Connectormodul nur importiert werden kann, wenn die Ausführungsrichtlinie auf „RemoteSigned" festgelegt ist. Wenn dies nicht der Fall ist, erhalten Sie beim Versuch, das Modul zu importieren, die folgende Fehlermeldung:
  
- **Fehler**: <em>Import-Module: Datei C: \\ Programmdateien \\ Allgemeine Dateien \\ Microsoft lync Server 2013 \\ \\ -Module LyncOnlineConnector \\ LyncOnlineConnectorStartup. psm1 können nicht geladen werden, weil ausgeführte Skripts auf diesem System deaktiviert sind. Weitere Informationen finden Sie unter about_Execution_Policies https://go.microsoft.com/fwlink/?LinkID=135170 .</em>

- **Auflösung** Um dieses Problem zu beheben, starten Sie PowerShell als Administrator, und führen Sie dann den folgenden Befehl aus:
    ```PowerShell
    Set-ExecutionPolicy RemoteSigned
    ```
    Details zur Ausführungsrichtlinie finden Sie unter [Informationen zu Ausführungsrichtlinien](https://go.microsoft.com/fwlink/?LinkID=135170).
  
## <a name="import-module-error-caused-by-incorrect-version-of-windows-powershell"></a>„Import-Module"-Fehler aufgrund einer falschen Version von Windows PowerShell
<a name="BKMKIncorrectVersion"> </a>

Das Skype for Business Online-Connectormodul kann nur in Windows PowerShell 3.0 ausgeführt werden. Beim Versuch, das Modul in einer früheren Version von PowerShell auszuführen, tritt beim Importprozess ein Fehler auf, und etwa die folgende Fehlermeldung wird angezeigt:
  
  - **Fehler**: *Import-Module: die Version der geladenen PowerShell lautet "2,0". Das Modul 'd: \\ Programmdateien \\ Allgemeine Dateien \\ Microsoft lync Server 2013 \\ \\ -Module LyncOnlineConnector \\ LyncOnlineConnector. psd1 ' erfordert eine minimale PowerShell-Version von ' 3,0 ', die ausgeführt werden soll. Überprüfen Sie die Installation der PowerShell, und versuchen Sie es erneut.*

- **Lösung**: die einzige Möglichkeit, dieses Problem zu beheben, besteht darin, Windows PowerShell 3,0 zu installieren, die im Microsoft Download Center unter verfügbar ist [https://www.microsoft.com/download/details.aspx?id=34595](https://www.microsoft.com/download/details.aspx?id=34595) .
  
## <a name="modern-authentication-fails-when-winrm-basic-authentication-has-been-disabled"></a>Die moderne Authentifizierung schlägt fehl, wenn die WinRM-Standardauthentifizierung deaktiviert wurde.
<a name="BKMKWinRMBasicAuth"> </a>

Die aktuelle Version des Skype for Business Online-Connector-Moduls verwendet eine moderne Authentifizierung, aber der zugrunde liegende Windows-Remote Verwaltungsclient (WinRM) muss so konfiguriert sein, dass die Standardauthentifizierung zugelassen wird.  Bei der modernen Authentifizierung werden Inhaber Token verwendet, die normalerweise in der *Autorisierung: Bearer* -Kopfzeile übergeben werden. Windows PowerShell, auf der Skype for Business PowerShell aufbaut, ermöglicht keine Manipulation dieser Kopfzeile.  Stattdessen verwendet Skype for Business PowerShell den *Authorization: Basic* -Header, um das Inhaber Token zu übergeben.

Anweisungen zum Aktivieren von WinRM für die Standardauthentifizierung finden Sie unter [herunterladen und Installieren von Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/download-and-install-windows-powershell-5-1) .

## <a name="failed-to-connect-to-live-id-server"></a>Fehler beim Herstellen der Verbindung mit dem Live ID-Server
<a name="BKMKFailedConnect"> </a>

Es gibt drei typische Gründe, aus denen beim Verbindungsversuch Fehler auftreten und die folgende Fehlermeldung angezeigt wird:

  - **Fehler**: *Get-CsWebTicket: Fehler beim Verbinden von Live ID-Servern. Stellen Sie sicher, dass Proxy aktiviert ist oder Computer über eine Netzwerkverbindung mit Live ID-Servern verfügt.*

- **Lösung**: häufig bedeutet dieser Fehler, dass der Microsoft Online Services-Anmelde-Assistent nicht ausgeführt wird. Sie können den Status dieses Diensts überprüfen, indem Sie an der PowerShell-Eingabeaufforderung den folgenden Befehl ausführen: 
    ```PowerShell
    Get-Service "msoidsvc"
    ```
    Wenn der Dienst nicht ausgeführt wird, starten Sie ihn mit diesem Befehl:
    ```PowerShell
    Start-Service "msoidsvc"
    ```

    Wenn der Dienst ausgeführt wird, bestehen möglicherweise Probleme mit der Netzwerkverbindung zwischen Ihrem Computer und dem Microsoft Live ID-Authentifizierungsserver. Überprüfen Sie dies, indem Sie Internet Explorer öffnen und zu [https://login.microsoftonline.com/](https://login.microsoftonline.com/.) navigieren. Versuchen Sie, sich von dort aus an Microsoft 365 oder Office 365 anzumelden. Wenn dabei ein Fehler auftritt, liegen wahrscheinlich Probleme mit der Netzwerkverbindung vor.
  
    Eine weniger häufige Möglichkeit: Der Verbindungs-URI für den Microsoft Live ID-Authentifizierungsserver ist mit einem falschen Wert konfiguriert. Wenn Sie bereits festgestellt haben, dass der Anmeldeassistent ausgeführt wird und dass keine Probleme mit der Netzwerkkonnektivität vorliegen, kann dies die Ursache sein. Wenden Sie sich in diesem Fall an den Microsoft-Support.
  
## <a name="failed-to-load-live-id-module"></a>Fehler beim Laden des Live ID-Moduls
<a name="BKMKFailedLoad"> </a>

Als eine der Voraussetzungen für die Verwendung von PowerShell zum Verwalten von Skype for Business Online muss der Microsoft Online Services-Anmeldeassistent installiert sein. Wenn der Anmeldeassistent nicht installiert ist, erhalten Sie beim Versuch, eine Remotesitzung mit Skype for Business Online einzurichten, die folgende Fehlermeldung:

- **Fehler**: *Get-CsWebTicket: kann das Live ID-Modul nicht laden. Stellen Sie sicher, dass die richtige Version des Live ID-Anmelde-Assistenten installiert ist.*

- **Lösung**: der Microsoft Online Services-Anmelde Assistent steht im Microsoft Download Center des [Microsoft Online Services-Anmelde Assistenten für IT-Experten](https://www.microsoft.com/download/details.aspx?id=28177) zur Verfügung RTW

## <a name="logon-failed-for-the-user"></a>Fehler bei der Anmeldung des Benutzers
<a name="BKMKLogonFailed"> </a>

Wenn Sie versuchen, eine Remoteverbindung mit Skype for Business Online herzustellen, müssen Sie den Benutzernamen und das Kennwort eines gültigen Skype for Business Online-Benutzerkontos angeben. Anderenfalls tritt bei der Anmeldung ein Fehler auf, und etwa die folgende Fehlermeldung wird angezeigt:

- **Fehler**: *Get-CsWebTicket: die Anmeldung für den Benutzer "kenmyer@litwareinc.com" ist fehlgeschlagen. Erstellen Sie ein neues PSCredential-Objekt, indem Sie sicherstellen, dass Sie den richtigen Benutzernamen und das richtige Kennwort verwendet haben.*

- **Lösung**: Wenn Sie der Meinung sind, dass Sie ein gültiges Benutzerkonto verwenden und dass Sie über das richtige Kennwort verfügen, versuchen Sie erneut, sich anzumelden. Wenn dabei ein Fehler auftritt, versuchen Sie mit den gleichen Anmeldeinformationen, sich unter [https://login.microsoftonline.com/](https://login.microsoftonline.com/) anzumelden. Wenn Sie sich dort nicht anmelden können, wenden Sie sich an den Microsoft-Support. 

  
## <a name="the-user-does-not-have-permission-to-manage-this-tenant"></a>Der Benutzer verfügt nicht über die Berechtigung zum Verwalten dieses Mandanten
<a name="BKMKUserPermission"> </a>

Sie müssen Mitglied der Gruppe „Mandantenadministratoren" sein, um eine PowerShell-Remoteverbindung mit Skype for Business Online herzustellen. Wenn dies nicht der Fall ist, tritt beim Verbindungsversuch ein Fehler auf, und die folgende Fehlermeldung wird angezeigt:

- **Fehler**: *"New-PSSession: [admin.vdomain.com]" beim Verarbeiten von Daten aus dem Remoteserver admin.vdomain.com Fehler mit der folgenden Fehlermeldung: der Benutzer "User@foo.com" verfügt nicht über die Berechtigung zum Verwalten dieses Mandanten. Berechtigungen können gewährt werden, indem der Benutzer der entsprechenden RBAC-Rolle zugewiesen wird. Weitere Informationen finden Sie auf der [Remote Problembehandlung](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_remote_troubleshooting?view=powershell-5.1).*

- **Lösung**: Wenn Sie der Meinung sind, dass Sie ein Mitglied der Gruppe der mandantenadministratoren sind oder sein sollten, müssen Sie sich an den Microsoft-Support wenden.
  
## <a name="ability-to-connect-to-tenant-has-been-disabled-in-skype-for-business-online"></a>Die Möglichkeit, Verbindungen mit dem Mandanten herzustellen, wurde in Skype for Business Online deaktiviert
<a name="BKMKAbilityConnect"> </a>

Damit Sie PowerShell mit Skype for Business Online verwalten können, muss die „EnableRemotePowerShellAccess"-Eigenschaft Ihrer PowerShell-Mandantenrichtlinie auf  `True` festgelegt sein. Wenn dies nicht der Fall ist, tritt bei der Verbindung ein Fehler auf, und die folgende Fehlermeldung wird angezeigt:

- **Fehler**: *"New-PSSession: [admin.vdomain.com]" beim Verarbeiten von Daten aus dem Remoteserver admin.vdomain.com Fehler mit der folgenden Fehlermeldung: die Möglichkeit zum Herstellen einer Verbindung mit diesem Mandanten mithilfe einer Remote-PowerShell-Sitzung wurde deaktiviert. Bitte wenden Sie sich an die lync-Hilfe, um die Mandanten-PowerShell-Richtlinie dieses Mandanten Weitere Informationen finden Sie auf der [Remote Problembehandlung](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_remote_troubleshooting?view=powershell-5.1).*

- **Lösung**: Wenn diese Fehlermeldung angezeigt wird, müssen Sie sich an den Microsoft-Support wenden, um den Remote-PowerShell-Zugriff zu aktivieren.
  
## <a name="the-maximum-number-of-concurrent-shells-for-this-user-in-skype-for-business-online-has-been-exceeded"></a>Die maximale Anzahl von gleichzeitigen Shells für den Benutzer in Skype for Business Online wurde überschritten
<a name="BKMKMaxNumberShellsUser"> </a>

Jeder Administrator darf maximal drei gleichzeitige Remoteverbindungen mit Skype for Business Online herstellen. Wenn drei PowerShell-Remoteverbindungen aktiv sind, tritt beim Versuch, eine vierte gleichzeitige Verbindung herzustellen, ein Fehler auf. Dabei wird die folgende Fehlermeldung angezeigt:

- **Fehler**: *New-PSSession: [admin.vdomain.com] Verbindung mit dem Remoteserver admin.vdomain.com fehlgeschlagen mit der folgenden Fehlermeldung: der WS-Verwaltungsdienst kann die Anforderung nicht verarbeiten. Die maximale Anzahl von gleichzeitigen Shells für diesen Benutzer wurde überschritten. Schließen Sie vorhandene Shells, oder erhöhen Sie das Kontingent für diesen Benutzer. Weitere Informationen finden Sie unter [Remote Troubleshooting] ( https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_remote_troubleshooting?view=powershell-5.1 *

- **Lösung**: die einzige Möglichkeit, dieses Problem zu beheben, besteht darin, mindestens eine der vorherigen Verbindungen zu schließen. Wenn Sie mit einer Skype for Business Online-Sitzung fertig sind, sollten Sie die Sitzung mit dem Cmdlet **Remove-PSSession** beenden. Damit können Sie das Problem vermeiden.
  
## <a name="the-maximum-number-of-concurrent-shells-for-this-tenant-in-skype-for-business-online-has-been-exceeded"></a>Die maximale Anzahl von gleichzeitigen Shells für den Mandanten in Skype for Business Online wurde überschritten
<a name="BKMKMaxNumberShellsTenant"> </a>

Obwohl für jeden Administrator maximal drei gleichzeitige Verbindungen mit einem Skype for Business Online-Mandanten zulässig sind, darf kein einzelner Mandant mehr als 20 gleichzeitige Verbindungen haben. So haben beispielsweise sechs Administratoren jeweils drei offene Sitzungen. Wenn ein vierter Administrator versucht, mehr als 2 Verbindungen zu erstellen (wodurch insgesamt 21 gleichzeitige Verbindungen entstehen), schlägt dieser Versuch mit der folgenden Fehlermeldung fehl:
  
- **Fehler**: *New-PSSession: [admin.vdomain.com] Verbindung mit dem Remoteserver admin.vdomain.com fehlgeschlagen mit der folgenden Fehlermeldung: der WS-Verwaltungsdienst kann die Anforderung nicht verarbeiten. Die maximale Anzahl von gleichzeitigen Shells für diesen Mandanten wurde überschritten. Schließen Sie vorhandene Shells, oder heben Sie das Kontingent für diesen Mandanten auf. Weitere Informationen finden Sie unter [Remote Troubleshooting] ( https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_remote_troubleshooting?view=powershell-5.1 *

- **Lösung**: die einzige Möglichkeit, dieses Problem zu beheben, besteht darin, mindestens eine der vorherigen Verbindungen zu schließen. Wenn Sie mit einer Skype for Business Online-Sitzung fertig sind, sollten Sie die Sitzung mit dem Cmdlet **Remove-PSSession** beenden. Damit können Sie das Problem vermeiden.  
 
## <a name="related-topics"></a>Verwandte Themen
[Einrichten Ihres Computers für die Skype for Business Online-Verwaltung mithilfe von Windows PowerShell](set-up-your-computer-for-windows-powershell.md)

  
 
