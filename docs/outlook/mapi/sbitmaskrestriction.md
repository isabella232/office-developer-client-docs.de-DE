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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9197201388530bd7755eb1987ecc863220e3847
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566607"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="5f672-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="5f672-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="5f672-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f672-105">Beschreibt eine Einschränkung Bitmaske, die eine bitweise **AND** -Operation ausführen und testen das Ergebnis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f672-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f672-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5f672-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f672-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f672-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="5f672-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="5f672-108">Members</span></span>

 <span data-ttu-id="5f672-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="5f672-109">**relBMR**</span></span>
  
> <span data-ttu-id="5f672-110">Relationale Operator, der beschreibt, wie die Maske angegeben im **UlMask** -Member auf das Eigenschafts-Tag angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f672-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="5f672-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5f672-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="5f672-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="5f672-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="5f672-113">Führen Sie eine bitweise **AND** -Operation der Maske im **UlMask** -Member, mit der-Eigenschaft, die durch die **UlPropTag** Member und Test für gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5f672-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="5f672-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="5f672-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="5f672-115">Führen Sie eine bitweise **AND** -Operation der Maske im **UlMask** -Member, mit der-Eigenschaft, die durch die **UlPropTag** Member und Test für wird nicht gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5f672-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="5f672-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="5f672-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="5f672-117">Eigenschaftentag der-Eigenschaft auf der die Bitmaske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f672-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="5f672-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="5f672-118">**ulMask**</span></span>
  
> <span data-ttu-id="5f672-119">Bitmaske für die Eigenschaft identifizierten **UlPropTag**gelten.</span><span class="sxs-lookup"><span data-stu-id="5f672-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f672-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="5f672-120">Remarks</span></span>

<span data-ttu-id="5f672-121">Die Struktur **SBitMaskRestriction** führt eine bitweise **AND** -Operation verwenden die Bitmaske beschrieben in das **UlMask** -Element, und der Wert der Eigenschaft vom **UlPropTag** Member beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f672-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="5f672-122">Wenn das Ergebnis gleich NULL ist, wird die BMR_EQZ erfüllt.</span><span class="sxs-lookup"><span data-stu-id="5f672-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="5f672-123">Wenn es ungleich NULL ist, d. h., ist mindestens eines der gleichen Bits als **UlMask**, verfügt der Eigenschaftswert dann BMR_NEZ erfüllt.</span><span class="sxs-lookup"><span data-stu-id="5f672-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="5f672-124">Weitere Informationen zu den **SBitMaskRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5f672-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f672-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f672-125">See also</span></span>



[<span data-ttu-id="5f672-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5f672-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="5f672-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5f672-127">MAPI Structures</span></span>](mapi-structures.md)

