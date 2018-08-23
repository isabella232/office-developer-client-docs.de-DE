---
title: Erstellen eines Profils mit dem Profilassistenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f30dca8323f74bc2817bab375b58fcc1bc15c18b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574258"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="f762d-103">Erstellen eines Profils mit dem Profilassistenten</span><span class="sxs-lookup"><span data-stu-id="f762d-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="f762d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f762d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f762d-105">Der Profil-Assistent ist ein MAPI-Feature, mit dem einen Benutzer zum Erstellen eines Profils in die einfachste Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="f762d-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="f762d-106">Der Profil-Assistent zeigt eine Reihe von Dialogfeldern in dem der Benutzer aufgefordert, wählen Sie Nachrichtendienste, und geben Sie Werte für einige der wichtigsten Konfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f762d-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="f762d-107">Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent Standardwerte bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f762d-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="f762d-108">Rufen Sie zum Aufrufen der Profil-Assistent **LaunchWizard**, eine Funktion, die basierend auf den [LAUNCHWIZARDENTRY](launchwizardentry.md) Prototyp.</span><span class="sxs-lookup"><span data-stu-id="f762d-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="f762d-109">Der Benutzer kann nur die Message-Dienste und -Dienstanbieter hinzufügen, um das neue Profil, die die Profile-Assistent unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f762d-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="f762d-110">Da jede Messagingdiensts möglicherweise mehr Eigenschaften benötigt festgelegt werden soll, als der Profil-Assistent verarbeitet werden können, achten Sie darauf, dass, wenn Sie dieses Verfahren verwenden, für eine oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f762d-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

