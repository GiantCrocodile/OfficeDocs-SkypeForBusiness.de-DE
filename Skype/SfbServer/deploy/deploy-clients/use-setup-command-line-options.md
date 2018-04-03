---
title: Verwenden der Setup-Befehlszeilenoptionen in Skype for Business Server 2015
ms.author: chucked
author: chuckedmonson
manager: serdars
ms.date: 10/20/2017
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 99878c3c-ff31-48e2-8424-580d7b07a7bf
description: 'Zusammenfassung: Erfahren Sie mehr über Setup.exe Befehlszeile Vorgänge während des Setups von Office.'
ms.openlocfilehash: 0fa4f31750697f0bd0dbe87bbde025cbc7f530bd
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="use-setup-command-line-options-in-skype-for-business-server-2015"></a>Verwenden der Setup-Befehlszeilenoptionen in Skype for Business Server 2015
 
**Zusammenfassung:** Informationen Sie zu Setup.exe Befehlszeile Vorgänge während des Setups von Office.
  
Die Befehlszeile von "Setup.exe" wird nur für wenige Vorgänge des Office-Setups verwendet. Verwenden Sie die Setup-Befehlszeilenoptionen, sondern in der Regel verwenden Office-Anpassungstool und der Datei Config.xml für Produkt-Setup und Anpassung Sie.
  
Die Befehlszeile der Office "Setup.exe" erkennt die in der folgenden Tabelle beschriebenen Befehlzeilenoptionen.
  
**Office-Setup-Befehlszeilenoptionen**

|**Setup-Befehlszeilenoption**|**Beschreibung**|
|:-----|:-----|
|/admin  <br/> |Führt das Office-Anpassungstool aus, um eine Setupanpassungsdatei (.msp-Datei) zu erstellen.  <br/> |
|/adminfile [Pfad]  <br/> |Wendet die angegebene Setupanpassungsdatei auf die Installation an. Sie können einen Pfad zu einer bestimmten Anpassungsdatei (.msp-Datei) oder zu dem Ordner angeben, in dem Sie Anpassungsdateien speichern.  <br/> |
|/config [Pfad]  <br/> |Gibt die Datei Config.xml, die Setup während der Installation verwendet. Verwenden Sie die Option/config auf die Datei Config.xml angeben, die Sie für Skype für Business-Installationen, beispielsweise angepasst:`/config \\server\share\Skype15\Skype.WW\Config.xml` <br/> |
|/modify Skype  <br/> |Wird mit einer geänderten config.xml-Datei verwendet, um Setup im Wartungsmodus auszuführen und Änderungen an einer vorhandenen Office-Installation durchzuführen. Angenommen, Sie können die / modify Option zum Hinzufügen oder Entfernen von Skype für Business-Features.  <br/> |
|/repair Skype  <br/> |Führt Setup aus dem Computer des Benutzers, Skype für Unternehmen zu reparieren.  <br/> |
|/uninstall Skype  <br/> |Führt Setup aus, um Skype für Unternehmen aus dem Computer des Benutzers zu entfernen.  <br/> |
   
Ausführliche Informationen zum Verwenden der Setup-Befehlszeilenoptionen finden Sie unter [https://go.microsoft.com/fwlink/p/?linkid=267515](https://go.microsoft.com/fwlink/p/?linkid=267515). 
  
