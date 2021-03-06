---
title: Installieren des lokalen Konfigurationsspeichers – Aufruf (Konfiguration)
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
ms.date: 2/8/2018
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.dep.DeployReplicaConfig
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 92dccbca-7a5b-4064-9f2e-964b8e62433c
description: Wenn Sie mit der Installation der Datenbank beginnen möchten, die die lokale schreibgeschützte Kopie des zentralen Verwaltungsspeichers enthält, wählen Sie zwischen dem Abrufen der definierten Konfiguration, die mithilfe des Topologie-Generators aus dem bereits installierten und konfigurierten zentralen Verwaltungsspeicher oder Lesen der definierten Konfiguration von anderen Medien. Wählen Sie für einen Computer, der sich im internen Netzwerk Ihrer Organisation befindet, die Option Konfiguration automatisch aus dem zentralen Verwaltungsspeicher abrufen aus.
ms.openlocfilehash: 7638ab56e2ddcc8951ae989de11e72e0817a20bc
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41823639"
---
# <a name="install-local-configuration-store-invoke-configure"></a>Installieren des lokalen Konfigurationsspeichers – Aufruf (Konfiguration)
 
Wenn Sie mit der Installation der Datenbank beginnen möchten, die die lokale schreibgeschützte Kopie des zentralen Verwaltungsspeichers enthält, wählen Sie zwischen dem Abrufen der definierten Konfiguration, die mithilfe des Topologie-Generators aus dem bereits installierten und konfigurierten zentralen Verwaltungsspeicher oder Lesen der definierten Konfiguration von anderen Medien. Wählen Sie für einen Computer, der sich im internen Netzwerk Ihrer Organisation befindet, **die Option Konfiguration automatisch aus dem zentralen Verwaltungsspeicher abrufen aus**.
  
Wenn Sie ein Replikat des zentralen Verwaltungsspeichers auf einem Edgeserver installieren, wählen Sie aus, um die exportierte Kopie des Konfigurationsdokuments von tragbaren Medien wie einem USB-Flashlaufwerk, einem USB-Festplattenlaufwerk, einer CD-ROM oder einem anderen Medium zu lesen. 
  
> [!IMPORTANT]
> Wenn Sie den lokalen Konfigurationsspeicher auf einem Edgeserver installieren, müssen die Konfigurationsinformationen in einem Format vorliegen, das aus dem zentralen Verwaltungsspeicher exportiert wurde, indem Sie das Windows PowerShell-Cmdlet ausführen:`Export-CsConfiguration -FileName <ConfigurationFilePath.zip>`
  
Nachdem Sie die entsprechende Option ausgewählt haben, klicken Sie auf **weiter**.
  

