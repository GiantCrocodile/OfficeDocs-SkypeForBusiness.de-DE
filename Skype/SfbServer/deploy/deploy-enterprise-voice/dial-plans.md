---
title: Erstellen oder Ändern eines Wählplans in Skype for Business Server 2015
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Admin
ms.assetid: d2fef3d0-7e78-4591-b712-d62ac71d71a5
description: 'Zusammenfassung: Informationen Sie zum Erstellen oder Ändern von Wähleinstellungen mithilfe der Skype für Business Server-Systemsteuerung.'
ms.openlocfilehash: eaa2446c86b117558953416d0815a38371b205b1
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="create-or-modify-a-dial-plan-in-skype-for-business-server-2015"></a>Erstellen oder Ändern eines Wählplans in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zum Erstellen oder Ändern von Wähleinstellungen mithilfe der Skype für Business Server-Systemsteuerung.
  
### <a name="to-create-a-dial-plan"></a>So erstellen Sie einen Wählplan

1. Öffnen von Skype Business Server-Systemsteuerung.
    
2. Klicken Sie in der linken Navigationsleiste auf **VoIP-Routing** und dann auf **Wählplan**.
    
3. Klicken Sie auf der Seite **Wählplan** auf **Neu** und wählen Sie einen Bereich für den Wählplan aus:
    
   - **Standortwählplan** wird auf einen gesamten Standort angewendet, ausgenommen auf Benutzer oder Gruppen, die einem Wählplan zugeordnet wurden. Wenn Sie die **Website** für einen Wählplan Bereich auswählen, müssen Sie im Dialogfeld **Standort auswählen** die Website auswählen. Wenn bereits ein Wählplan für einen Standort erstellt wurde, wird der Standort nicht im Dialogfeld **Standort auswählen** angezeigt.
    
   - **Poolwählplan** kann auf ein PSTN-Gateway oder eine Registrierungsstelle angewendet werden. Wenn Sie für einen Wählplan Bereich **Pool** auswählen, wählen Sie im Dialogfeld **Wählen Sie einen Dienst** die PSTN-Gateway oder der Registrierung. Wenn bereits ein Wählplan für einen Dienst (PSTN-Gateway oder Registrierungsstelle) erstellt wurde, wird der Dienst nicht in der Liste angezeigt.
    
   - **Benutzerwählplan** kann auf bestimmte Benutzer oder Gruppen angewendet werden.
    
    > [!NOTE]
    > Nachdem Sie den Bereich für den Wählplan ausgewählt haben, kann dieser nicht mehr geändert werden. 
  
4. Wenn Sie einen Wählplan erstellen, geben Sie im Dialogfeld **Neuer Wählplan** im Feld **Name** einen beschreibenden Namen ein. Nach dem Speichern kann dieser Name nicht mehr geändert werden.
    
    > [!NOTE]
    > Für standortwähleinstellungen im Feld **Name** wird mit dem Namen des Standorts vorausgefüllt und kann nicht geändert werden. > für poolwählpläne im Feld **Name** wird mit dem PSTN-Gateway oder Name der Registrierungsstelle vorausgefüllt und kann nicht geändert werden.
  
5. Das Feld **Einfacher Name** wird mit demselben Namen vorausgefüllt, der im Feld **Name** erscheint. Sie können dieses Feld optional bearbeiten, um einen aussagekräftigeren Namen anzugeben, der den Standort, Dienst oder Benutzer zur Anwendung des Wählplans besser beschreibt.
    
    > [!IMPORTANT]
    > Die **einfacher Name** muss für alle Wählpläne in Ihrer Bereitstellung eindeutig sein. 256 Unicodezeichen, kann jeweils ein Buchstaben oder numerische Zeichen, einen Bindestrich (-), einen Punkt (.) oder einem Unterstrich (_) nicht überschreiten. > Zeichen **nicht unterstützt** gehören, Leerzeichen und reservierte Zeichen gemäß Definition in RFC 3966 (http://www.ietf.org/rfc/rfc3966.txt). Reservierte Zeichen, die in der **Einfachen Namen** **nicht unterstützt** werden, sind: > ";" "/" "?" ":" "@" "&amp;" "=" "+""$""," 
  
6. (Optional) Geben Sie im Feld **Beschreibung** zusätzliche beschreibende Informationen zum Wählplan ein.
    
7. (Optional) Wenn Sie diesen Wählplan als eine Region für Einwählnummern verwenden möchten, geben Sie eine **Einwahlkonferenzregion** an. Wenn Sie diesen Wählplan nicht für Einwählnummern verwenden möchten, lassen Sie dieses Feld leer. 
    
    > [!NOTE]
    > Regionen für Einwahlkonferenzen werden benötigt, um Einwählnummern für Konferenzen einem oder mehreren Wählplänen zuzuordnen. 
  
8. (Optional) Geben Sie im Feld **Präfix für externen Zugriff** nur dann einen Wert an, wenn Benutzer eine oder mehrere zusätzliche Nummern wählen müssen, um eine externe Leitung zu erhalten (z. B. 9). Sie können ein Präfix eingeben, das aus bis zu vier Zeichen besteht (#, * und 0-9).
    
    > [!NOTE]
    > Wenn Sie ein Präfix für den externen Zugriff eingeben, müssen Sie keine neue Normalisierungsregel zur Unterstützung des Präfix erstellen. 
  
9. Führen Sie die folgenden Schritte aus, um Normalisierungsregeln für den Wählplan zuzuordnen und zu konfigurieren:
    
    - Um eine oder mehrere Regeln aus einer Liste von alle verfügbaren in Ihrer Bereitstellung von Enterprise-VoIP-Normalisierungsregeln auszuwählen, klicken Sie auf **auswählen**. Klicken Sie im Dialogfeld **Normalisierungsregeln auswählen** auf die Regeln, die Sie dem Wählplan zuordnen möchten und klicken Sie anschließend auf **OK**.
    
   - Klicken Sie auf **Neu**, um eine neue Normalisierungsregel zu definieren und dem Wählplan zuzuordnen. Ausführliche Informationen zum Definieren einer neuen Regel finden Sie unter [Erstellen oder Ändern einer Normalisierungsregel in Skype für Business 2015](normalization-rules.md).
    
   - Klicken Sie auf den Regelnamen und anschließend auf **Details einblenden**, um eine Normalisierungsregel zu bearbeiten, die bereits dem Wählplan zugeordnet ist. 
    
   - Um eine vorhandene Normalisierungsregel als Startpunkt für die Definition einer neuen Regel zu verwenden, markieren Sie den Regelnamen, klicken Sie auf **Kopieren** und anschließend auf **Einfügen**. 
    
   - Wenn Sie eine Normalisierungsregel aus dem Wählplan entfernen möchten, markieren Sie den Regelnamen und klicken Sie auf **Entfernen**.
    
     > [!NOTE]
     > Jedem Wählplan muss mindestens eine Normalisierungsregel zugeordnet sein. Informationen dazu, wie Sie alle Normalisierungsregeln Einwahl bestimmen Plan erfordert, finden Sie unter [Plan für ausgehende VoIP-routing in Skype für Business Server 2015](../../plan-your-deployment/enterprise-voice-solution/outbound-voice-routing.md) in der Planungsdokumentation.
  
10. Stellen Sie sicher, dass die Wähleinstellungen Normalisierungsregeln in der richtigen Reihenfolge angeordnet sind. Um eine Regel Position in der Liste zu ändern, markieren Sie den Namen der Regel und klicken Sie auf den Pfeil nach oben oder nach-unten Sie-Pfeil.
    
    > [!IMPORTANT]
    > Skype für Business Server der Regelliste Normalisierung von oben nach unten durchläuft und verwendet die erste Regel, die mit die gewählte Nummer übereinstimmt. Wenn Sie einen Wählplan so konfigurieren, dass eine gewählte Nummer mit mehr als einer Normalisierungsregel übereinstimmen kann, müssen Sie sicherstellen, dass die einschränkenderen Regeln über den weniger einschränkenden Regeln angeordnet sind. > Die Standardeinstellung **Alle beibehalten** Normalisierung rule^(\d{11})$ ermittelt eine beliebige Anzahl von Ziffern 11. Wenn Sie eine Normalisierungsregel hinzuzufügen, die 11 Ziffern entspricht, die mit 1425 beginnen, stellen Sie beispielsweise sicher, dass **Alle beibehalten** unterhalb der weitere restrictive^(1425\d{7})$ Regel sortiert ist.
  
11. (Optional) Geben Sie eine Nummer zum Testen des Wählplans ein und klicken Sie auf **Los**. Die Testergebnisse werden unterhalb von **Geben Sie eine Testnummer ein** angezeigt.
    
12. Klicken Sie anschließend auf **OK**. 
    
13. Klicken Sie auf der Seite **Wählplan** auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**. 
    
    > [!NOTE]
    > Jedes Mal, wenn Sie einen Wählplan erstellen, müssen Sie den Befehl **Commit für alle Elemente ausführen** aufrufen, um die Konfigurationsänderung zu veröffentlichen. Weitere Informationen hierzu finden Sie unter [Veröffentlichen ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md) in der Betriebsdokumentation.
  
### <a name="to-modify-a-dial-plan"></a>So ändern Sie einen Satz mit Wähleinstellungen

1.  Melden Sie sich an dem Computer als Mitglied der Gruppe RTCUniversalServerAdmins oder als Mitglied der Rolle CsVoiceAdministrator, CsServerAdministrator oder csadministrator an. Weitere Informationen hierzu finden Sie unter **Delegate Setup Permissions**.
    
2. Öffnen Sie ein Browserfenster, und geben Sie die Admin-URL, um die Skype Business Server-Systemsteuerung zu öffnen.  
    
3. Klicken Sie in der linken Navigationsleiste auf **VoIP-Routing** und dann auf **Wählplan**.
    
4. Doppelklicken Sie auf der Seite **Wähleinstellungen** auf einen Satz mit Wähleinstellungen.
    
    > [!NOTE]
    > Bereich und Name der Wähleinstellungen wurden beim Erstellen der Wähleinstellungen festgelegt. Sie können nicht geändert werden. 
  
5. (Optional) Bearbeiten Sie im Abschnitt **Wähleinstellungen bearbeiten** das Feld **Einfacher Name** (dieses wird mit dem Namen im Feld **Name** vorausgefüllt), um einen beschreibenderen Namen einzugeben, der den Standort, Dienst oder Benutzer angibt, für den die Wähleinstellungen gelten.
    
    > [!IMPORTANT]
    > Die **einfacher Name** muss unter allen Wählplänen in der Lync Server 2013-Bereitstellung eindeutig sein. 256 Unicodezeichen, kann jeweils ein Buchstaben oder numerische Zeichen, einen Bindestrich (-), einen Punkt (.), ein Pluszeichen (+) oder einem Unterstrich (_) nicht überschreiten. > Leerzeichen sind im Feld **einfacher Name** nicht zulässig.
  
6. (Optional) Geben Sie im Feld **Beschreibung** beschreibende Informationen zu den Wähleinstellungen ein.
    
7. (Optional) Wenn Sie diesen Wählplan als eine Region für Einwählnummern verwenden möchten, geben Sie eine **Einwahlkonferenzregion** an. Wenn Sie diesen Wählplan nicht für Einwählnummern verwenden möchten, lassen Sie dieses Feld leer. 
    
    > [!NOTE]
    > Regionen für Einwahlkonferenzen werden benötigt, um Einwählnummern für Konferenzen einem oder mehreren Wählplänen zuzuordnen. 
  
8. (Optional) Geben Sie im Feld **Präfix für externen Zugriff** nur dann einen Wert an, wenn Benutzer eine oder mehrere zusätzliche Nummern wählen müssen, um eine externe Leitung zu erhalten (z. B. 9). Sie können ein Präfix eingeben, das aus bis zu vier Zeichen besteht (d. h. #, * und 0-9).
    
    > [!NOTE]
    > Wenn Sie ein Präfix für den externen Zugriff eingeben, müssen Sie keine neue Normalisierungsregel zur Unterstützung des Präfix erstellen. 
  
9. Zuordnen und Konfigurieren von Normalisierungsregeln für die Wähleinstellungen:
    
   - Um eine oder mehrere Regeln aus einer Liste von alle verfügbaren in Ihrer Bereitstellung von Enterprise-VoIP-Normalisierungsregeln auszuwählen, klicken Sie auf **auswählen**. Klicken Sie im Dialogfeld **Normalisierungsregeln auswählen** auf die Regeln, die Sie den Wähleinstellungen zuordnen möchten und klicken Sie anschließend auf **OK**.
    
   - Klicken Sie auf **Neu**, um eine neue Normalisierungsregel zu definieren und dem Wählplan zuzuordnen. Ausführliche Informationen zum Definieren einer neuen Regel finden Sie unter [Erstellen oder Ändern einer Normalisierungsregel in Skype für Business 2015](normalization-rules.md).
    
   - Klicken Sie auf den Regelnamen und anschließend auf **Details einblenden**, um eine Normalisierungsregel zu bearbeiten, die bereits dem Wählplan zugeordnet ist. 
    
   - Um eine vorhandene Normalisierungsregel als Startpunkt für die Definition einer neuen Regel zu verwenden, markieren Sie den Regelnamen, klicken Sie auf **Kopieren** und anschließend auf **Einfügen**. 
    
   - Wenn Sie eine Normalisierungsregel aus dem Wählplan entfernen möchten, markieren Sie den Regelnamen und klicken Sie auf **Entfernen**.
    
    > [!NOTE]
    > Jedem Wählplan muss mindestens eine Normalisierungsregel zugeordnet sein. Weitere Informationen dazu, wie Sie alle Normalisierungsregeln Einwahl bestimmen Plan erfordert, finden Sie unter [Plan für ausgehende VoIP-routing in Skype für Business Server 2015](../../plan-your-deployment/enterprise-voice-solution/outbound-voice-routing.md) in der Planungsdokumentation.
  
10. Stellen Sie sicher, dass die Wähleinstellungen Normalisierungsregeln in der richtigen Reihenfolge angeordnet sind. Um eine Regel Position in der Liste zu ändern, markieren Sie den Namen der Regel und klicken Sie auf den Pfeil nach oben oder nach-unten Sie-Pfeil.
    
    > [!IMPORTANT]
    > Skype für Business Server der Regelliste Normalisierung von oben nach unten durchläuft und verwendet die erste Regel, die mit die gewählte Nummer übereinstimmt. Wenn Sie einen Wählplan so konfigurieren, dass eine gewählte Nummer mit mehr als einer Normalisierungsregel übereinstimmen kann, müssen Sie sicherstellen, dass die einschränkenderen Regeln über den weniger einschränkenden Regeln angeordnet sind. > Die Standardeinstellung **Alle beibehalten** Normalisierung rule^(\d{11})$ ermittelt eine beliebige Anzahl von Ziffern 11. Wenn beispielsweise Sie eine Normalisierungsregel hinzuzufügen, die 11 Ziffern entspricht, die mit 1425 beginnen, stellen Sie sicher, dass **Alle beibehalten** unterhalb der weitere restrictive^(1425\d{7})$ Regel sortiert ist.
  
11. (Optional) Geben Sie eine Nummer zum Testen des Wählplans ein und klicken Sie auf **Los**. Die Testergebnisse werden unterhalb von **Geben Sie eine Testnummer ein** angezeigt.
    
    > [!NOTE]
    > Sie können einen Wählplan speichern, der den Test nicht bestanden hat, und ihn später neu konfigurieren. Weitere Informationen hierzu finden Sie unter [VoIP-Routing testen](http://technet.microsoft.com/library/d3aae909-fef6-440f-b144-0b62dc82bf5d.aspx). 
  
12. Klicken Sie anschließend auf **OK**. 
    
13. Klicken Sie auf der Seite **Wählplan** auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**. 
    
    > [!NOTE]
    > Jedes Mal, wenn Sie einen Wählplan erstellen oder ändern, müssen Sie den Befehl **Commit für alle Elemente ausführen** ausführen, um die Konfigurationsänderung zu veröffentlichen. Weitere Informationen hierzu finden Sie unter [Veröffentlichen ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md) in der Betriebsdokumentation.
  
## <a name="see-also"></a>Siehe auch

#### 

[Veröffentlichen von ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md)
