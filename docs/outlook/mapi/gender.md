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
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588454"
---
# <a name="gender"></a><span data-ttu-id="d632f-103">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="d632f-103">Gender</span></span>

  
  
<span data-ttu-id="d632f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d632f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d632f-105">Gibt die möglichen Werte für das Geschlecht der messaging-Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="d632f-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d632f-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d632f-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d632f-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="d632f-107">Members</span></span>

 <span data-ttu-id="d632f-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="d632f-108">_genderMin_</span></span>
  
> <span data-ttu-id="d632f-109">Die minimale Anzahl von unterschiedliche Werte für das Geschlecht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d632f-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="d632f-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="d632f-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="d632f-111">Das Geschlecht ist nicht für die messaging-Benutzer angegeben.</span><span class="sxs-lookup"><span data-stu-id="d632f-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="d632f-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="d632f-112">_genderFemale_</span></span>
  
> <span data-ttu-id="d632f-113">Der messaging-Benutzer ist Weiblich.</span><span class="sxs-lookup"><span data-stu-id="d632f-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="d632f-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="d632f-114">_genderMale_</span></span>
  
> <span data-ttu-id="d632f-115">Der messaging-Benutzer ist Männlich.</span><span class="sxs-lookup"><span data-stu-id="d632f-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="d632f-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="d632f-116">_genderCount_</span></span>
  
> <span data-ttu-id="d632f-117">Die Anzahl der unterschiedlichen Werte für das Geschlecht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d632f-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="d632f-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="d632f-118">_genderMax_</span></span>
  
> <span data-ttu-id="d632f-119">Die maximale Anzahl von unterschiedlichen Werten für das Geschlecht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d632f-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d632f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d632f-120">See also</span></span>



[<span data-ttu-id="d632f-121">PidTagGender (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d632f-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

