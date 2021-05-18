---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405513"
---
# <a name="spropattrarray"></a><span data-ttu-id="987fd-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="987fd-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="987fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="987fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="987fd-105">Enthält eine Liste von Attributen für Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="987fd-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="987fd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="987fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="987fd-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="987fd-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="987fd-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="987fd-108">Related macros:</span></span>  <br/> |<span data-ttu-id="987fd-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="987fd-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="987fd-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="987fd-110">Members</span></span>

 <span data-ttu-id="987fd-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="987fd-111">**cValues**</span></span>
  
> <span data-ttu-id="987fd-112">Anzahl der Eigenschaftenattribute im **aPropAttr-Element.**</span><span class="sxs-lookup"><span data-stu-id="987fd-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="987fd-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="987fd-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="987fd-114">Ein Array von Eigenschaftenattributen.</span><span class="sxs-lookup"><span data-stu-id="987fd-114">An array of property attributes.</span></span> <span data-ttu-id="987fd-115">Gültige Werte für Attribute sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="987fd-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="987fd-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="987fd-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="987fd-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="987fd-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="987fd-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="987fd-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="987fd-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="987fd-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="987fd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="987fd-120">Remarks</span></span>

<span data-ttu-id="987fd-121">Die **SPropAttrArray-Struktur** wird von Eigenschaftsdatenobjekten verwendet, die die [IPropData : IMAPIProp-Schnittstelle](ipropdataimapiprop.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="987fd-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="987fd-122">Sie wird auch von der MAPI-Implementierung von [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) verwendet, die auf strukturiertem Speicher basiert.</span><span class="sxs-lookup"><span data-stu-id="987fd-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="987fd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="987fd-123">See also</span></span>



[<span data-ttu-id="987fd-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="987fd-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="987fd-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="987fd-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="987fd-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="987fd-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="987fd-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="987fd-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="987fd-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="987fd-128">MAPI Structures</span></span>](mapi-structures.md)

