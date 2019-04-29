---
title: Erstellen eines Profils mithilfe des Profil-Assistenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411736"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Erstellen eines Profils mithilfe des Profil-Assistenten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Profil-Assistent ist ein MAPI-Feature, mit dem ein Benutzer ein Profil auf die einfachste Weise erstellen kann. Der Profil-Assistent zeigt eine Reihe von Dialogfeldern an, mit denen der Benutzer Nachrichtendienste auswählen und Werte für einige der wichtigsten Konfigurationseigenschaften eingeben muss. Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent die Standardwerte. Rufen Sie zum Aufrufen des Profil-Assistenten **LaunchWizard**auf, eine auf dem [LAUNCHWIZARDENTRY](launchwizardentry.md) -Prototyp basierende Funktion. 
  
Der Benutzer kann nur die Nachrichtendienste und Dienstanbieter zu dem neuen Profil hinzufügen, das den Profil-Assistenten unterstützt. Da für jeden Nachrichtendienst möglicherweise weitere Eigenschaften festgelegt werden müssen, als der Profil-Assistent verarbeiten kann, sollten Sie beachten, dass bei Verwendung dieses Ansatzes ein oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden können.
  

