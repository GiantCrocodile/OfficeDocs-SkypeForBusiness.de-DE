---
title: Auswählen von Übersetzungsregeln
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 3/24/2015
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.lscp.VoiceTrunkSelRule
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 55776a94-4888-4436-a3b6-0e6f8252e392
description: Enterprise-VoIP erfordert, dass alle Wählzeichenfolgen in das e. 164-Format für die inverssuche (RNL) normalisiert werden. Der Trunkpeer (also das zugeordnete Gateway, Nebenstellensystem oder der zugeordnete SIP-Trunk) erfordert möglicherweise, dass die Nummern in einem lokalen Wählformat vorliegen. Um Nummern aus dem E.164-Format in ein lokales Wählformat zu übersetzen, können Sie optional eine oder mehrere Übersetzungsregeln definieren, mit denen der Anforderungs-URI vor dem Routen an den Trunkpeer geändert wird. Sie können beispielsweise eine Übersetzungsregel erstellen, mit der die Vorwahl +44 aus einer Wählzeichenfolge entfernt und durch 0144 ersetzt wird.
ms.openlocfilehash: ab2a39442ce41f96769668d19de0694d4a464a4b
ms.sourcegitcommit: e577b4bdf3827fdfaf4482928adde177a64e4406
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
---
# <a name="select-translation-rules"></a>Auswählen von Übersetzungsregeln
 
 Enterprise-VoIP erfordert, dass alle Wählzeichenfolgen in das e. 164-Format für die inverssuche (RNL) normalisiert werden. Der Trunkpeer (also das zugeordnete Gateway, Nebenstellensystem oder der zugeordnete SIP-Trunk) erfordert möglicherweise, dass die Nummern in einem lokalen Wählformat vorliegen. Um Nummern aus dem E.164-Format in ein lokales Wählformat zu übersetzen, können Sie optional eine oder mehrere Übersetzungsregeln definieren, mit denen der Anforderungs-URI vor dem Routen an den Trunkpeer geändert wird. Sie können beispielsweise eine Übersetzungsregel erstellen, mit der die Vorwahl +44 aus einer Wählzeichenfolge entfernt und durch 0144 ersetzt wird.
  
> [!IMPORTANT]
> Die Möglichkeit, einen Enterprise-VoIP-Routing testen eine oder mehrere Übersetzungsregeln zugeordnet ist als Alternative zum Konfigurieren von Übersetzungsregeln für den trunkpeer verwendet werden soll. Ordnen Sie Übersetzungsregeln nicht mit einer Enterprise-VoIP-Routing testen, wenn Sie Übersetzungsregeln für den trunkpeer konfiguriert haben, da zwischen die zwei Regeln Konflikte auftreten könnten. 
  
Klicken Sie auf eine Regel in der Liste und anschließend auf **OK**, um eine vorhandene Übersetzungsregel zu verwenden.
  
Ausführliche Informationen zu den verschiedenen Verfahren, die Sie mithilfe der Skype für Business Server-Systemsteuerung ausführen können, finden Sie unter [Verwalten von Skype für Business Server 2015](../../manage/manage.md).
  
