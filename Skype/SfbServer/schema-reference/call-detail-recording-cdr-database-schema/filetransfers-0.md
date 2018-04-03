---
title: FileTransfers-Tabelle in Skype für Business Server 2015
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 7/15/2015
ms.audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
description: Jeder Datensatz steht für eine dateiübertragungssitzung.
ms.openlocfilehash: 07ab898246efbac623910886000e97037f43ead2
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="filetransfers-table-in-skype-for-business-server-2015"></a>FileTransfers-Tabelle in Skype für Business Server 2015
 
Jeder Datensatz steht für eine dateiübertragungssitzung.
  
|**Spalte**|**Datentyp**|**Schlüssel/Index**|**Details**|
|:-----|:-----|:-----|:-----|
|**SessionIdTime** <br/> |datetime  <br/> |Primär, Fremd  <br/> |Zeitpunkt der sitzungsanforderung. Zusammen mit **SessionIdSeq** verwendet zur eindeutigen Identifizierung eine Sitzung. Finden Sie unter der [Dialogs-Tabelle in Skype für Business Server 2015](dialogs.md) Weitere Informationen. <br/> |
|**SessionIdSeq** <br/> |int  <br/> |Primär, Fremd  <br/> |ID-Nummer, um die Sitzung zu identifizieren. In Verbindung mit **SessionIdTime** verwendet, um eine Sitzung eindeutig zu identifizieren. Finden Sie unter der [Dialogs-Tabelle in Skype für Business Server 2015](dialogs.md) Weitere Informationen. <br/> |
|**Dateiname** <br/> |nvarchar(256)  <br/> ||Der Name der Datei.  <br/> |
|**FileIdentity** <br/> |uniqueidentifier  <br/> ||Eindeutiger Bezeichner zum unterscheiden zwischen dateiübertragungen mit demselben Namen.  <br/> |
|**Cookie** <br/> |nvarchar(128)  <br/> |Primary  <br/> |Verwendet, um jede Nachricht zur nachverfolgung als wird hiermit zugeordnet zu identifizieren.  <br/> |
|**Akzeptieren** <br/> |bit  <br/> ||TRUE oder NULL kann sein. Wenn TRUE, dann ablehnen, und Abbrechen werden NULL sein.  <br/> |
|**Ablehnen** <br/> |bit  <br/> ||TRUE oder NULL kann sein. Bei TRUE wird annehmen und Abbrechen NULL sein.  <br/> |
|**Abbrechen** <br/> |bit  <br/> ||TRUE oder NULL kann sein. Bei TRUE wird annehmen und Ablehnen NULL sein.  <br/> |
|**ZuletztGeändertUm** <br/> |DateTime  <br/> ||Für die interne Verwendung durch den Überwachungsdienst.  <br/> Dieses Feld wurde in Skype für Business Server 2015 eingeführt.  <br/> |
   
