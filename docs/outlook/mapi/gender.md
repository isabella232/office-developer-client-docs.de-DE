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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342581"
---
# <a name="gender"></a><span data-ttu-id="ce466-103">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="ce466-103">Gender</span></span>

  
  
<span data-ttu-id="ce466-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce466-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce466-105">Gibt die möglichen Werte für das Geschlecht eines Messaging Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="ce466-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ce466-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ce466-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="ce466-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="ce466-107">Members</span></span>

 <span data-ttu-id="ce466-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="ce466-108">_genderMin_</span></span>
  
> <span data-ttu-id="ce466-109">Die Mindestanzahl von unterschiedlichen Werten, die für das Geschlecht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ce466-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="ce466-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="ce466-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="ce466-111">Das Geschlecht ist für den Messagingbenutzer nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce466-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="ce466-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="ce466-112">_genderFemale_</span></span>
  
> <span data-ttu-id="ce466-113">Der Messagingbenutzer ist weiblich.</span><span class="sxs-lookup"><span data-stu-id="ce466-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="ce466-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="ce466-114">_genderMale_</span></span>
  
> <span data-ttu-id="ce466-115">Der Messaging-Benutzer ist männlich.</span><span class="sxs-lookup"><span data-stu-id="ce466-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="ce466-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="ce466-116">_genderCount_</span></span>
  
> <span data-ttu-id="ce466-117">Die Anzahl der unterstützten Werte für das Geschlecht.</span><span class="sxs-lookup"><span data-stu-id="ce466-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="ce466-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="ce466-118">_genderMax_</span></span>
  
> <span data-ttu-id="ce466-119">Die maximale Anzahl unterschiedlicher Werte für das Geschlecht.</span><span class="sxs-lookup"><span data-stu-id="ce466-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce466-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce466-120">See also</span></span>



[<span data-ttu-id="ce466-121">Kanonische Pidtaggender (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce466-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

