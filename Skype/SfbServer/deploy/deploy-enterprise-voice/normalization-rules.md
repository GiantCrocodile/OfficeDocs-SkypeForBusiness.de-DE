---
title: Erstellen oder Ändern einer Normalisierungsregel in Skype for Business 2015
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
ms.assetid: e8547d7b-f74d-4a73-9a7d-df20d7a87fcd
description: 'Zusammenfassung: Informationen Sie zum definieren, erstellen und Ändern einer Normalisierungsregel in Skype für Business Server 2015.'
ms.openlocfilehash: 5b55e5e930680d3c51908b77d44a80e2e74ef89c
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="create-or-modify-a-normalization-rule-in-skype-for-business-2015"></a>Erstellen oder Ändern einer Normalisierungsregel in Skype for Business 2015
 
**Zusammenfassung:** Informationen Sie zum definieren, erstellen und Ändern einer Normalisierungsregel in Skype für Business Server 2015.
  
Definieren, erstellen und Ändern von Normalisierungsregeln in Skype für Business Server.
  
### <a name="to-define-a-normalization-rule-by-using-build-a-normalization-rule"></a>So definieren Sie eine Normalisierungsregel mit Normalisierungsregel erstellen

1. Öffnen von Skype Business Server-Systemsteuerung
    
2. (Optional) Führen Sie die Schritte in [Erstellen oder Ändern von Wähleinstellungen in Skype für Business Server 2015](dial-plans.md) bis Schritt 11 oder [Modify a Dial Plan](http://technet.microsoft.com/library/a91f02df-cf60-40cf-82fe-e0342c118b91.aspx) bis Schritt 10.
    
3. Geben Sie unter **Neue Normalisierungsregel** oder **Normalisierungsregel bearbeiten**einen Namen, der das im **Namen** (beispielsweise 5stellendurchwahl).) normalisierende Nummernmuster beschreibt.
    
4. (Optional) Geben Sie in **Beschreibung** eine Beschreibung der Normalisierungsregel ein (beispielsweise „Übersetzt 5-stellige Durchwahlnummern“).
    
5. Geben Sie im Abschnitt **Normalisierungsregel erstellen** Werte in die folgenden Felder ein:
    
   - **Anfangsziffern** (Optional) Geben Sie die führenden Ziffern gewählter Nummern, die Sie das Muster abgleichen möchten. Wenn Sie das Muster abgleichen möchten gewählte type425 beispielsweise Zahlen mit 425 beginnt.
    
   - **Länge** Geben Sie die Anzahl der Nachkommastellen in das Vergleichsmuster, und wählen Sie, ob Übereinstimmung Nummern beliebiger Länge gewählten Übereinstimmung Rufnummern, die mindestens diese Länge sind oder das Muster dieser Länge genau entsprechen soll.
    
   - **So entfernen Sie Ziffern** (Optional) Geben Sie die Anzahl von Anfangsziffern ein, die aus gewählten Nummern entfernt werden Sie das Muster abgleichen möchten.
    
   - **Hinzuzufügende Ziffern** (Optional) Geben Sie die Ziffern auf gewählten Nummern hinzugefügt werden soll, dass Sie das Muster abgleichen möchten.
    
    Die in diesen Feldern eingegebenen Werte werden in den Feldern **Muster für Vergleich** und **Übersetzungsregel** widergespiegelt. Beispielsweise wenn Sie leer ist, Typ7 **Starten Ziffern** in das Feld **Länge verlassen** und wählen Sie **genau**, und geben Sie 0 in **Ziffern zu entfernen**, wird der resultierende reguläre Ausdruck in dem **Muster abgleichen** :
    
    ^(\d{7})$
    
6. Geben Sie in **Übersetzungsregel** ein Muster für das Format der übersetzten E.164-Telefonnummern ein:
    
   - Ein Wert, der die Anzahl von Ziffern repräsentiert, die im Vergleichsmuster angegeben ist. Wenn das Vergleichsmuster beispielsweise ^ (\d{7})$ dann$ 1 in der übersetzungsregel stellt 7 Ziffer gewählte Nummern.
    
   - (Optional) Geben Sie einen Wert in das Feld **hinzuzufügende Ziffern** an Stellen die übersetzte Nummer (beispielsweise + 1425) vorangestellt werden.
    
    Z. B., wenn **Muster abgleichen** contains^(\d{7})$ dem Muster für gewählter Nummern und **übersetzungsregel** enthält + 1425 Telefonnummern $1 als das Muster für das e. 164, übersetzt die Regel 5550100 in + 14255550100.
    
7. (Optional) Falls die Normalisierungsregel eine interne Telefonnummer des Unternehmens ergibt, klicken Sie auf **Interne Durchwahl**.
    
8. (Optional) Geben Sie eine Nummer zum Testen der Normalisierungsregel ein und klicken Sie auf **Los**. Die Testergebnisse werden unterhalb von **Geben Sie eine Testnummer ein** angezeigt.
    
    > [!NOTE]
    > Sie können eine Normalisierungsregel speichern, die den Test nicht bestanden hat und sie später neu konfigurieren. Weitere Informationen hierzu finden Sie unter [VoIP-Routing testen](http://technet.microsoft.com/library/d3aae909-fef6-440f-b144-0b62dc82bf5d.aspx). 
  
9. Klicken Sie auf **OK**, um die Normalisierungsregel zu speichern.
    
10. Klicken Sie auf **OK**, um die Wähleinstellungen zu speichern.
    
11. Klicken Sie auf der Seite **Wählplan** auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**. 
    
    > [!NOTE]
    > Jedes Mal, wenn Sie eine Normalisierungsregel erstellen oder ändern, müssen Sie den Befehl **Commit für alle** ausführen, um die Konfigurationsänderung zu veröffentlichen. Weitere Informationen hierzu finden Sie unter [Veröffentlichen ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md) in der Betriebsdokumentation.
  
### <a name="to-define-a-normalization-rule-manually"></a>So definieren Sie eine Normalisierungsregel manuell

1. Öffnen von Skype Business Server-Systemsteuerung
    
2. (Optional) Führen Sie die Schritte in [Erstellen oder Ändern von Wähleinstellungen in Skype für Business Server 2015](dial-plans.md). 
    
3. Geben Sie unter **Neue Normalisierungsregel** oder **Normalisierungsregel bearbeiten**einen Namen, der das im **Feld Name** (beispielsweise Name der Normalisierung rule5DigitExtension) normalisierende Nummernmuster beschreibt.
    
4. (Optional) Geben Sie im Feld **Beschreibung** eine Beschreibung der Normalisierungsregel ein (beispielsweise „Übersetzt 5-stellige Durchwahlnummern“).
    
5. Klicken Sie in **Normalisierungsregel erstellen** auf **Bearbeiten**.
    
6. Geben Sie in **Regulären Ausdruck eingeben** Folgendes ein:
    
   - Geben Sie in **Dieses Muster abgleichen** das Muster an, das für den Abgleich der gewählten Telefonnummer verwendet werden soll.
    
   - Geben Sie in **Übersetzungsregel** ein Muster für das Format der übersetzten E.164-Telefonnummern ein.
    
    Beispiel: bei Eingabe ^ (\d{7})$ in **dieses Muster** und + 1425$ 1 in **übersetzungsregel**, die Regel 5550100 in + 14255550100 normalisiert.
    
7. (Optional) Falls die Normalisierungsregel eine interne Telefonnummer des Unternehmens ergibt, klicken Sie auf **Interne Durchwahl**.
    
8. (Optional) Geben Sie eine Nummer zum Testen der Normalisierungsregel ein und klicken Sie auf **Los**. Die Testergebnisse werden unterhalb von **Geben Sie eine Testnummer ein** angezeigt.
    
9. Klicken Sie auf **OK**, um die Normalisierungsregel zu speichern.
    
10. Klicken Sie auf **OK**, um die Wähleinstellungen zu speichern.
    
11. Klicken Sie auf der Seite **Wählplan** auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**.
    
    > [!NOTE]
    > Jedes Mal, wenn Sie eine Normalisierungsregel erstellen oder ändern, müssen Sie den Befehl **Commit für alle** ausführen, um die Konfigurationsänderung zu veröffentlichen. Weitere Informationen hierzu finden Sie unter [Veröffentlichen ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md) in der Betriebsdokumentation.
  
