---
title: Hinzufügen eines SQL Server-Speichers Archivierungsserver
ms.author: kenwith
author: kenwith
manager: serdars
ms.date: 2/8/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.lync.tb.AddArchivingServerSqlStorePage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 26e0a748-e31d-4c66-b225-b37e0a45408f
description: Der Archivierungsserver erfordert eine unterstützte 64-Bit-Edition von der SQL Server-Datenbanksoftware zum Speichern der Daten archivieren. Sie können entweder auswählen eine zuvor definierte SQL Server-Datenbank für die Archivierung verwendet werden soll, oder definieren eine neue SQL Server-Datenbank durch einen vollqualifizierten Domänennamen (FQDN) des Servers, auf dem SQL Server-Datenbank befinden, und die Instanz von SQL Server angeben, Sie möchten für die neue SQL Server-Datenbank verwendet (werden kann die Standardinstanz oder eine benannte Instanz, die Sie angeben).
ms.openlocfilehash: 2c63b6bf71c156bc62e07add023f3049af399095
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="add-archiving-server-sql-server-store"></a>Hinzufügen eines SQL Server-Speichers Archivierungsserver
 
Der Archivierungsserver erfordert eine unterstützte 64-Bit-Edition von der SQL Server-Datenbanksoftware zum Speichern der Daten archivieren. Sie können entweder auswählen eine zuvor definierte SQL Server-Datenbank für die Archivierung verwendet werden soll, oder definieren eine neue SQL Server-Datenbank durch einen vollqualifizierten Domänennamen (FQDN) des Servers, auf dem SQL Server-Datenbank befinden, und die Instanz von SQL Server angeben, Sie möchten für die neue SQL Server-Datenbank verwendet (werden kann die Standardinstanz oder eine benannte Instanz, die Sie angeben).
  
> [!NOTE]
> Wenn das Konto, mit dem Veröffentlichen der Topologie, der ausreichenden Benutzerrechte und-Berechtigungen verfügt, können Sie die Archivierungsdatenbank (LcsLog) erstellen, wenn Sie Ihre Topologie veröffentlichen. Sie können auch die Datenbank des Installationsvorgangs später erstellen oder auf andere Weise. 
  
> [!NOTE]
> Zum Installieren und die Datenbanken auf dem SQL Server-basierten Server für die Archivierung bereitzustellen, müssen Sie Mitglied der Gruppe der SQL Server-Sysadmins für den SQL Server-basierten Server sein, auf dem Sie die Datenbankdateien installieren. Wenn Sie ein Mitglied der SQL Server-Gruppe Sysadmins nicht sind, müssen Sie anfordern, der Gruppe hinzugefügt werden soll, bis die Datenbankdateien bereitgestellt werden. Wenn Sie ein Mitglied der Gruppe Sysadmins hergestellt werden können, sollten Sie sich an den Datenbankadministrator SQL Server bereitstellen, mit dem Skript konfigurieren und Bereitstellen der Datenbanken. Ausführliche Informationen über die Benutzerrechte und Berechtigungen, mit denen Sie die Verfahren durchführen müssen, finden Sie unter [Berechtigungen für SQL Server](http://technet.microsoft.com/library/56ea0c02-bcf5-4d45-aa13-570531c29074.aspx) in der Bereitstellungsdokumentation.
  
