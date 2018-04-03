---
title: Bereitstellen von Skype Room Systems v2
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 2/6/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.custom: Strat_SB_Admin
ms.assetid: 678689e4-d547-499b-be64-7d8f16dd8668
description: Lesen Sie in diesem Thema erfahren Sie Skype Raum Systemen v2 und wie es mit Exchange und Skype für Business Server 2015 integriert ist.
ms.openlocfilehash: 54dc3d42d406fea2bdefcac5eb726dd77fde078f
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="deploy-skype-room-systems-v2"></a>Bereitstellen von Skype Room Systems v2
 
Lesen Sie in diesem Thema erfahren Sie Skype Raum Systemen v2 und wie es mit Exchange und Skype für Business Server 2015 integriert ist.
  
In diesem Thema werden zum Erstellen von Skype Raum Systemen v2 in Microsoft Exchange und Skype für Business Server 2015 verwendeten Konten vorgestellt. Bereitstellung Anweisungen für Skype Raum Systemen v2 Geräte wird unter [Konfigurieren einer Skype Raum Systemen v2 Konsole](console.md)behandelt. Ihre Infrastruktur weist wahrscheinlich eine der folgenden Konfigurationen auf:
  
- Online-Bereitstellung: vollständig auf Office 365-Umgebung Ihrer Organisation bereitgestellt wird. Weitere Informationen finden Sie unter [Bereitstellen von Skype Raum Systemen v2 mit Office 365](with-office-365.md).
    
- Lokale Bereitstellung: Ihrer Organisation sind, die es verwaltet, Server, auf dem Active Directory, Exchange und Skype für Business Server 2015 gehostet werden. Weitere Informationen finden Sie unter [Bereitstellen von Skype Raum Systemen v2 mit Skype für Business Server 2015](with-skype-for-business-server-2015.md)
    
- Hybridbereitstellung: Ihre Organisation hat eine Kombination von Diensten, mit einigen gehostet an lokalen und der über Office 365 online gehostet. Mit Skype Raum Systemen v2 werden die folgenden hybridszenarien unterstützt: 
    
  - Exchange Online mit Skype für Business Server 2015 lokal. Weitere Informationen finden Sie unter [Bereitstellen von Skype Raum Systemen v2 mit Exchange Online (Hybrid)](with-exchange-online.md).
    
  - Exchange lokal mit Skype für Business Online. Weitere Informationen finden Sie unter [Bereitstellen von Skype Raum Systemen v2 mit Exchange lokal (Hybrid)](with-exchange-on-premises.md).
    
Ihre vorhandene Konfiguration beeinflusst die Vorbereitung der Geräteinstallation.
  
Skype Raum Systemen v2 muss in Active Directory, Exchange und Skype für Business "Benutzerkonto" zugewiesen werden soll. Das Konto wird zum Zugriff auf die Besprechung Kalender und Skype für Business Connectivity herstellen. Benutzer können dieses Konto buchen, indem sie eine Besprechung mit ihm planen. Skype Raum Systemen v2 werden diese Besprechung teilnehmen und verschiedene Features für die Besprechungsteilnehmer bereitstellen können.
  
> [!IMPORTANT]
> Ohne Benutzerkonto kann keine dieser Funktionen verwendet werden. 
  
Jedes Benutzerkonto ist für ein einzelnes Skype Raum Systemen v2 Gerät eindeutig und erfordert einige Setup:
  
- Das Benutzerkonto muss ordnungsgemäß konfiguriert werden.
    
- Ihrer Infrastruktur muss konfiguriert werden, damit Skype Raum Systemen v2, um das Benutzerkonto zu überprüfen und die entsprechenden Microsoft-Dienste zu erreichen können.
    
> [!IMPORTANT]
> Es wird dringend empfohlen, das Konto rechtzeitig vor der eigentlichen Hardwareinstallation zu erstellen. Im Idealfall beginnen Sie zwei bis drei Wochen vor der Installation mit der Kontovorbereitung. 
  
Sie können ein Benutzerkonto als das Ressourcenkonto vorstellen, die Personen als einen des Raums oder eine Besprechung Konferenzraum des Kontos zu erkennen. Wenn Sie eine Besprechung in diesem Konferenzraum planen möchten, laden Sie das Konto zu dieser Besprechung ein. Um Skype Raum Systemen v2 möglichst effektiv zu verwenden, führen Sie identisch mit dem Benutzerkonto, das jeweils zugeordnet ist.
  
Wenn bereits ein Postfach-Ressourcenkonto festgelegt ist für die Besprechung Speicherplatz, an dem Sie Skype Raum Systemen v2 installiert sind, können Sie dieses Ressourcenkontos in ein Benutzerkonto ändern. Wenn das erledigt ist, müssen Sie, nur das Benutzerkonto zu einem Gerät, v2 Skype Raum Systeme hinzuzufügen. Sehen Sie sich dazu die unten gezeigten Beispiele für die Einrichtung von Benutzerkonten an.
  
Durch zusätzliche Konfiguration kann die Remoteverwaltung Microsoft Operations Management Suite (OMS) verwenden, wie beschrieben in [Planen Skype Raum v2 systemverwaltung mit OMS](../../plan-your-deployment/clients-and-devices/oms-management.md) [Bereitstellen Skype Raum v2 systemverwaltung mit OMS](with-oms.md)und [Verwalten Skype-Chatroom-Systemen v2 Geräte mit OMS](../../manage/skype-room-systems-v2/oms.md). 
  
## <a name="basic-configuration"></a>Basiskonfiguration

Diese Eigenschaften darstellen, die Mindestkonfiguration für ein Benutzerkonto Skype Raum Systemen v2 entwickelt. Möglicherweise muss Ihr Benutzerkonto darüber hinaus konfiguriert werden.
  
|**Eigenschaft**|**Zweck**|
|:-----|:-----|
|Exchange-Postfach (Exchange 2013 SP1 oder höher, oder Exchange Online)  <br/> |Aktivieren das Konto mit einem Exchange-Postfach verleiht dem Benutzerkonto die Fähigkeit zum Empfangen und Senden von e-Mail-Nachrichten und Besprechungsanfragen und um einen Kalender Besprechungen auf dem Skype Raum Systemen v2-Gerät anzuzeigen. Das Skype Raum Systemen v2 Postfach muss ein Raumpostfach sein.  <br/> |
|Skype für Unternehmen ist aktiviert.  <br/> |Skype für Unternehmen muss, um die verschiedenen Konferenzfunktionen, wie Videokonferenzen, Instant Messaging und Bildschirmfreigabe-verwenden aktiviert sein. Skype für Business Online und Skype für Business Server werden unterstützt.  <br/> |
|Kennwort aktiviert  <br/> |Das Benutzerkonto muss mit einem Kennwort aktiviert werden, oder es kann nicht mit Exchange oder Skype für Business Server authentifizieren.  <br/> |
   
## <a name="advanced-configuration"></a>Erweiterte Konfiguration

Während die Eigenschaften für die grundlegende Konfiguration das Benutzerkonto in einer einfachen Umgebung eingerichtet werden zulässig, es ist möglich Ihrer Umgebung hat die anderen Einschränkungen auf Directory-Konten, die erfüllt sein müssen, Reihenfolge für Skype Raum Systemen v2 erfolgreich verwenden die Benutzer: Konto.
  
|**Eigenschaft**|**Zweck**|
|:-----|:-----|
|Zertifikatbasierte Authentifizierung  <br/> |Zertifikate möglicherweise für Exchange und Skype für Business Server erforderlich. Zum Bereitstellen von Zertifikaten können Sie diese laden, wenn Sie als Administrator angemeldet sind.  <br/> |
   
Die beste Möglichkeit zum Einrichten von Benutzerkonten ist von remote Windows PowerShell konfigurieren. [Microsoft stellt Skripts](https://go.microsoft.com/fwlink/?linkid=870105) , die helfen neue Benutzerkonten erstellen oder vorhandene Ressourcenkonten, mit denen Sie damit können Sie diese in kompatibel Skype Raum Systemen v2-Benutzerkonten aktivieren zu überprüfen.
  
Wenn Sie die Benutzeroberfläche von Office 365 über Windows PowerShell-Cmdlets verwenden möchten, können einige Schritte manuell ausgeführt werden. Finden Sie unter [Erstellen eines Geräts-Kontos mithilfe von Office 365](https://technet.microsoft.com/en-us/itpro/surface-hub/create-a-device-account-using-office-365).
  
## <a name="see-also"></a>Siehe auch

#### 

[Planen von Skype Raum Systemen v2](../../plan-your-deployment/clients-and-devices/skype-room-systems-v2-0.md)
  
[Konfigurieren einer Skype Raum Systemen v2-Konsole](console.md)
  
[Verwalten von Skype Raum Systemen v2](../../manage/skype-room-systems-v2/skype-room-systems-v2.md)
