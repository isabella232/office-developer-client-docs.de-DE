---
title: Geschlecht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791777"
---
# <a name="gender"></a><span data-ttu-id="46825-103">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="46825-103">Gender</span></span>

  
  
<span data-ttu-id="46825-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46825-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46825-105">Gibt die möglichen Werte für das Geschlecht der messaging-Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="46825-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="46825-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="46825-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="46825-107">Members</span><span class="sxs-lookup"><span data-stu-id="46825-107">Members</span></span>

 <span data-ttu-id="46825-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="46825-108">_genderMin_</span></span>
  
> <span data-ttu-id="46825-109">Die minimale Anzahl von unterschiedliche Werte für das Geschlecht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46825-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="46825-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="46825-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="46825-111">Das Geschlecht ist nicht für die messaging-Benutzer angegeben.</span><span class="sxs-lookup"><span data-stu-id="46825-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="46825-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="46825-112">_genderFemale_</span></span>
  
> <span data-ttu-id="46825-113">Der messaging-Benutzer ist Weiblich.</span><span class="sxs-lookup"><span data-stu-id="46825-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="46825-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="46825-114">_genderMale_</span></span>
  
> <span data-ttu-id="46825-115">Der messaging-Benutzer ist Männlich.</span><span class="sxs-lookup"><span data-stu-id="46825-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="46825-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="46825-116">_genderCount_</span></span>
  
> <span data-ttu-id="46825-117">Die Anzahl der unterschiedlichen Werte für das Geschlecht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46825-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="46825-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="46825-118">_genderMax_</span></span>
  
> <span data-ttu-id="46825-119">Die maximale Anzahl von unterschiedlichen Werten für das Geschlecht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46825-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46825-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46825-120">See also</span></span>



[<span data-ttu-id="46825-121">Kanonische PidTagGender-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="46825-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

