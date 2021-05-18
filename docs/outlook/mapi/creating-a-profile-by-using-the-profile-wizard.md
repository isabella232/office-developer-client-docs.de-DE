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
  
Der Profil-Assistent ist ein MAPI-Feature, mit dem ein Benutzer ein Profil auf einfachste Weise erstellen kann. Der Profil-Assistent zeigt eine Reihe von Dialogfelder an, in denen der Benutzer aufgefordert wird, Nachrichtendienste auszuwählen und Werte für einige der wichtigsten Konfigurationseigenschaften ein eingeben. Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent die bereitgestellten Standardwerte. Rufen Sie zum Aufrufen des Profil-Assistenten **LaunchWizard** auf, eine Funktion, die auf dem [LAUNCHWIZARDENTRY-Prototyp](launchwizardentry.md) basiert. 
  
Der Benutzer kann dem neuen Profil, das den Profil-Assistenten unterstützt, nur diese Nachrichtendienste und Dienstanbieter hinzufügen. Da für jeden Nachrichtendienst möglicherweise mehr Eigenschaften festgelegt werden müssen, als der Profil-Assistent verarbeiten kann, sollten Sie beachten, dass bei verwendung dieses Ansatzes eine oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden können.
  

