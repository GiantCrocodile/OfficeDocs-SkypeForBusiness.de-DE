---
title: Nutzungsbericht über die Reaktionsgruppe in Skype for Business Server 2015
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 3248b320-a552-400a-8485-6891af4eb0f3
description: 'Zusammenfassung: Erfahren Sie mehr über die Anwendung "Reaktionsgruppe" in Skype für Business Server 2015.'
ms.openlocfilehash: 7fb30b5ac068b9f87e68cb98b975b87e06c455f1
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="response-group-usage-report-in-skype-for-business-server-2015"></a>Nutzungsbericht über die Reaktionsgruppe in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zu der Anwendung "Reaktionsgruppe" in Skype für Business Server 2015.
  
Die Anwendung "Reaktionsgruppe" bietet eine Möglichkeit für Skype für Business Server 2015 beantworten und Route Telefonanrufe basierend auf die Nummer, die gewählt wurde und, optional, die Antworten des Anrufers zu einer Reihe von Fragen. Normalerweise werden Reaktionsgruppenanrufe nicht an eine Einzelperson, sondern an ein Personenteam weitergeleitet, das als Agentgruppe bezeichnet wird. Angenommen, wenn die Telefonnummer für Ihr Helpdesk angerufen werden, kann Skype für Business Server 2015 automatisch dieses Aufrufs an den ersten verfügbaren Helpdesk-Agent weiterleiten. Alternativ kann Skype für Business Server bitten Sie eine Reihe von Fragen ("drücken Sie 1, wenn Sie die Hardware Probleme auftreten. Wenn Sie Softwareprobleme haben, drücken Sie die 2. Wenn Sie Netzwerkprobleme haben, drücken Sie die 3.“) und den Anruf dann entsprechend der Antwort auf diese Fragen an den am besten geeigneten Helpdesk-Agenten weiterleiten.
  
Der Nutzungsbericht über die Reaktionsgruppe gibt einen detaillierten Einblick in die Anzahl der Telefonanrufe, die von allen Reaktionsgruppen-Workflows empfangen wurden. Diese Anrufe werden dann in spezifischere Kategorien unterteilt, z. B. „Angebotene Anrufe“, „Angenommene Anrufe“ und „Abgebrochene Anrufe“.
  
Bei der Verwendung des Nutzungsberichts über die Reaktionsgruppe ist es wichtig, den Unterschied zwischen den gemeldeten Anruftypen zu verstehen:
  
- **Empfangene Anrufe**. Gesamtzahl der empfangenen Anrufe von allen Instanzen der Reaktionsgruppenanwendung.
    
- **Erfolgreiche Anrufe**. Gesamtzahl der Anrufe, die von der Reaktionsgruppenanwendung angenommen wurden.
    
- **Angebotene Anrufe**. Gesamtzahl der Anrufe, die an einen Reaktionsgruppenagent weitergeleitet wurden.
    
- **Angenommene Anrufe**. Gesamtzahl der Anrufe, die tatsächlich von einem Reaktionsgruppenagent angenommen wurden.
    
- **Prozentsatz abgebrochener Anrufe**. Prozentsatz der Anrufe, die von der Reaktionsgruppenanwendung empfangen, aber nicht von einem Agenten angenommen wurden. Dieser Wert wird berechnet, indem die angenommenen Anrufe von den empfangenen Anrufen abgezogen werden und dieser Wert dann durch die Anzahl der empfangenen Anrufe geteilt wird. Wenn Sie beispielsweise 10 Anrufe empfangen haben und 7 davon beantwortet wurden, ziehen Sie 7 von 10 ab, wonach 3 unbeantwortete Anrufe übrig bleiben. Dieser Wert wird dann durch 10 geteilt, woraus sich ein Prozentsatz von 30 % für abgebrochene Anrufe ergibt.
    
- **Durchgestellte Anrufe**. Gesamtzahl der Reaktionsgruppenanrufe, die aufgrund eines Timeouts oder eines Überlaufens der Warteschleife durchgestellt wurden.
    
Wenn Sie sich den Nutzungsbericht über die Reaktionsgruppe ansehen und sich nicht mehr an die Definition eines Anruftyps erinnern können, halten Sie einfach die Maus über die Beschriftung des entsprechenden Anruftyps. Daraufhin wird eine QuickInfo mit einer kurzen Beschreibung des Anruftyps angezeigt.
  
Mit einem Nutzungsbericht über Reaktionsgruppe können Sie nach einem Workflow-URI (die mit dem Workflow verknüpfte SIP-Adresse) filtern. Workflow-URIs werden nicht tatsächlich im Bericht angezeigt. Wenn Sie z. B. mehr darüber erfahren möchten, welche Workflows die meisten Anrufe entgegennehmen oder in welchen Workflows die meisten Anrufe durchgestellt werden, klicken Sie auf die entsprechende Metrik, um den Anruflistenbericht für Reaktionsgruppen für diesen bestimmten Zeitraum anzuzeigen. In diesem Bericht werden die Workflow-URIs aufgelistet.
  
## <a name="accessing-the-response-group-usage-report"></a>Zugreifen auf den Nutzungsbericht über die Reaktionsgruppe

Sie können über die Startseite für Überwachungsberichte auf den Nutzungsbericht über die Reaktionsgruppe zugreifen. Sie können die [Antwort Gruppe Call List Report in Skype für Business Server 2015](call-list-report.md) Drilldown, indem Sie auf eine der folgenden Metriken:
  
- Empfangene Anrufe
    
- Erfolgreiche Anrufe
    
- Angebotene Anrufe
    
- Angenommene Anrufe
    
- Durchgestellte Anrufe
    
## <a name="making-the-best-use-of-the-response-group-usage-report"></a>Optimale Verwendung des Nutzungsberichts über die Reaktionsgruppe

Eine der interessantesten Verwendungen des Nutzungsberichts über die Reaktionsgruppe ist vielleicht nicht auf den ersten Blick erkennbar: die Möglichkeit zum Abrufen von Nutzungsinformationen für einen einzelnen Reaktionsgruppenworkflow.
  
> [!CAUTION]
> Eine reaktionsgruppenworkflow ist im Wesentlichen eine Reihe von Anweisungen, die bestimmt, was Skype für Business Server wird ausgeführt, wenn ein Benutzer eine bestimmten Rufnummer wählt. Dafür ist jeder Workflow eindeutig einer Telefonnummer zugeordnet. Wenn jemand diese Nummer anruft, wird durch den Workflow festgelegt, wie der Anruf verarbeitet wird. Beispielsweise kann der Anruf zur Beantwortung einer Reihe von Fragen an das interaktive Sprachantwortsystem (IVR, Interactive Voice Response) weitergeleitet werden, sodass der Anrufer zur Eingabe weiterer Informationen aufgefordert wird („Für Hardwaresupport, drücken Sie die 1. Für Softwaresupport, drücken Sie die 2.“). Alternativ dazu kann der Anruf vom Workflow in eine Warteschleife gestellt und gehalten werden, bis ein Agent den Anruf entgegennehmen kann. Auch die Verfügbarkeit von Agenten zur Anrufannahme wird vom Workflow vorgegeben: Mithilfe von Workflows werden sowohl Geschäftszeiten (die Wochentage und Tageszeiten, zu denen Agenten für die Annahme von Anrufen verfügbar sind) als auch Feiertage (Tage, an denen keine Agenten zur Anrufannahme bereitstehen) konfiguriert. Jedes Mal, wenn eine Telefonnummer gewählt wird, die zur Reaktionsgruppenanwendung gehört, wird eigentlich ein Reaktionsgruppenworkflow angerufen. 
  
Obwohl im Nutzungsbericht über Reaktionsgruppe keine Workflow-URIs angezeigt werden, kann dennoch die Nutzungsstatistik für einen einzelnen Workflow angezeigt werden, was oftmals sehr nützlich sein kann. Angenommen, Sie haben vor kurzem eine neue Anzeigenkampagne lanciert und möchten gern erfahren, ob interessierte Leute anrufen, um mehr über dieses Produkt zu erfahren. Wenn Sie mit der in der Anzeigenkampagne genannten Telefonnummer einen Reaktionsgruppenworkflow verknüpft haben, können Sie auf einfache Weise feststellen, wie viele Personen (wenn überhaupt) diese Nummer gewählt haben.
  
Sie können auch einen ähnlichen Ansatz verwenden, um die Anzahl der Anrufe zu messen, die von Ihrem internen Helpdesk oder Ihrer Kundendienstabteilung behandelt werden.
  
Wenn Sie die Nutzungsstatistik für einen bestimmten Workflow prüfen möchten, geben Sie den Workflow-URI in das Feld „Workflow-URI“ ein. Wie oben erwähnt, erscheinen im Bericht keine Workflow-URIs (die mit einem Workflow verknüpfte SIP-Adresse). Das bedeutet, Sie müssen den URI eines Workflows auf andere Weise herausfinden. Eine Möglichkeit hierzu ist die Verwendung von Windows PowerShell und die Skype für Business Server-Verwaltungsshell. Mit diesem Befehl werden beispielsweise die URIs für Ihre gesamten Reaktionsgruppenworkflows zurückgegeben:
  
```
Get-CsRgsWorkflow | Select-Object Name, PrimaryUri
```

Die zurückgegebenen Daten sehen so ähnlich aus, wie diese:
  
```
Name                            PrimaryUri
----                            ----------
Customer Support                sip:support@litwareinc.com
Help Desk                       sip:helpdesk@litwareinc.com
New Ad Campaign                 sip:newads@litwareinc.com

```

Mit diesem Befehl werden Informationen für einen einzelnen Workflow mit dem Namen „New Ad Campaign“ zurückgegeben:
  
```
Get-CsRgsWorkflow -Name "New Ad Campaign" | Select-Object Name, PrimaryUri

```

## <a name="filters"></a>Filter

Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Beispielsweise können Sie im Reaktionsgruppen-Verwendungsbericht Daten für all Ihre Reaktionsgruppen-Workflows anzeigen oder für einen einzelnen Workflow. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden die Anrufe nach Stunde, Tag, Woche oder Monat zusammengefasst.
  
In der folgenden Tabelle sind die Filter aufgeführt, die Sie im Reaktionsgruppen-Verwendungsbericht verwenden können.
  
**Reaktionsgruppen-Verwendungsbericht – Filter**

|**Name**|**Beschreibung**|
|:-----|:-----|
|**Von** <br/> |Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:  <br/> 07.07.2015 13:00  <br/> Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:  <br/> 07.07.2015  <br/> Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):  <br/> 03.07.2015  <br/> Eine Woche läuft immer von Sonntag bis einschließlich Samstag.  <br/> |
|**Bis** <br/> |Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:  <br/> 07.07.2015 13:00  <br/> Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:  <br/> 07.07.2015  <br/> Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):  <br/> 03.07.2015  <br/> Eine Woche läuft immer von Sonntag bis einschließlich Samstag.  <br/> |
|**Intervall** <br/> | Zeitintervall. Wählen Sie eine der folgenden Optionen aus: <br/>  Stündlich (maximal 25 Stunden können angezeigt werden) <br/>  Täglich (maximal 31 Tage können angezeigt werden) <br/>  Wöchentlich (maximal 12 Wochen können angezeigt werden) <br/>  Monatlich (maximal 12 Monate können angezeigt werden) <br/>  Wenn mit dem angegebenen Start- und Endzeitpunkt die maximale Anzahl der zulässigen Werte für das ausgewählte Intervall überschritten wird, wird nur die maximale Anzahl an Werten (beginnend mit dem Startzeitpunkt) angezeigt. Beispiel: Wenn Sie das Intervall „Täglich“ mit dem Startdatum 07.07.2015 und dem Enddatum 28.02.2015 ausgewählt haben, werden Daten für die Tage 07.08.2015 12:00 Uhr bis 07.09.2015 12:00 Uhr angezeigt (d. h. Daten für insgesamt 31 Tage). <br/> |
|**Workflow-URI** <br/> |Bietet Ihnen die Möglichkeit, die zurückgegebenen Daten auf den angegebenen Reaktionsgruppenworkflow zu beschränken. Geben Sie die Workflow-SIP-Adresse ein, um diesen Filter zu verwenden. Beispiel:  <br/> SIP:Helpdesk@litwareinc.com  <br/> |
   
## <a name="metrics"></a>Metriken

In der folgenden Tabelle sind die Informationen aufgeführt, die im Reaktionsgruppen-Verwendungsbericht angegeben werden.
  
**Reaktionsgruppen-Verwendungsbericht – Metriken**

|**Name**|**Können Sie nach dieser Metrik werden sortiert?**|**Beschreibung**|
|:-----|:-----|:-----|
|**Stündlich** <br/> **Täglich** <br/> **Wöchentlich** <br/> **Monatlich** <br/> |Nein  <br/> |Gibt das ausgewählte Zeitintervall an. Sie können auf ein einzelnes Zeitintervall klicken, um Details zu diesem Intervall abzurufen. Wenn Sie beispielsweise das Intervall „Täglich“ verwenden und auf 07.07.2015 klicken, sehen Sie die nach Stunden aufgeschlüsselten Benutzerregistrierungsaktivitäten an diesem Tag.  <br/> |
|**Empfangene Anrufe** <br/> |Nein  <br/> |Gesamtanzahl der empfangenen Anrufe von allen Instanzen der Reaktionsgruppenanwendung. Wenn Sie auf dieses Element klicken, zeigt der Bericht die Anrufliste der Reaktionsgruppe für die gewählte Zeitspanne an.  <br/> |
|**Erfolgreiche Anrufe** <br/> |Nein  <br/> |Gesamtanzahl der Anrufe, die von der Reaktionsgruppenanwendung angenommen wurden. Wenn Sie auf dieses Element klicken, zeigt der Bericht die Anrufliste der Reaktionsgruppe für die gewählte Zeitspanne an.  <br/> |
|**Angebotene Anrufe** <br/> |Nein  <br/> |Gesamtanzahl der Anrufe, die an einen Reaktionsgruppenvertreter weitergeleitet wurden. Wenn Sie auf dieses Element klicken, zeigt der Bericht die Anrufliste der Reaktionsgruppe für die gewählte Zeitspanne an.  <br/> |
|**Angenommene Anrufe** <br/> |Nein  <br/> |Gesamtanzahl der Anrufe, die von einem Reaktionsgruppenvertreter tatsächlich angenommen wurden. Wenn Sie auf dieses Element klicken, zeigt der Bericht die Anrufliste der Reaktionsgruppe für die gewählte Zeitspanne an.  <br/> |
|**Prozentsatz abgebrochener Anrufe** <br/> |Nein  <br/> |Gesamtanzahl der Anrufe, die von der Reaktionsgruppenanwendung empfangen, aber nicht von einem Vertreter angenommen wurden. Dies wird berechnet, indem die angenommenen Anrufe von den empfangenen Anrufen abgezogen werden und dieser Wert dann durch die Anzahl der empfangenen Anrufe geteilt wird. Wenn Sie beispielsweise 10 Anrufe empfangen haben und sieben davon beantwortet wurden, ziehen Sie sieben von 10 ab, wonach drei unbeantwortete Anrufe übrig bleiben. Dieser Wert wird dann durch 10 geteilt, woraus sich ein Prozentsatz von 30 % für abgebrochene Anrufe ergibt.  <br/> |
|**Durchschnittliche Anrufminuten pro Agent** <br/> |Nein  <br/> |Durchschnittliche Dauer, die ein Reaktionsgruppenvertreter für einen Anruf aufgewendet hat.  <br/> |
|**Durchgestellte Anrufe** <br/> |Nein  <br/> |Gesamtanzahl der Reaktionsgruppenanrufe, die aufgrund einer Timeout- oder Überlaufwarteschleife durchgestellt wurden. Wenn Sie auf dieses Element klicken, zeigt der Bericht die Anrufliste der Reaktionsgruppe für die gewählte Zeitspanne an.  <br/> |
   
