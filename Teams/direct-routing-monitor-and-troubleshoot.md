---
title: Überwachung und Problembehandlung von direktem Routing
ms.reviewer: ''
ms.author: crowe
author: CarolynRowe
manager: serdars
audience: ITPro
ms.topic: troubleshooting
ms.service: msteams
localization_priority: Normal
search.appverid: MET150
ms.collection:
- M365-voice
appliesto:
- Microsoft Teams
f1.keywords:
- NOCSH
description: Erfahren Sie, wie Sie die direkte Routingkonfiguration überwachen und behandeln können, einschließlich Session Border Controllers, Direct Routing-Komponenten und Telecom Trunks.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 52ab594b901606ccf7c3b43fc8484d989c248fcd
ms.sourcegitcommit: a9e16aa3539103f3618427ffc7ebbda6919b5176
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "43901910"
---
# <a name="monitor-and-troubleshoot-direct-routing"></a>Überwachung und Problembehandlung von direktem Routing

In diesem Artikel wird beschrieben, wie Sie Ihre direkte Routing Konfiguration überwachen und beheben können. 

Die Möglichkeit zum tätigen und empfangen von Anrufen mithilfe des direkten Routings umfasst die folgenden Komponenten: 

- Session Border Controllers (SBCS) 
- Direkte Routing Komponenten in der Microsoft-Cloud 
- Telekom-Stämme 

Wenn Probleme bei der Problembehandlung auftreten, können Sie einen Supportfall mit Ihrem SBC-Anbieter oder Microsoft öffnen. 

Microsoft arbeitet an der Bereitstellung weiterer Tools für die Problembehandlung und Überwachung. Bitte überprüfen Sie die Dokumentation regelmäßig auf Updates. 

## <a name="monitoring-availability-of-session-border-controllers-using-session-initiation-protocol-sip-options-messages"></a>Überwachen der Verfügbarkeit von Sitzungs Grenz Controllern mithilfe von SIP-Options Meldungen (Session Initiation Protocol)

Das direkte Routing verwendet SIP-Optionen, die von den Session Border Controllern zur Überwachung des SBC-Status gesendet werden. Vom mandantenadministrator sind keine Aktionen erforderlich, um die Überwachung der SIP-Optionen zu aktivieren. Die gesammelten Informationen werden berücksichtigt, wenn Routingentscheidungen getroffen werden. 

Wenn beispielsweise für einen bestimmten Benutzer mehrere SBCS verfügbar sind, um einen Anruf weiterleiten zu können, werden bei der direkten Weiterleitung die SIP-Optionsinformationen berücksichtigt, die von jedem SBC empfangen werden, um das Routing zu ermitteln. 

Das folgende Diagramm zeigt ein Beispiel für die Konfiguration: 

![Konfigurationsbeispiel für SIP-Optionen](media/sip-options-config-example.png)

Wenn ein Benutzer einen Anruf an Number + 1 425 \<mit sieben Ziffern> durchführt, wird die Route von einem direkten Routing ausgewertet. Die Route umfasst zwei SBCS: sbc1.contoso.com und sbc2.contoso.com. Beide SBCS haben in der Route dieselbe Priorität. Vor der Auswahl eines SBC bewertet der Routingmechanismus die Integrität des SBCS basierend auf dem Zeitpunkt, zu dem der SBC die SIP-Optionen beim letzten Mal gesendet hat. 

Ein SBC wird als "fehlerfrei" eingestuft, wenn beim Senden des Anrufs Statistiken angezeigt werden, dass die SBC-Optionen jede Minute gesendet werden.  

Wenn ein Anruf durchgeführt wird, gilt die folgende Logik:

- Der SBC wurde um 11:00 Uhr gekoppelt.  
- Der SBC sendet Optionen für 11:01 Uhr, 11:02 Uhr usw.  
- Bei 11:15 führt ein Benutzer einen Anruf aus, und der Routingmechanismus wählt diesen SBC aus. 

Beim direkten Routing werden die regulären Intervall Optionen dreimal verwendet (das reguläre Intervall beträgt eine Minute). Wenn Optionen in den letzten drei Minuten gesendet wurden, gilt der SBC als fehlerfrei.

Wenn der SBC im Beispiel Optionen zu einem beliebigen Zeitraum zwischen 11:12 und 11:15 Uhr (der Zeitpunkt, zu dem der Anruf getätigt wurde) gesendet hat, wird er als fehlerfrei angesehen. Wenn dies nicht der Fall ist, wird der SBC von der Route herabgestuft. 

Herabstufung bedeutet, dass der SBC nicht zuerst getestet wird. Beispielsweise haben wir sbc1.contoso.com und sbc2.contoso.com mit gleicher Priorität.  

Wenn sbc1.contoso.com die SIP-Optionen nicht wie zuvor beschrieben in regelmäßigen Abständen sendet, wird es herabgestuft. Als nächstes versucht sbc2.contoso.com den Anruf. Wenn sbc2. contoso. con den Anruf nicht übermitteln kann, wird der sbc1.contoso.com (degradiert) erneut versucht, bevor ein Fehler generiert wird. 

Wenn zwei (oder mehr) SBCS in einer Route als "gesund" und "gleich" gelten, wird Fisher-Yates shuffle angewendet, um die Anrufe zwischen dem SBCS zu verteilen.

## <a name="monitor-call-quality-analytics-dashboard-and-sbc-logs"></a>Überwachen von Anruf Qualitätsanalyse-Dashboard und SBC-Protokollen 
 
In einigen Fällen, besonders während der anfänglichen Kopplung, gibt es möglicherweise Probleme im Zusammenhang mit der Fehlkonfiguration des SBCS oder des Direct Routing-Diensts. 

Sie können die folgenden Tools verwenden, um Ihre Konfiguration zu überwachen:  
 
- Anrufqualitäts-Dashboard 
- SBC-Protokolle 

Der Direct Routing-Dienst weist sehr anschauliche Fehlercodes auf, die entweder für die anrufanalyse oder für die SBC-Protokolle gemeldet wurden. 

Das Dashboard "Anrufqualität" bietet Informationen zur Anrufqualität und Zuverlässigkeit. Weitere Informationen zur Behandlung von Problemen mit der anrufanalyse finden Sie unter [aktivieren und Verwenden von Anruf Qualitäts Dashboard für Microsoft Teams und Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/using-call-quality-in-your-organization/turning-on-and-using-call-quality-dashboard) und [Verwenden von Anruf Analysen zur Behandlung schlechter Anrufqualität](https://docs.microsoft.com/SkypeForBusiness/using-call-quality-in-your-organization/use-call-analytics-to-troubleshoot-poor-call-quality). 

Bei Anruf Fehlern bietet die anrufanalyse Standard-SIP-Codes, die Ihnen bei der Problembehandlung helfen. 

![Beispiel für SIP-Code für Anruf Fehler](media/failed-response-code.png)

Anruf Analysen können jedoch nur dann hilfreich sein, wenn Anrufe die internen Komponenten des direkten Routings erreichen und Fehler auftreten. Bei Problemen mit SBC-Kopplungen oder Problemen, bei denen SIP "Invite" abgelehnt wurde (beispielsweise ist der Name des trunk-FQDN falsch konfiguriert), kann die anrufanalyse nicht helfen. Lesen Sie in diesem Fall die SBC-Protokolle. Direktes Routing sendet eine detaillierte Beschreibung der Probleme an die SBCS. Diese Probleme können aus den SBC-Protokollen gelesen werden. 
