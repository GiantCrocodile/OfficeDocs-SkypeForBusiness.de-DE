---
title: Zertifikatsanforderung (Grundlagen)
ms.author: jambirk
author: jambirk
manager: serdars
ms.date: 3/26/2015
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.dep.DeployCertRequestBasics
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 2c6b40d5-207a-4ca9-a090-e43350f4968f
description: Die Seite namens- und Sicherheitseinstellungen stellt ein Textfeld zum definieren einen Anzeigenamen ein Dropdown-Listenfeld für die Bitlänge von privaten und öffentlichen Schlüsselpaars und ein Kontrollkästchen, mit dem Sie das Zertifikat privaten Schlüssel als exportierbar markieren können.
ms.openlocfilehash: e9c70074a168b00288b931cb168b5fea210367c2
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="certificate-request-basic"></a>Zertifikatsanforderung (Grundlagen)
 
Die Seite **Namens- und Sicherheitseinstellungen** stellt ein Textfeld, um einen **Anzeigenamen**ein Dropdown-Listenfeld für die **Bitlänge** von privaten und öffentlichen Schlüsselpaars und ein Kontrollkästchen, die Ihnen ermöglicht, **Mark das Zertifikat privaten Schlüssel als definieren "Exportierbar" markieren**.
  
Beim Anzeigenamen (oder einfachen Namen) eines Zertifikats handelt es sich um einen benutzerfreundlichen und problemlos identifizierbaren Namen für den Benutzer, der das Zertifikat anzeigt.
  
Für die Bitlänge des öffentlich-privaten Schlüsselpaars kann der Wert 1024, 2048 oder 4096 festgelegt werden.
  
Aktivieren des Kontrollkästchens für **das Zertifikat privaten Schlüssel als exportierbar markieren** können das Zertifikat und der private Schlüssel exportiert und an einem anderen Computer oder Server verschoben werden. Die einzige Zeit, die dies erforderlich ist ist, wenn Sie einen Pool von Edge-Server für das Medium Mediarelay-Authentifizierungsdienst (MRAS) erstellen.
  
> [!CAUTION]
> Um die Sicherheit des Zertifikats und Schlüsselpaars zu gewährleisten, sollten Sie der Markierung auswählen privaten Schlüssel des Zertifikats als exportierbar nur, wenn dies unbedingt erforderlich ist. 
  
