---
title: Erstellen oder Ändern einer Übersetzungsregel für die Darstellung der ID des Angerufenen in Skype for Business Server 2015
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
ms.assetid: ba112df8-3bb4-48e4-a353-4bf9110ccd71
description: 'Zusammenfassung: Erfahren Sie, wie Sie eine übersetzungsregel definieren, indem Sie mit dem Erstellen einer Übersetzungsregel-Tool in Skype für Business Server 2015.'
ms.openlocfilehash: aa433375ad4dfa2dcc0c141d36b6d51ae28647f1
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="create-or-modify-a-translation-rule-for-called-id-presentation-in-skype-for-business-server-2015"></a>Erstellen oder Ändern einer Übersetzungsregel für die Darstellung der ID des Angerufenen in Skype for Business Server 2015
 
**Zusammenfassung:** Hier erfahren Sie, wie Sie eine übersetzungsregel definieren, indem Sie mit dem Erstellen einer Übersetzungsregel-Tool in Skype für Business Server 2015.
  
Gehen Sie folgendermaßen vor, wenn Sie eine übersetzungsregel definieren durch Eingabe einer Gruppe von Werten in das Tool **eine Übersetzungsregel erstellen** und Aktivieren von Skype Business Server-Systemsteuerung auf den entsprechenden Vergleichsmuster und die übersetzungsregel zu generieren möchten. Alternativ können Sie manuell einen regulären Ausdruck erstellen, um das Vergleichsmuster und die Übersetzungsregel zu definieren. Weitere Informationen hierzu finden Sie unter [Erstellen oder Ändern einer Übersetzung Regel manuell](http://technet.microsoft.com/library/049d1db3-af58-48c5-be89-52e1d068a4bd.aspx).
  
### <a name="to-define-a-rule-by-using-the-build-a-translation-rule-tool"></a>So definieren Sie eine Regel mit dem Tool zum Erstellen einer Übersetzungsregel

1. Öffnen von Skype Business Server-Systemsteuerung.
    
2. Führen Sie zur Definition einer übersetzungsregel, führen Sie die Schritte in [Konfigurieren eines Trunks mit Medien in Skype für Business Server 2015 umgehen](configure-trunk-with-media-bypass.md) bis Schritt 10 oder [Konfigurieren eines Trunks ohne Medien in Skype für Business Server 2015 umgehen](configure-trunk-without-media-bypass.md) bis Schritt 9.
    
3. Geben Sie unter **Name** auf der Seite **Neue Übersetzungsregel** oder **Übersetzungsregel bearbeiten** einen Namen ein, der das zu übersetzende Nummernmuster beschreibt.
    
4. (Optional) Geben Sie unter **Beschreibung**eine Beschreibung der übersetzungsregel für Beispiel uns International Ferngespräche.
    
5. Geben Sie im Abschnitt **Übersetzungsregel erstellen** des Dialogfelds die folgenden Werte ein:
    
   - **Anfangsziffern**: (Optional) Geben Sie die Anfangsziffern der Nummern ein, die Sie mit dem Muster abgleichen möchten. Beispiel: Geben Sie + in dieses Feld, um Nummern im e. 164-format (die beginnen mit +).
    
   - **Länge**: Geben Sie die Anzahl von Ziffern im Vergleichsmuster ein und wählen Sie aus, ob mit dem Muster Nummern abgeglichen werden sollen, die exakt diese Länge, mindestens diese Länge oder eine beliebige Länge aufweisen. Geben Sie beispielsweise 11 und SelectAt in der Dropdown-Liste mit Zahlen übereinstimmen, die mindestens 11 Ziffern umfassen sind mindestens.
    
   - **Zu entfernende Ziffern**: (Optional) Geben Sie die Anzahl von Anfangsziffern ein, die entfernt werden sollen. Geben Sie beispielsweise 1 entfernen, um die + vom Beginn der Zahl.
    
   - **Hinzuzufügende Ziffern**: (Optional) Geben Sie die Ziffern ein, die der übersetzten Nummer vorangestellt werden sollen. Geben Sie beispielsweise 011 wie gewünscht 011 an der übersetzten Nummern vorangestellt werden, wenn die Regel angewendet wird.
    
    Die in diesen Feldern eingegebenen Werte werden in den Feldern **Muster für Vergleich** und **Übersetzungsregel** widergespiegelt. Wenn Sie beispielsweise die vorstehend genannten Beispielwerte verwenden, lautet der reguläre Ausdruck im Feld **Muster für Vergleich** wie folgt:
    
    ^\+(\d{9}\d+)$
    
    Das Feld **Übersetzungsregel** gibt ein Muster für das Format der übersetzten Nummern an. Dieses Muster besteht aus zwei Teilen:
    
   - Ein Wert (z. B. $1), der die Anzahl der Nachkommastellen in das Vergleichsmuster darstellt
    
   - (Optional) Einem Wert, den Sie durch eine Eingabe im Feld **Hinzuzufügende Ziffern** voranstellen können
    
    Verwendung der vorstehend 011$ 1 wird im Feld **übersetzungsregel** angezeigt.
    
    Bei Anwendung dieser Übersetzungsregel wird die Nummer +441235551010 in 011441235551010 umgewandelt.
    
6. Klicken Sie auf **OK**, um die Übersetzungsregel zu speichern.
    
7. Klicken Sie auf **OK**, um die Trunkkonfiguration zu speichern.
    
8. Klicken Sie auf der Seite **Trunkkonfiguration** auf **Commit** und klicken Sie anschließend auf **Commit für alle Elemente ausführen**. 
    
   > [!NOTE]
   > Immer dann, wenn Sie eine Übersetzungsregel erstellen oder ändern, müssen Sie den Befehl **Commit für alle Elemente ausführen** ausführen, um die Konfigurationsänderung zu veröffentlichen. Weitere Informationen hierzu finden Sie unter [Veröffentlichen ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md) in der Betriebsdokumentation.
  
### <a name="to-define-a-translation-rule-manually"></a>So definieren Sie eine Übersetzungsregel manuell

1. Öffnen von Skype Business Server-Systemsteuerung
    
2. Führen Sie zur Definition einer übersetzungsregel, führen Sie die Schritte in [Konfigurieren eines Trunks mit Medien in Skype für Business Server 2015 umgehen](configure-trunk-with-media-bypass.md) bis Schritt 10 oder [Konfigurieren eines Trunks ohne Medien in Skype für Business Server 2015 umgehen](configure-trunk-without-media-bypass.md) bis Schritt 9.
    
3. Geben Sie im Feld **Name** auf der Seite **Neue Übersetzungsregel** oder **Übersetzungsregel bearbeiten** einen Namen ein, der das zu übersetzende Nummernmuster beschreibt.
    
4. (Optional) Geben Sie eine Beschreibung der übersetzungsregel, beispielsweise uns International Ferngespräche wählen im Feld **Beschreibung**.
    
5. Klicken Sie im unteren Bereich des Abschnitts **Übersetzungsregel erstellen** auf **Bearbeiten**.
    
6. Geben Sie unter **Regulären Ausdruck eingeben** Folgendes ein:
    
   - Geben Sie unter **Übereinstimmung mit dem folgenden Muster** das Muster an, das für den Abgleich der zu übersetzenden Nummern verwendet werden soll.
    
   - Geben Sie unter **Übersetzungsregel** ein Muster für das Format der übersetzten Nummern an.
    
    Beispiel: bei Eingabe ^\+(\d{9}\d+)$ in **dieses Muster abgleichen** and011$ 1 in **übersetzungsregel**, die Regel + 441235551010 in 011441235551010 übersetzt.
    
7. Klicken Sie auf **OK**, um die Übersetzungsregel zu speichern.
    
8. Klicken Sie auf **OK**, um die Trunkkonfiguration zu speichern.
    
9. Klicken Sie auf der Seite **Trunkkonfiguration** auf **Commit** und klicken Sie anschließend auf **Commit für alle Elemente ausführen**. 
    
    > [!NOTE]
    > Immer dann, wenn Sie eine Übersetzungsregel erstellen oder ändern, müssen Sie den Befehl **Commit für alle Elemente ausführen** ausführen, um die Konfigurationsänderung zu veröffentlichen. Weitere Informationen hierzu finden Sie unter [Veröffentlichen ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md) in der Betriebsdokumentation.
  
## <a name="see-also"></a>Siehe auch

#### 

[Konfigurieren eines Trunks mit medienumgehung in Skype für Business Server 2015](configure-trunk-with-media-bypass.md)
  
[Konfigurieren eines Trunks ohne medienumgehung in Skype für Business Server 2015](configure-trunk-without-media-bypass.md)
  
[Veröffentlichen von ausstehenden Änderungen an der VoIP-Routingkonfiguration in Skype für Business 2015](voice-route-config-changes.md)
#### 

[Bereitstellen von medienumgehung in Skype für Business Server 2015](deploy-media-bypass.md)
