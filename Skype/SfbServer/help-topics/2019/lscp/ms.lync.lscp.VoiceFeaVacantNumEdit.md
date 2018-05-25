---
title: Nicht zugewiesene Telefonnummer Erstellen einer neuen oder Bearbeiten einer vorhandenen
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.lscp.VoiceFeaVacantNumEdit
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 58903e40-6b93-40d6-88f8-1201743cd9be
description: Nicht zugewiesene Nummern sind Rufnummern, die für Ihre Organisation gültig sind, jedoch keinem Benutzer oder Telefon zugewiesen sind. In der Tabelle mit den nicht zugewiesenen Nummern ist angegeben, wie Anrufe bei nicht zugewiesenen Nummern behandelt werden sollen.
ms.openlocfilehash: b4cdd3d4efad5299b855c546edf2359698ef6a47
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="unassigned-phone-number-create-new-or-edit-existing"></a>Nicht zugewiesene Telefonnummer: Erstellen Sie einer neuen oder bearbeiten Sie einer vorhandenen
 
Nicht zugewiesene Nummern sind Rufnummern, die für Ihre Organisation gültig sind, jedoch keinem Benutzer oder Telefon zugewiesen sind. In der Tabelle mit den nicht zugewiesenen Nummern ist angegeben, wie Anrufe bei nicht zugewiesenen Nummern behandelt werden sollen.
  
> [!IMPORTANT]
> Wenn Sie einen neuen Bereichs nicht zugewiesenen Nummern erstellen oder Bearbeiten einer vorhandenen fertig sind, klicken Sie auf **OK** , um zur Seite **Nicht zugewiesene Nummer** zurückzugeben, die alle Bereiche auflistet. Die Änderungen, die Sie auf der Seite **Neu Unassigned Number Range** oder die **Rage für nicht zugewiesene Nummer bearbeiten** vorgenommen sind nicht in die Datenbank übernommen, bis Sie **Alle Commit** klicken Sie auf der Seite **Nicht zugewiesene Nummer** auf.
  
## <a name="ui-reference"></a>Referenz zur Benutzeroberfläche

In der folgenden Liste werden die Felder der Seite beschrieben.
  
- **Name** Geben Sie einen beschreibenden Namen, der den nicht zugewiesenen Nummernbereich. Nachdem Sie den Bereich gespeichert haben, kann dieser Name geändert werden.
    
- **Zahlenbereich** Geben Sie im ersten Feld die Anfangsnummer des Bereichs nicht zugewiesener Nummern. Geben Sie in das zweite Feld die Endnummer des Bereichs.
    
  - Die Startnummer für den Bereich muss kleiner oder gleich der Endnummer sein.
    
  - Wenn die erste Nummer im Bereich oder die letzte Nummer im Bereich eine Durchwahl umfassen, müssen sowohl die erste als auch die letzte Nummer im Bereich einen Durchwahl aufweisen und die Durchwahlnummer muss für die erste und die letzte Nummer übereinstimmen.
    
  - Die Anzahl muss mit den regulären Ausdruck übereinstimmen (tel:) ? (\+) [1-9] ? \d{0,17}(; Ext = [1-9] \d{0,9}) ?. Dies bedeutet, dass die Anzahl beginnt mit der Zeichenfolge tel: (Wenn Sie nicht, dass diese Zeichenfolge angeben es wird automatisch hinzugefügt werden für Sie), ein Pluszeichen (+) sowie ein Zahl von 1 bis 9. Die Telefonnummer kann bis zu 17 Zeichen umfassen, gefolgt von einer Durchwahl im Format ";ext=" plus der Durchwahlnummer.
    
- **Konferenzankündigungsdienst** Wählen Sie **Ankündigung** die ankündigungsanwendung den eingehenden Anruf behandeln sein oder **Exchange UM** für eine automatische Telefonzentrale von Exchange UM den eingehenden Anruf behandeln haben.
    
- Wenn Sie eine **Ankündigung** für **Ankündigungsdienst**ausgewählt haben:
    
  - **FQDN des Zielservers** Wählen Sie die Dienst-ID des Anwendungsdiensts, der die ankündigungsanwendung ausgeführt wird, die eingehende Anrufe für diesen Bereich nicht zugewiesener Nummern behandelt werden sollen.
    
  - **Ankündigung** Wählen Sie die Ankündigung für diesen Bereich nicht zugewiesener Nummern wiedergegeben werden soll.
    
-  Wenn Sie **Exchange UM** für **Ankündigungsdienst**ausgewählt haben:
    
  - **Telefonnummer der automatischen Telefonzentrale** Wählen Sie die Telefonnummer für die Exchange UM-Telefonzentrale aus.
    
Ausführliche Informationen zur Ankündigung Features und Funktionen finden Sie unter [Planen für die ankündigungsanwendung in Skype für Business 2015](../../plan-your-deployment/enterprise-voice-solution/announcement.md) in der Planungsdokumentation. Ausführliche Informationen zur Verwendung von nicht zugewiesenen Nummernbereiche finden Sie unter [Konfigurieren von Routing von nicht zugewiesenen Telefonnummern](http://technet.microsoft.com/library/a0650659-dce7-455f-8977-02454bbfa400.aspx) in der Betriebsdokumentation.
  
