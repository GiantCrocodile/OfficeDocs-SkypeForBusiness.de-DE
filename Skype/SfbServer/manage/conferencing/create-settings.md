---
title: Erstellen von Einstellungen für die besprechungskonfiguration in Skype for Business Server
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: 6d8f9ff8-2a04-4175-9bf0-1ec5d78fd015
description: 'Zusammenfassung: Hier erfahren Sie, wie Sie die Einstellungen für die besprechungskonfiguration in Skype for Business Server erstellen.'
ms.openlocfilehash: cd3d207816f352a33fb3fd228e7249d9e5d836b3
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41818606"
---
# <a name="create-meeting-configuration-settings-in-skype-for-business-server"></a>Erstellen von Einstellungen für die besprechungskonfiguration in Skype for Business Server
 
**Zusammenfassung:** Hier erfahren Sie, wie Sie in Skype for Business Server Besprechungs Konfigurationseinstellungen erstellen.
  
Sie können die Einstellungen für die besprechungskonfiguration über die Skype for Business Server-Systemsteuerung oder über die Skype for Business Server-Verwaltungsshell erstellen.
  
## <a name="create-meeting-configuration-settings-by-using-skype-for-business-server-control-panel"></a>Erstellen von Einstellungen für die besprechungskonfiguration mithilfe der Skype for Business Server-Systemsteuerung

1. Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.
    
2.  Öffnen Sie die Skype for Business Server-Systemsteuerung.
    
3. Klicken Sie in der linken Navigationsleiste auf **Konferenzen** und anschließend auf **Besprechungskonfiguration**.
    
4. Klicken Sie auf der Seite **Besprechungskonfiguration** auf **Neu** und führen Sie eine der folgenden Aktionen aus:
    
    - Klicken Sie auf **Standortkonfiguration**, um eine Richtlinie auf Standortebene zu erstellen. Geben Sie im Suchfeld **Standort auswählen** einen Teil oder den gesamten Namen des Standorts ein, für den Sie Einstellungen für den Besprechungsbeitritt definieren möchten. Klicken Sie in der resultierenden Liste der Standorte auf den gewünschten Standort und klicken Sie auf **OK**.
    
    - Klicken Sie auf **Poolkonfiguration**, um eine Richtlinie auf Poolebene zu erstellen. Geben Sie im Suchfeld **Dienst auswählen** einen Teil oder den gesamten Namen des Pooldienstes ein, für den Sie Einstellungen für den Besprechungsbeitritt definieren möchten. Klicken Sie in der resultierenden Liste der Dienste auf den gewünschten Pool und klicken Sie auf **OK**.
    
5. Deaktivieren Sie das Kontrollkästchen **PSTN-Anrufer umgehen Wartebereich**, um Teilnehmer, die sich über das Festnetz einwählen, zunächst an den Wartebereich weiterzuleiten. In der Standardeinstellung gelangen Anrufer, die sich über das Festnetz einwählen, direkt zur Besprechung.
    
6. Legen Sie im Abschnitt **Als Referenten festlegen** fest, wer in der Besprechung als Referent agieren kann:
    
   - Klicken Sie auf **Keiner**, um nur dem Organisator die Rolle des Referenten zuzuweisen.
    
   - Klicken Sie auf **Unternehmen**, um nur denjenigen Teilnehmern die Funktion des Referenten zu ermöglichen, die Mitglieder Ihrer Organisation sind. Dies ist die Standardeinstellung.
    
   - Klicken Sie auf **Jeder**, um allen Teilnehmern das Agieren als Referent zu ermöglichen.
    
7. Wenn der Organisator bei der Planung einer Besprechung einen Konferenztyp auswählen soll, deaktivieren Sie das Kontrollkästchen **Konferenztyp standardmäßig zugewiesen**. In der Standardeinstellung wird der Konferenztyp automatisch zugewiesen.
    
8. Wenn Sie verhindern möchten, dass anonyme (nicht authentifizierte) Benutzer automatisch zugelassen werden, deaktivieren Sie das Kontrollkästchen **Anonyme Benutzer standardmäßig zulassen**. In der Standardeinstellung werden anonyme Benutzer automatisch für Besprechungen zugelassen.
    
9. Führen Sie die folgenden Schritte aus, um die Besprechungseinladung anzupassen, die an die Teilnehmer gesendet wird. Beachten Sie, dass für URLs und den benutzerdefinierten Fußzeilentext eine maximale Größe von 1 KB gilt. Wenn Sie, mit Ausnahme von **Hilfe-URL**, keinen Wert für die Anpassungen angeben, werden sie nicht in die Besprechung aufgenommen. Wenn Sie keine benutzerdefinierte Hilfe-URL angeben, wird die Standardhilfe-URL für Skype for Business in der Einladung angezeigt. 
    
   - Zum Anpassen des Logos, das in der Besprechungseinladung angezeigt wird, geben Sie in **Logo-URL** den Speicherort des Logos ein. Das Logo muss ein GIF- oder JPG-Bild mit einer Größe von 188 x 30 Pixel sein. 
    
   - Zum Anpassen des Hilfetexts, der in der Besprechungseinladung angezeigt wird, geben Sie in **Hilfe-URL** den Speicherort des Hilfetexts ein.
    
   - Zum Anpassen der rechtlichen Hinweise, die in der Besprechungseinladung angezeigt werden, geben Sie in **URL zu rechtlichen Hinweisen** den Speicherort der rechtlichen Hinweise ein.
    
   - Zum Anpassen des Fußzeilentexts, der in der Besprechungseinladung angezeigt wird, geben Sie in **Benutzerdefinierter Fußzeilentext** Text ein.
    
10. Klicken Sie auf **Commit ausführen**.
    
## <a name="create-meeting-configuration-settings-by-using-skype-for-business-server-management-shell"></a>Erstellen von Einstellungen für die besprechungskonfiguration mithilfe der Skype for Business Server-Verwaltungsshell

Verwenden Sie das **New-CsMeetingConfiguration**-Cmdlet, um Besprechungskonfigurationseinstellungen zu erstellen.
  
Mit dem folgenden Befehl wird ein neuer Satz von Besprechungskonfigurationseinstellungen für den Standort „Redmond“ erstellt:
  
```PowerShell
New-CsMeetingConfiguration -Identity "site:Redmond"
```

Da im vorherigen Befehl keine weiteren Parameter (außer dem obligatorischen Identity-Parameter) angegeben wurden, werden in den neuen Besprechungskonfigurationseinstellungen für alle Eigenschaften die Standardwerte verwendet.
  
Um Einstellungen zu erstellen, die andere Eigenschaftswerte verwenden, geben Sie einfach den entsprechenden Parameter und Parameterwert ein. Wenn Sie beispielsweise eine Auflistung von Besprechungskonfigurationseinstellungen erstellen möchten, die standardmäßig jeden als Referent zu einer Besprechung zulassen, verwenden Sie den folgenden Befehl:
  
```PowerShell
New-CsMeetingConfiguration -Identity "site:Redmond" -DesignateAsPresenter "Everyone"
```

Mehrere Eigenschaftswerte können eingestellt werden, indem Sie mehrere Parameter angeben. Beispielsweise wird mit dem folgenden Befehl jeder als Referent zu einer Besprechung zugelassen und außerdem werden PSTN-Benutzer gezwungen, im Wartebereich zu warten, bis sie formell zur Besprechung zugelassen werden:
  
```PowerShell
New-CsMeetingConfiguration -Identity "site:Redmond" -DesignateAsPresenter "Everyone" -PSTNUCallersBypassLobby $True
```

Weitere Informationen, einschließlich einer vollständigen Liste der Parameter, finden Sie unter [New-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/new-csmeetingconfiguration?view=skype-ps).
  

