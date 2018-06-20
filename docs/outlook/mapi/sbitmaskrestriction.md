---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795427"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="60ab7-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="60ab7-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="60ab7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="60ab7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="60ab7-105">Beschreibt eine Einschränkung Bitmaske, die eine bitweise **AND** -Operation ausführen und testen das Ergebnis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60ab7-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60ab7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="60ab7-106">Header file:</span></span>  <br/> |<span data-ttu-id="60ab7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60ab7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="60ab7-108">Members</span><span class="sxs-lookup"><span data-stu-id="60ab7-108">Members</span></span>

 <span data-ttu-id="60ab7-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="60ab7-109">**relBMR**</span></span>
  
> <span data-ttu-id="60ab7-110">Relationale Operator, der beschreibt, wie die Maske angegeben im **UlMask** -Member auf das Eigenschafts-Tag angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60ab7-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="60ab7-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="60ab7-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="60ab7-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="60ab7-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="60ab7-113">Führen Sie eine bitweise **AND** -Operation der Maske im **UlMask** -Member, mit der-Eigenschaft, die durch die **UlPropTag** Member und Test für gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="60ab7-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="60ab7-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="60ab7-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="60ab7-115">Führen Sie eine bitweise **AND** -Operation der Maske im **UlMask** -Member, mit der-Eigenschaft, die durch die **UlPropTag** Member und Test für wird nicht gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="60ab7-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="60ab7-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="60ab7-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="60ab7-117">Eigenschaftentag der-Eigenschaft auf der die Bitmaske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="60ab7-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="60ab7-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="60ab7-118">**ulMask**</span></span>
  
> <span data-ttu-id="60ab7-119">Bitmaske für die Eigenschaft identifizierten **UlPropTag**gelten.</span><span class="sxs-lookup"><span data-stu-id="60ab7-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60ab7-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60ab7-120">Remarks</span></span>

<span data-ttu-id="60ab7-121">Die Struktur **SBitMaskRestriction** führt eine bitweise **AND** -Operation verwenden die Bitmaske beschrieben in das **UlMask** -Element, und der Wert der Eigenschaft vom **UlPropTag** Member beschrieben.</span><span class="sxs-lookup"><span data-stu-id="60ab7-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="60ab7-122">Wenn das Ergebnis gleich NULL ist, wird die BMR_EQZ erfüllt.</span><span class="sxs-lookup"><span data-stu-id="60ab7-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="60ab7-123">Wenn es ungleich NULL ist, d. h., ist mindestens eines der gleichen Bits als **UlMask**, verfügt der Eigenschaftswert dann BMR_NEZ erfüllt.</span><span class="sxs-lookup"><span data-stu-id="60ab7-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="60ab7-124">Weitere Informationen zu den **SBitMaskRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="60ab7-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60ab7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60ab7-125">See also</span></span>



[<span data-ttu-id="60ab7-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="60ab7-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="60ab7-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="60ab7-127">MAPI Structures</span></span>](mapi-structures.md)
