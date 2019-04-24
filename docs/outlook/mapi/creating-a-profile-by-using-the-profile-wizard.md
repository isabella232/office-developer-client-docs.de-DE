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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332935"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="94acd-103">Erstellen eines Profils mithilfe des Profil-Assistenten</span><span class="sxs-lookup"><span data-stu-id="94acd-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="94acd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94acd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94acd-105">Der Profil-Assistent ist ein MAPI-Feature, mit dem ein Benutzer ein Profil auf die einfachste Weise erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="94acd-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="94acd-106">Der Profil-Assistent zeigt eine Reihe von Dialogfeldern an, mit denen der Benutzer Nachrichtendienste auswählen und Werte für einige der wichtigsten Konfigurationseigenschaften eingeben muss.</span><span class="sxs-lookup"><span data-stu-id="94acd-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="94acd-107">Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="94acd-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="94acd-108">Rufen Sie zum Aufrufen des Profil-Assistenten **LaunchWizard**auf, eine auf dem [LAUNCHWIZARDENTRY](launchwizardentry.md) -Prototyp basierende Funktion.</span><span class="sxs-lookup"><span data-stu-id="94acd-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="94acd-109">Der Benutzer kann nur die Nachrichtendienste und Dienstanbieter zu dem neuen Profil hinzufügen, das den Profil-Assistenten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94acd-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="94acd-110">Da für jeden Nachrichtendienst möglicherweise weitere Eigenschaften festgelegt werden müssen, als der Profil-Assistent verarbeiten kann, sollten Sie beachten, dass bei Verwendung dieses Ansatzes ein oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="94acd-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

