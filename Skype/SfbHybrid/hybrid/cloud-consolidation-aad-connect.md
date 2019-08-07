---
title: Aktualisieren von Aad Connect, um mehr als eine Gesamtstruktur einzubeziehen
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.reviewer: bjwhalen
ms.topic: article
ms.prod: skype-for-business-itpro
search.appverid: MET150
ms.collection:
- Hybrid
- M365-voice
- M365-collaboration
- Teams_ITAdmin_Help
- Adm_Skype4B_Online
audience: ITPro
appliesto:
- Skype for Business
- Microsoft Teams
localization_priority: Normal
description: Dieser Anhang enthält detaillierte Schritte zum Aktualisieren von Aad Connect, um mehr als eine Gesamtstruktur als Teil der Cloud-Konsolidierung für Teams und Skype for Business einzubeziehen.
ms.openlocfilehash: cbb4811d999601524557e7106840a66682565e5f
ms.sourcegitcommit: ab47ff88f51a96aaf8bc99a6303e114d41ca5c2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2019
ms.locfileid: "36160581"
---
# <a name="update-aad-connect-to-include-more-than-one-forest"></a>Aktualisieren von Aad Connect, um mehr als eine Gesamtstruktur einzubeziehen

Azure AD Connect unterstützt die [Synchronisierung von mehreren Gesamtstrukturen](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-topologies). Es unterstützt jedoch nur eine Instanz von Azure AD Connect-Synchronisierung mit Aad. In Fällen, in denen Azure AD bereits in einer Gesamtstruktur installiert ist, muss die vorhandene Instanz von Aad Connect daher zur Synchronisierung von der zusätzlichen Gesamtstruktur aktualisiert werden.

 - Wenn alle Identitäten nur einmal in beiden Gesamtstrukturen dargestellt werden (das heißt, Sie haben keine e-Mail-aktivierten Kontakte hergestellt), können Sie einfach den Aad-Verbindungs-Assistenten erneut ausführen, die Option "Synchronisierungsoptionen anpassen" auswählen und dann auf der Seite " **Ihre Verzeichnisse verbinden" **den Namen der zusätzlichen Gesamtstruktur und creds ein.<br><br>
 ![Die Seite "Ihre Verzeichnisse verbinden"](../media/cloud-consolidation-connect-your-directories.png)
 - Wenn Benutzer jedoch in mehr als einem Verzeichnis vorhanden sein können und Sie die Daten zusammenführen (beispielsweise wenn Kontaktobjekte in einer Gesamtstruktur vorhanden sind, die Benutzern in einer anderen Gesamtstruktur entspricht), müssen Sie Azure AD Connect deinstallieren und erneut installieren.  Dies liegt daran, dass die Bedingung "gesamtstrukturübergreifende Join Rules" nur während der ersten Installation konfiguriert werden kann. Dies geschieht auf der folgenden Seite:<br><br>
 ![Die Seite zum eindeutigen Identifizieren Ihrer Benutzer](../media/cloud-consolidation-uniquely-identifying-your-users.png)


## <a name="see-also"></a>Siehe auch

[Cloud-Konsolidierung für Teams und Skype for Business](cloud-consolidation.md)