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
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424476"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="230fa-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="230fa-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="230fa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="230fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="230fa-105">Beschreibt eine Bitmaskeneinschränkung, die verwendet wird, um einen bitweisen **AND-Vorgang** durchzuführen und das Ergebnis zu testen.</span><span class="sxs-lookup"><span data-stu-id="230fa-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="230fa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="230fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="230fa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="230fa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="230fa-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="230fa-108">Members</span></span>

 <span data-ttu-id="230fa-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="230fa-109">**relBMR**</span></span>
  
> <span data-ttu-id="230fa-110">Relationaler Operator, der beschreibt, wie die im **ulMask-Element** angegebene Maske auf das Eigenschaftstag angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="230fa-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="230fa-111">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="230fa-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="230fa-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="230fa-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="230fa-113">Führen Sie einen bitweisen **AND-Vorgang** der Maske im **ulMask-Element** aus, mit der Eigenschaft, die durch das **ulPropTag-Element** dargestellt wird, und testen Sie, ob sie gleich Null ist.</span><span class="sxs-lookup"><span data-stu-id="230fa-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="230fa-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="230fa-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="230fa-115">Führen Sie einen bitweisen **#A0** der Maske im **ulMask-Element** aus, mit der Eigenschaft, die durch das **ulPropTag-Element** dargestellt wird, und testen Sie, ob sie nicht gleich Null ist.</span><span class="sxs-lookup"><span data-stu-id="230fa-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="230fa-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="230fa-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="230fa-117">Eigenschaftstag der Eigenschaft, auf die die Bitmaske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="230fa-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="230fa-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="230fa-118">**ulMask**</span></span>
  
> <span data-ttu-id="230fa-119">Bitmaske, die auf die durch **ulPropTag** identifizierte Eigenschaft angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="230fa-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="230fa-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="230fa-120">Remarks</span></span>

<span data-ttu-id="230fa-121">Die **SBitMaskRestriction-Struktur** führt einen bitweisen **#A0** mithilfe der im **ulMask-Element** beschriebenen Bitmaske und des Werts der Eigenschaft durch, die vom **ulPropTag-Element beschrieben** wird.</span><span class="sxs-lookup"><span data-stu-id="230fa-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="230fa-122">Wenn das Ergebnis null ist, BMR_EQZ erfüllt.</span><span class="sxs-lookup"><span data-stu-id="230fa-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="230fa-123">Wenn der Wert ungleich null ist, d. h. wenn der Eigenschaftswert mindestens einen der gleichen Bits wie **ulMask** festgelegt hat, ist BMR_NEZ erfüllt.</span><span class="sxs-lookup"><span data-stu-id="230fa-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="230fa-124">Weitere Informationen zur Struktur und Einschränkungen **von SBitMaskRestriction** im Allgemeinen finden Sie unter [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="230fa-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="230fa-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="230fa-125">See also</span></span>



[<span data-ttu-id="230fa-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="230fa-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="230fa-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="230fa-127">MAPI Structures</span></span>](mapi-structures.md)

