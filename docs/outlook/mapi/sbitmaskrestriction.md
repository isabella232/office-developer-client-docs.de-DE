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
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357526"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="f3096-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="f3096-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="f3096-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3096-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3096-105">Beschreibt eine Bitmasken Einschränkung, die zum Durchführen einer bitweisen **and-** Operation und zum Testen des Ergebnisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3096-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3096-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f3096-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3096-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f3096-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="f3096-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="f3096-108">Members</span></span>

 <span data-ttu-id="f3096-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="f3096-109">**relBMR**</span></span>
  
> <span data-ttu-id="f3096-110">Relationaler Operator, der beschreibt, wie die im **ulMask** -Element angegebene Maske auf das Property-Tag angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3096-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="f3096-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="f3096-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="f3096-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="f3096-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="f3096-113">Führen Sie eine bitweise **and** -Operation der Maske im **ulMask** -Element mit der vom **ulPropTag** -Element dargestellten Eigenschaft aus, und testen Sie, dass Sie gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f3096-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="f3096-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="f3096-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="f3096-115">Führen Sie eine bitweise **and** -Operation der Maske im **ulMask** -Element mit der vom **ulPropTag** -Element dargestellten Eigenschaft aus, und testen Sie, ob Sie ungleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f3096-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="f3096-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="f3096-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="f3096-117">Property-Tag der Eigenschaft, auf die die Bitmaske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3096-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="f3096-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="f3096-118">**ulMask**</span></span>
  
> <span data-ttu-id="f3096-119">Bitmaske, die auf die durch **ulPropTag**angegebene Eigenschaft angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3096-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3096-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3096-120">Remarks</span></span>

<span data-ttu-id="f3096-121">Die **SBitMaskRestriction** -Struktur führt eine bitweise **and** -Operation mit der im **ulMask** -Element beschriebenen Bitmaske und dem Wert der vom **ulPropTag** -Element beschriebenen Eigenschaft aus.</span><span class="sxs-lookup"><span data-stu-id="f3096-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="f3096-122">Wenn das Ergebnis NULL ist, ist BMR_EQZ zufrieden.</span><span class="sxs-lookup"><span data-stu-id="f3096-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="f3096-123">Wenn es ungleich NULL ist, das heißt, wenn der Eigenschaftswert mindestens eines der Bits hat, die als **ulMask**festgelegt sind, dann BMR_NEZ.</span><span class="sxs-lookup"><span data-stu-id="f3096-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="f3096-124">Weitere Informationen zur **SBitMaskRestriction** -Struktur und zu Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f3096-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3096-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3096-125">See also</span></span>



[<span data-ttu-id="f3096-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f3096-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="f3096-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f3096-127">MAPI Structures</span></span>](mapi-structures.md)

