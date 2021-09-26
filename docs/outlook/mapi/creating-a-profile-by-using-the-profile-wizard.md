---
title: Erstellen eines Profils mithilfe des Profil-Assistenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eed28b64effa080a604e1ea97ddf5911796e07ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631034"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Erstellen eines Profils mithilfe des Profil-Assistenten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Profil-Assistent ist ein MAPI-Feature, mit dem ein Benutzer ein Profil auf die einfachste Weise erstellen kann. Der Profil-Assistent zeigt eine Reihe von Dialogfeldern an, in denen der Benutzer Nachrichtendienste auswählen und Werte für einige der wichtigsten Konfigurationseigenschaften eingeben kann. Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent die angegebenen Standardwerte. Um den Profil-Assistenten aufzurufen, rufen Sie **LaunchWizard** auf, eine Funktion, die auf dem [LAUNCHWIZARDENTRY-Prototyp](launchwizardentry.md) basiert. 
  
Der Benutzer kann dem neuen Profil, das den Profil-Assistenten unterstützt, nur diese Nachrichtendienste und Dienstanbieter hinzufügen. Da für jeden Nachrichtendienst möglicherweise mehr Eigenschaften festgelegt werden müssen, als der Profil-Assistent behandeln kann, beachten Sie, dass bei Verwendung dieses Ansatzes eine oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden können.
  

