---
title: Geschlecht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428648"
---
# <a name="gender"></a><span data-ttu-id="1753f-103">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="1753f-103">Gender</span></span>

  
  
<span data-ttu-id="1753f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1753f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1753f-105">Gibt die möglichen Werte für das Geschlecht eines Messagingbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="1753f-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1753f-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1753f-106">Quick info</span></span>

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a><span data-ttu-id="1753f-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="1753f-107">Members</span></span>

 <span data-ttu-id="1753f-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="1753f-108">_genderMin_</span></span>
  
> <span data-ttu-id="1753f-109">Die Mindestanzahl unterschiedlicher Werte, die für das Geschlecht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1753f-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="1753f-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="1753f-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="1753f-111">Das Geschlecht wird für den Messagingbenutzer nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="1753f-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="1753f-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="1753f-112">_genderFemale_</span></span>
  
> <span data-ttu-id="1753f-113">Der Messagingbenutzer ist weiblich.</span><span class="sxs-lookup"><span data-stu-id="1753f-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="1753f-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="1753f-114">_genderMale_</span></span>
  
> <span data-ttu-id="1753f-115">Der Messagingbenutzer ist männlich.</span><span class="sxs-lookup"><span data-stu-id="1753f-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="1753f-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="1753f-116">_genderCount_</span></span>
  
> <span data-ttu-id="1753f-117">Die Anzahl der verschiedenen Werte, die für das Geschlecht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1753f-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="1753f-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="1753f-118">_genderMax_</span></span>
  
> <span data-ttu-id="1753f-119">Die maximale Anzahl unterschiedlicher Werte, die für das Geschlecht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1753f-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1753f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1753f-120">See also</span></span>



[<span data-ttu-id="1753f-121">PidTagGender (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1753f-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

