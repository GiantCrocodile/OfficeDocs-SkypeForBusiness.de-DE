---
title: Konfigurieren von Hybrid Konnektivität | Bereitstellen von Skype for Business Server 2019 Connect
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.reviewer: bjwhalen
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection:
- Hybrid
- M365-voice
- M365-collaboration
- Teams_ITAdmin_Help
- Adm_Skype4B_Online
description: Anweisungen zum Implementieren der Hybrid Konnektivität zwischen Skype for Business Server und Skype for Business Online.
ms.openlocfilehash: ab7fb32c16e57e554c702a7b0f29ba350c1eedbe
ms.sourcegitcommit: ab47ff88f51a96aaf8bc99a6303e114d41ca5c2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2019
ms.locfileid: "36160571"
---
# <a name="configure-hybrid-connectivity-between-skype-for-business-server-and-office-365"></a>Konfigurieren der Hybrid Konnektivität zwischen Skype for Business Server und Office 365

**Zusammenfassung:** In diesem Thema erfahren Sie, wie Sie die hybride Konnektivität zwischen Skype for Business Server und Microsoft Teams oder Skype for Business Online konfigurieren.  Hybrid Konnektivität ermöglicht es Ihnen, ihre lokalen Benutzer in Teams oder Skype for Business Online zu migrieren, und ermöglicht den Benutzern, Cloud-Dienste zu nutzen.
  
Bevor Sie die Schritte in diesem Thema ausführen, sollten Sie die [Plan Hybrid-Konnektivität zwischen Skype for Business Server und Office 365](plan-hybrid-connectivity.md)gelesen haben.
  
In der folgenden Tabelle sind die Aufgaben aufgeführt, die zum Konfigurieren Skype for Business Hybrid Konnektivität erforderlich sind, sowie Links zu den zugehörigen Artikeln, um weitere Informationen zu erhalten.
  
|Schritt|Beschreibung|
|:-----|:-----|
|Erstellen eines Mandanten Kontos für Office 365   <br/> |Informationen zu Office 365 finden Sie unter [Office 365](https://go.microsoft.com/fwlink/p/?LinkId=254980).  <br/> Wenn Sie sicherstellen möchten, dass Ihre Umgebung für Office 365 bereit ist, lesen Sie die [System Anforderungen](https://products.office.com/en-US/office-system-requirements).  <br/> Ausführliche Informationen zum Einrichten von Office 365 finden Sie unter [Erste Schritte mit Office 365](https://go.microsoft.com/fwlink/p/?LinkId=254982).  <br/> |
|Hinzufügen Ihrer Domäne zu Ihrem Office 365 Mandanten und Überprüfen des Besitzes  <br/> | Sie müssen Ihre Domäne Ihrem Office 365 Mandanten hinzufügen und dann die Schritte ausführen, um die Domäne mit Office 365 zu überprüfen. Dadurch wird bestätigt, dass Sie der Besitzer der Domäne sind. <br/> Wenn Sie Ihre Domäne Ihrem Office 365 Mandanten hinzufügen möchten, führen Sie die unter [Hinzufügen einer Domäne zu Office 365](https://support.office.com/en-us/article/add-a-domain-to-office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611?ui=en-US&rs=en-US&ad=US)beschriebenen Schritte aus.  <br/> |
|Einrichten Active Directory Synchronisierung  <br/> |Durch Active Directory Synchronisierung wird Ihre lokale Active Directory kontinuierlich mit Office 365 synchronisiert. Auf diese Weise können Sie synchronisierte Versionen aller Benutzerkonten und Gruppen erstellen.  <br/> <br> **Wichtig:** Sie müssen die Ad-Konten für alle Skype for Business Benutzer in Ihrer Organisation zwischen Ihren lokalen und Online Bereitstellungen synchronisieren, auch wenn Benutzer nicht in Teams oder Skype for Business Online verschoben werden. Wenn Sie nicht alle Benutzer synchronisieren, funktioniert die Kommunikation zwischen lokalen und Online Benutzern in Ihrer Organisation möglicherweise nicht wie erwartet. Weitere Informationen finden Sie unter [configure Azure AD Connect for Hybrid Environments](configure-azure-ad-connect.md).         |
| Konfigurieren von Skype for Business Hybrid | Es gibt drei grundlegende Schritte: <br><br> 1. Konfigurieren Sie die lokale Umgebung für die Zusammenlegung mit Office 365. <br> 2. Konfigurieren Sie Ihre lokale Umgebung, um Office 365 zu Vertrauen und den freigegebenen SIP-Adressraum mit Office 365 zu aktivieren.<br> 3. Aktivieren Sie den freigegebenen SIP-Adressraum in Ihrem Office 365 Mandanten. <br><br> Wenn Sie darüber hinaus Exchange lokal haben, können Sie OAuth zwischen Ihrer lokalen Exchange-Umgebung und Skype for Business Online Umgebungen konfigurieren. <br> <br>Weitere Informationen finden Sie unter [configure Skype for Business Hybrid](configure-federation-with-skype-for-business-online.md).
|Migrieren von Pilotbenutzern  <br/> |Nachdem Sie die Schritte zum Vorbereiten und Konfigurieren Ihrer Umgebung für Teams oder Skype for Business Online abgeschlossen haben, können Sie mit dem Verschieben von Pilotbenutzern zu Ihrem Online Office 365-Mandanten beginnen. Weitere Informationen finden Sie unter [Migrieren von Benutzern von lokal zu Skype for Business Online](move-users-from-on-premises-to-skype-for-business-online.md) und [Migrieren von Benutzern von lokal in Microsoft Teams](move-users-from-on-premises-to-Teams.md).  <br/> |