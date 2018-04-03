---
title: 'Skype for Business Server 2015: Rechner zur Kapazitätsplanung'
ms.author: heidip
author: microsoftheidi
ms.date: 2/1/2018
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: bc4d93b1-0c38-4bf8-8b65-692ff3e2446d
description: 'Zusammenfassung: Informationen zur Verwendung des Rechner Kapazität.'
ms.openlocfilehash: 5d94dab15b104703efc76b227e6e9dd1286f9955
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="skype-for-business-server-2015-capacity-planning-calculator"></a>Skype for Business Server 2015: Rechner zur Kapazitätsplanung
 
**Zusammenfassung:** Wie Sie das Kapazitätsrechnertool verwenden.
  
[Skype für Business Server 2015 Kapazitätsrechner](https://www.microsoft.com/en-us/download/details.aspx?id=51196) erweitert die [Skype für Business 2015 Planning Tool](https://www.microsoft.com/en-us/download/details.aspx?id=50357) und die Dokumentation an [Ihre Skype für Business Server 2015 Bereitstellung planen](https://technet.microsoft.com/en-us/library/dn951427). Verwenden Sie den Rechner, nachdem Sie die Anleitung gelesen und mithilfe des Planungstools eine empfohlene Topologie erstellt haben.
  
Die Skype für Business Server 2015 Kapazitätsrechner hilft bestimmen Sie die Anforderungen an die Server basierend auf der Anzahl von Benutzern und der Kommunikationstools, die Ihrer Organisation verwendet werden. Nachdem Sie Ihr Benutzerprofil und die Funktionen festgelegt haben, die Sie Ihren Nutzern zur Verfügung stellen möchten, verwenden Sie den Rechner zur Bestimmung der Anzahl von Servern, des Speicherumfangs und der Bandbreite, die erforderlich sein wird. Diese Version des Rechners bietet keine Anleitungen in Hinblick auf Datenträger-E/A-Anforderungen.
  
Den besten Nutzen erzielen Sie mit dem Rechner, wenn Sie genaue und ausführliche Informationen zu Ihrem speziellen Benutzerprofil haben. Beispielsweise können der Prozentsatz von VoIP-aktivierten Benutzern, der Durchschnitt der Anrufe pro Benutzer und Stunde, die Anrufdauer und der Prozentsatz von gleichzeitigen Benutzern in Konferenzen einen großen Unterschied hinsichtlich der Serveranforderungen ausmachen. Die Genauigkeit der Empfehlungen, die vom Rechner erstellt werden, hängt von der Genauigkeit der Informationen ab, die Sie bereitgestellt haben.
  
Nachdem Sie das Planungstool und der Planung Kapazitätsrechner verwendet haben, sollten Sie simulieren Ihrer vorgeschlagenen und geplanten laden, um sicherzustellen, dass Skype für Business Server 2015 angemessen bereitgestellt wird. Verwenden Sie zur Ausführung Belastungstests bei simulierten Auslastung der [Skype für Business Server 2015 Stress and Performance-Tool](https://www.microsoft.com/en-us/download/details.aspx?id=50367) bei [Skype für Business Server 2015 Stress and Performance-Tool](https://technet.microsoft.com/en-us/library/mt631400.aspx)dokumentiert.
  
## <a name="using-the-capacity-calculator"></a>Arbeiten mit dem Kapazitätsrechner

Der Rechner ist eine Microsoft Excel-Kalkulationstabelle. Die Felder für Ihre Eingaben sind orangefarben gehalten. Standardwerte werden in den Zellen (beispielsweise 80.000 Benutzern in einem Pool mit zwölf Front-End-Servern) eingegeben, aber Sie sollten diese Werte entsprechend der Anforderungen Ihrer Organisation ändern. 
  
Das Nutzungsmodell enthält die folgenden Abschnitte. Damit Sie Ihre Kapazitätsanforderungen berechnen können, geben Sie Daten gemäß der Beschreibung von oben nach unten zeilenweise ein: 
  
 **Chat und Anwesenheit (Instant Messaging/Presence, IM/P)**
  
- Geben Sie unter **Anzahl der Nutzer** die Anzahl von Nutzern ein, die gleichzeitig angemeldet sein werden. Diese Anzahl entspricht meist 80 % der Gesamtzahl der bereitgestellten Nutzer. In den meisten Situationen werden 100 % der gleichzeitigen Nutzer für Chat und Anwesenheit aktiviert. Der Standardwert ist 80.000.
    
- **Durchschnittliche Anzahl von Kontakten in der Kontaktliste** gibt die Anzahl von Kontakten an, die zur Überprüfung Ihrer Systemanforderungen verwendet wird. Diese Anzahl ist festgelegt und sollte von Ihnen nicht geändert werden.
    
 **Enterprise-VoIP**
  
- Geben Sie in **Nutzer, für die Enterprise-VoIP aktiviert ist** den Prozentsatz Ihrer Nutzer an, für die Enterprise-VoIP aktiviert ist. Der Standardwert ist 60 %. 
    
- Geben Sie in **Durchschnittliche Anzahl von Anrufen pro Nutzer pro Stunde (Spitze)** die Anzahl von Anrufen pro Stunde ein, die Sie für durchschnittliche Nutzer als Teilnehmer zu Spitzenlastzeiten erwarten. Der Standardwert ist 4. 
    
- Geben Sie in **Prozentsatz der Anrufe, die Medienumgehung nutzen** den Prozentsatz der Anrufe ein, die von Ihren Nutzern getätigt, aber nicht über den Vermittlungsserver abgewickelt werden. Der Standardwert ist 65 %, könnte aber niedriger ausfallen, wenn Sie geografisch weit verteilt sind oder einen hohen Prozentsatz an Nutzern haben, die zu Hause arbeiten.
    
- **Prozentsatz der VoIP-Benutzer beteiligt UC-PSTN-Anrufe**Geben Sie den Prozentsatz der Anrufe von Ihrer Organisation die UC-zu-PSTN-Anrufe sind. Der Standardwert ist 60 %.
    
- **In Prozentsatz der VoIP-Nutzer, die an UC-UC-Anrufen beteiligt sind** ist der Prozentsatz der Nutzer enthalten, die zwar für Enterprise-VoIP, aber nur für UC-UC-Anrufe aktiviert sind. Diese Anzahl wird auf Basis des Werts berechnet, den Sie in **Prozentsatz der VoIP-Nutzer, die an UC-PSTN-Anrufen beteiligt sind** eingegeben haben. 
    
 **Konferenzen**
  
- Geben Sie in **Prozentsatz der Nutzer in gleichzeitigen Konferenzen** den Prozentsatz an Nutzern ein, die gleichzeitig an einer Konferenz teilnehmen werden. Der Standardwert ist 5 %. 
    
- Geben Sie in **Prozentsatz der Konferenzen nur mit Gruppen-Chat (kein VoIP)** den Prozentsatz an Konferenzen ein, für die ausschließlich Chat genutzt wird, d. h. Konferenzen ganz ohne Audio. Der Standardwert ist 10 %.
    
- Geben Sie in **Prozentsatz der Nutzer, die Einwahlkonferenzen verwenden** den Prozentsatz an Teilnehmern ein, die Einwahlkonferenzen gleichzeitig verwenden werden. Der Standardwert ist 15 %.
    
- Geben Sie in **Prozentsatz der Konferenzen mit VoIP** den Prozentsatz an Konferenzen ein, die Audio einschließen werden. 
    
  - Wenn 20 % Ihrer VoIP-Konferenzen auch normale Videoelemente umfassen, aktivieren Sie das Kontrollkästchen **Einschließlich Video (kein Multiview)**.
    
  - Wenn 20 % Ihrer Konferenzen auch Multiview-Videoelemente umfassen, aktivieren Sie das Kontrollkästchen **Einschließlich Multiview**.
    
  - Wenn 50 % der Konferenzen VoIP auch die Anwendungsfreigabe angegeben wird, aktivieren Sie das Kontrollkästchen **einschließlich Anwendungsfreigabe** .
    
  - Wenn 20 % Ihrer VoIP-Konferenzen Datenuploads umfassen, zum Beispiel Microsoft PowerPoint-Präsentationen, aktivieren Sie das Kontrollkästchen **Einschließlich Webkonferenzen**.
    
 **Mobilität**
  
- **Prozentsatz der Benutzer für Mobilität aktiviert sind**Geben Sie den Prozentsatz der Benutzer die Verbindung mit Skype für Business Server mit mobilen Geräten aktiviert wird. Der Standardwert ist 40 %. 
    
Wenn Sie alle erforderliche Informationen eingegeben haben, schätzt die kapazitätsrechner für Ihre Anforderungen an. Die gelben Zellen anzeigen berechneten Werte für CPU, Arbeitsspeicher und bandbreitenanforderungen basierend auf in Skype für Business Server Performance Übungseinheiten ausgeführten Tests. Nummern werden bereitgestellt als Richtlinie nicht jedes einzelne Variante getestet und validiert. Die folgenden Werte werden berechnet: 
  
- **Front-End-CPU:** Prozentsatz der CPU-Nutzung, wenn die gesamte Last von einem Front-End-Server verarbeitet wurde, der dieselben Spezifikationen hat wie der Server, der für die Tests verwendet wurde (siehe Beschreibung am Ende dieses Themas).
    
- **Netzwerk in MBit/s:** Bandbreitenanforderungen in Megabit pro Sekunde (MBit/s) für die entsprechende Arbeitsauslastung.
    
- **Arbeitsspeicher in GB:** Arbeitsspeicher in Gigabyte (GB), der für die entsprechende Arbeitsauslastung erforderlich ist.
    
In den grünen Zellen werden Empfehlungen für das Nutzungsmodell angezeigt, das Sie eingegeben haben. 
  
- **Gesamtzahl der Front-End-Server:** Die Anzahl von erforderlichen physischen Servern basiert auf speziell dafür vorgesehenen Servern, auf denen Skype for Business Server 2015 ausgeführt wird und die jeweils einen Dualprozessor mit sechs Kernen und 2.260 Megahertz aufweisen.
    
    Es wird empfohlen, Hyperthreading zu aktivieren, denn damit lässt sich nachweislich die Leistung von Servern verbessern, die Audio/Video unterstützen.
    
- **Edgeserver:** Die Anzahl von erforderlichen Edgeservern. Diese Anzahl basiert auf 30 % aller gleichzeitigen Nutzer, die über die Edgeserver kommunizieren. Dieser Prozentsatz kann im Rechner nicht geändert werden. 
    
- **Speicher für die Dienste Archivierung/Aufzeichnung von Kommunikationsdatensätzen/Quality of Experience:** Die Anzahl von Speichern, die für Archivierungs- oder Überwachungsfeatures erforderlich sind, sofern diese in Ihrer Organisation aktiviert sind.
    
- **Erforderliche Back-End-Datenbankserver (erforderliche Pools):** Die Anzahl von Back-End-Datenbankservern, die erforderlich sind, damit die ausgewählte Auslastung unterstützt werden kann.
    
Die Zeile neben „Gesamtzahl der Front-End-Server“ enthält zusätzlich weitere Informationen zu der Last auf den Servern und im Netzwerk für alle geplanten Auslastungen zusammengenommen.
  
- **Durchschnittliche CPU-Auslastung:** Die durchschnittliche CPU-Nutzung pro Front-End-Server.
    
- **Netzwerk in MBit/s:** Die Bandbreitenzuteilung, die erforderlich ist, damit das von Ihnen eingegebene Nutzungsmodell unterstützt wird.
    
- **Arbeitsspeicher in GB:** Der Arbeitsspeicher in Gigabyte, der für jeden Front-End-Server erforderlich ist.
    
### <a name="adjusting-for-your-processors"></a>Anpassen an Ihre Prozessoren

Für alle CPU-Nutzungswerte auf dem Arbeitsblatt wird angenommen, dass jeder Server einen Dualprozessor mit sechs Kernen und 2,26 GHz, mindestens 32 GB Arbeitsspeicher und mindestens 8 10.000-U/min-Festplattenlaufwerke mit mindestens 72 GB freiem Speicherplatz hat. 
  
Wenn Ihre Server andere Prozessoren haben, können Sie die Werte entsprechend Ihrer Hardware anpassen.
  
