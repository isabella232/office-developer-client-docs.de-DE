---
title: Erstellen ein Profil mithilfe der Profil-Assistent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791480"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="b09f6-103">Erstellen ein Profil mithilfe der Profil-Assistent</span><span class="sxs-lookup"><span data-stu-id="b09f6-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="b09f6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b09f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b09f6-105">Der Profil-Assistent ist ein MAPI-Feature, mit dem einen Benutzer zum Erstellen eines Profils in die einfachste Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="b09f6-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="b09f6-106">Der Profil-Assistent zeigt eine Reihe von Dialogfeldern in dem der Benutzer aufgefordert, wählen Sie Nachrichtendienste, und geben Sie Werte für einige der wichtigsten Konfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b09f6-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="b09f6-107">Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent Standardwerte bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b09f6-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="b09f6-108">Rufen Sie zum Aufrufen der Profil-Assistent **LaunchWizard**, eine Funktion, die basierend auf den [LAUNCHWIZARDENTRY](launchwizardentry.md) Prototyp.</span><span class="sxs-lookup"><span data-stu-id="b09f6-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="b09f6-109">Der Benutzer kann nur die Message-Dienste und -Dienstanbieter hinzufügen, um das neue Profil, die die Profile-Assistent unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b09f6-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="b09f6-110">Da jede Messagingdiensts möglicherweise mehr Eigenschaften benötigt festgelegt werden soll, als der Profil-Assistent verarbeitet werden können, achten Sie darauf, dass, wenn Sie dieses Verfahren verwenden, für eine oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b09f6-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

