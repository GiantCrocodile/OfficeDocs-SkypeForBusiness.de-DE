---
title: Übersetzungsregeln in Skype for Business Server 2015
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.date: 8/17/2015
ms.audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: IT_Skype16
ms.custom: Strat_SB_Admin
ms.assetid: 6e067bd4-4931-4385-81ac-2acae45a16d8
description: Erfahren Sie mehr über Übersetzungsregeln, und wählen Sie die Normalisierung von Zeichenfolgen in Skype für Business Server Enterprise-VoIP.
ms.openlocfilehash: ff3718e89d152a2b6c7d1c78ccaaa055d00ffcdb
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="translation-rules-in-skype-for-business-server-2015"></a>Übersetzungsregeln in Skype for Business Server 2015
 
Erfahren Sie mehr über Übersetzungsregeln, und wählen Sie die Normalisierung von Zeichenfolgen in Skype für Business Server Enterprise-VoIP.
  
 Enterprise-VoIP erfordert, dass alle Wählzeichenfolgen in das e. 164-Format für die inverssuche (RNL) normalisiert werden. Übersetzungsregeln werden für die gewählte Nummern und Rufnummern unterstützt. Thetrunk Peer (d. h., die zugeordnete Gateways, private Branch Exchange, Nebenstellenanlage (PBX) oder SIP-Trunk) erfordern möglicherweise, dass Zahlen in eine lokale Wählformat sein. Um Nummern aus dem E.164-Format in ein lokales Wählformat zu übersetzen, können Sie eine oder mehrere Übersetzungsregeln definieren, mit denen der Anforderungs-URI vor dem Routen an den Trunkpeer geändert wird. Sie können beispielsweise eine Übersetzungsregel erstellen, mit der die Vorwahl +44 aus einer Wählzeichenfolge entfernt und durch 0144 ersetzt wird.
  
Durch die ausgehende Routenübersetzung auf dem Server können Sie die Konfigurationsanforderungen der einzelnen Trunkpeers für das Übersetzen von Rufnummern in ein lokales Wählformat reduzieren. Bei der Planung der Gateways und wie viele Gateways zuordnen zu einer bestimmten Mediation Server-Cluster, es kann hilfreich sein, Gruppe Trunk Peers mit ähnlichen lokale Wählvorgang Anforderungen. Dies kann die Anzahl von erforderlichen Übersetzungsregeln und den Zeitaufwand für das Schreiben dieser Regeln reduzieren.
  
> [!IMPORTANT]
> Ein Enterprise-VoIP-trunkkonfiguration eine oder mehrere Übersetzungsregeln zuordnen sollte als Alternative zum Konfigurieren von Übersetzungsregeln für den trunkpeer verwendet werden. Ordnen Sie keine Übersetzungsregeln ein Enterprise-VoIP-Routing testen, wenn Sie Übersetzungsregeln für den trunkpeer konfiguriert haben, da zwischen die zwei Regeln Konflikte auftreten könnten. 
  
## <a name="example-translation-rules"></a>Beispielübersetzungsregeln

Die folgenden Beispiele für Übersetzungsregeln zeigen, wie Sie Regeln auf dem Server erstellen können, um Nummern aus dem E.164-Format in ein lokales Format für den Trunkpeer zu übersetzen.
  
Ausführliche Informationen zur Implementierung von Übersetzungsregeln, finden Sie unter [Defining Translation Rules](http://technet.microsoft.com/library/4f6b975a-77e6-474c-9171-b139d84138c2.aspx) in der Bereitstellungsdokumentation.
  
|**Beschreibung**|**Anfangsziffern**|**Länge**|**Zu entfernende Ziffern**|**Hinzuzufügende Ziffern**|**Übereinstimmendes Muster**|**Übersetzung**|**Beispiel**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Normales Ferngespräch in den USA  <br/> (Pluszeichens das '+')  <br/> |+ 1  <br/> |Exakt 12  <br/> |1  <br/> |0  <br/> |^\+(1\d {10}) $  <br/> |$1  <br/> |+14255551010 wird zu 14255551010  <br/> |
|Internationales Ferngespräch aus den USA  <br/> (Pluszeichens "+" und Hinzufügen von 011)  <br/> |+  <br/> |Mindestens 11  <br/> |1  <br/> |011  <br/> |^\+(\d{9}\d+)$  <br/> |011$1  <br/> |+441235551010 wird zu 011441235551010  <br/> |
   
