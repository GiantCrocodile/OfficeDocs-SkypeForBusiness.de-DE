---
title: Zulassen, dass Skype for Business-Benutzer Skype-Kontakte hinzufügen
ms.reviewer: ''
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.topic: article
ms.assetid: 08666236-1894-42ae-8846-e49232bbc460
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
- Setup
- LIL_Placement
description: 'Hier erfahren Sie, wie Sie Personen, die Skype for Business nutzen, Skype for Business-Benutzer von außerhalb Ihrer Organisation kontaktieren und diese Ihrer Kontaktliste hinzufügen. '
ms.openlocfilehash: 71282fe105c85cadca9aab341fc1b5e6ffbe47d2
ms.sourcegitcommit: 36f7ec432090683aedb77a5bd7856e1b10af2a81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2020
ms.locfileid: "44164474"
---
# <a name="let-skype-for-business-users-add-skype-contacts"></a>Zulassen, dass Skype for Business-Benutzer Skype-Kontakte hinzufügen

Mit Skype for Business können Ihre Benutzer nach beliebigen Benutzern von Skype - der kostenlosen App - suchen und Chatnachrichten mit ihnen austauschen. In diesem Artikel wird erläutert, was Sie tun müssen, damit die Benutzer Skype-Kontakte hinzufügen können. 
  
Sie benötigen [Administratorberechtigungen](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d?ui=en-US&rs=en-US&ad=US) in Microsoft 365 oder Office 365, um dies zu tun.

![Ein Symbol mit dem Skype for Business-Logo](../images/sfb-logo-30x30.png) **Unter Verwendung des Skype for Business Admin Centers**
  
1. Registrieren Sie sich [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home#/homepage)bei Ihrem Microsoft 365-oder Office 365-Administratorkonto.
    
2. Wechseln Sie im Admin Center zu **Admin Centers** > **für Skype for Business**. 
    
    ![Choose the Skype for Business admin center.](../images/376a7a45-e6e3-4716-be09-d2f294d885a2.png)
  
3. Wählen Sie unter **Skype for Business Admin Center** die Option **Organisation** > **Externe Kommunikation** aus. 
    
4. Standardmäßig können Ihre Benutzer mit allen anderen Personen weltweit kommunizieren, die Skype for Business verwenden (vorausgesetzt, Ihre Firewall ist so konfiguriert, dass sie dies zulässt). 
    
    ![Wählen Sie zulassen, dass Personen Skype for Business für die Kommunikation mit Skype verwenden.](../images/333789f8-2ea6-4bbd-805b-18130f427999.png)
  
    Wenn Sie möchten, dass Ihre Benutzer mit Skype-Benutzern chatten, ABER nicht mit anderen, die Skype for Business verwenden, wählen Sie **Nur für zulässige Domänen aktivieren** aus. Wenn Sie den Kontakt mit Skype-Benutzern ermöglichen, wird „skype.com" automatisch im Hintergrund als zulässige Domäne hinzugefügt. 
    
    Wenn Sie den Kontakt über Skype for Business von allen anderen Unternehmen weltweit mit Ausnahme bestimmter Unternehmen zulassen möchten, wählen Sie **Aktivieren mit Ausnahme der blockierten Domänen** aus. Wählen Sie dann **+** aus, um die entsprechenden Domänen hinzuzufügen. Alle Personen mit Ausnahme derer in diesen Domänen können Kontakt zu Ihnen aufnehmen. (Ein Unternehmen kann diese Option z. B. wählen, wenn ein Rechtsstreit vorliegt und sichergestellt werden muss, dass kein Kontakt zu dem anderen Unternehmen unterhalten wird.)
    
5. Wählen Sie **Zulassen, dass Skype for Business zur Kommunikation mit Skype-Benutzern außerhalb Ihres Unternehmens verwendet wird**. 
    
6.  Wenn Sie die Windows-Firewall verwenden, öffnet Skype for Business die erforderlichen Ports automatisch.
    
    Wenn Ihre Organisation eine andere Lösung verwendet, um die Internet Verbindung von Computern in Ihrem Netzwerk zu beschränken, stellen Sie sicher, dass Clientcomputer auf alle [IP-Adressen und URLs](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2) für Skype-Konnektivität und die Skype-Verzeichnissuche zugreifen können. Dafür kann es erforderlich sein, sie der Liste für zugelassene ausgehende Verbindungen in Ihrer Firewall oder Proxy-Infrastrukturkonfiguration hinzuzufügen.
    
7. **WARTEN SIE MIT DEM TEST BIS ZU 24 STUNDEN**. Bei jeder Änderung der Einstellungen für externe Kommunikation kann es bis zu 24 Stunden dauern, bis die Änderungen in allen Rechenzentren übernommen wurden.
    
8. Zeigen Sie Ihren Benutzern, wie sie Skype-Kontakte finden und zu ihrer Liste mit Skype for Business-Kontakten hinzufügen können. Verweisen Sie die Benutzer auf [Suchen nach Personen in Skype for Business](https://support.office.com/article/b12500ef-e37f-4d22-aade-c11277e53f19).
    
## <a name="test-and-troubleshoot"></a>Tests und Problembehandlung

Um Ihr Setup zu testen, benötigen Sie einen Kontakt in Skype, der sich nicht hinter der Firewall Ihrer Firma befindet. Der Kontakt kann mit einem Gmail-Konto, Outlook.com-Konto oder einem anderen E-Mail-Kontotyp angemeldet sein.
  
1. Warten Sie nach einer Änderung der Einstellungen für externe Kommunikation **BIS ZU 24 STUNDEN, BEVOR SIE TESTS DURCHFÜHREN**.
    
2. Melden Sie sich bei Skype for Business ab und dann wieder an, damit Sie die Option zum Durchsuchen des Skype-Verzeichnisses sehen. 
    
    ![Wenn das Skype-Verzeichnis hervorgehoben ist, können Sie nach Personen suchen, die Skype-Konten haben.](../images/76ee9fab-1ac3-4f4a-9569-f5f2606dbb7a.png)
  
3. Suchen Sie in Skype for Business nach Ihrem Kontakt in Skype, und senden Sie eine Chatanfrage. 
    
    Wenn Sie die Meldung erhalten, dass Sie aufgrund einer Unternehmensrichtlinie nicht gesendet werden konnte, müssen Sie Ihre [Firewalleinstellungen](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2)überprüfen. 
    
4. Eine weitere Möglichkeit, zu testen, ob die Firewall das Problem darstellt: Gehen Sie zu einem Ort mit WLAN, der sich nicht hinter Ihrer Firewall befindet (zum Beispiel in ein Café), und senden Sie mit Skype for Business eine Chatanfrage an Ihren Skype-Kontakt. 
    
   - **Wenn Sie Ihrem Skype-Kontakt eine Anfrage gesendet haben, die dieser nicht erhalten hat**, bitten Sie ihn, Ihnen eine Chatanfrage zu senden. Wenn das Problem darin bestand, eine Verbindung zwischen Skype und Skype for Business herzustellen, ist das Problem damit oft gelöst.
    
   - Wenn die Nachricht im Café gesendet wird, an Ihrem Arbeitsplatz aber nicht, wissen Sie, dass die Firewall das Problem darstellt. 
    
## <a name="what-you-can-and-cant-do"></a>Was möglich und was nicht möglich ist

- **Skype for Businessfür Mac** ist es nicht möglich, nach Skype-Kontakten zu suchen und mit ihnen zu kommunizieren.
    
- Wenn die Verzeichnissuche aktiviert ist, können Sie nach Skype-und Skype for Business-Benutzern suchen und diese finden. Wenn Sie Sie aus irgendeinem Grund nicht finden können, indem Sie das Verzeichnis durchsuchen, können Sie Ihnen eine Kontakt Anfrage senden und diese dann bei Skype anmelden und akzeptieren, damit Sie mit Ihnen chatten können. 
    
- Chat-Nachrichtenverbindungen mit anderen Chat-Dienstanbietern wie Google oder Facebook sind nicht möglich. Sie können Skype for Business nicht zum Senden von Mobiltelefon-Textnachrichten verwenden.

- Es ist nicht möglich, Audio-oder Videoanrufe zwischen einem Skype-Kontakt und einem Skype for Business-Kontakt aufzuzeichnen.
    
## <a name="what-features-are-available-when-adding-skype-contacts"></a>Welche Funktionen sind beim Hinzufügen von Skype-Kontakten verfügbar?

Skype-Kontakte, die sich mit Ihrem Microsoft-Konto (vormals Windows Live ID) angemeldet haben, können einige, aber nicht alle Funktionen erhalten, wenn Sie mit Ihren Skype for Business-Benutzern sprechen.
  
|**Für Skype-Kontakte verfügbar**|**Für Skype-Kontakte nicht verfügbar**|
|:-----|:-----|
| Videounterhaltungen <br/>  Chatnachrichten zwischen zwei Personen <br/>  Anwesenheit <br/> | Chatunterhaltungen mit mehreren Personen <br/>  Audio- und Videounterhaltungen mit drei oder mehr Personen <br/>  Desktop- und Programmfreigabe <br/> |
   
[!INCLUDE [LinkedIn Learning Info](../../common/office/linkedin-learning-info.md)]
   
## <a name="related-topics"></a>Verwandte Themen

[Benutzern gestatten, externe Skype for Business-Benutzer zu kontaktieren](allow-users-to-contact-external-skype-for-business-users.md)
  
[Einrichten von Skype for Business Online](set-up-skype-for-business-online.md)

  
 
