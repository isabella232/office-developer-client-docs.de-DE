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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358114"
---
# <a name="spropattrarray"></a><span data-ttu-id="0af25-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="0af25-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="0af25-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0af25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0af25-105">Enthält eine Liste der Attribute für die Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="0af25-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0af25-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0af25-106">Header file:</span></span>  <br/> |<span data-ttu-id="0af25-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="0af25-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="0af25-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="0af25-108">Related macros:</span></span>  <br/> |<span data-ttu-id="0af25-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="0af25-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="0af25-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="0af25-110">Members</span></span>

 <span data-ttu-id="0af25-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0af25-111">**cValues**</span></span>
  
> <span data-ttu-id="0af25-112">Die Anzahl der Eigenschaftsattribute im **aPropAttr** -Element.</span><span class="sxs-lookup"><span data-stu-id="0af25-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="0af25-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="0af25-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="0af25-114">Ein Array von Eigenschaftsattributen.</span><span class="sxs-lookup"><span data-stu-id="0af25-114">An array of property attributes.</span></span> <span data-ttu-id="0af25-115">Gültige Werte für Attribute lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0af25-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="0af25-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="0af25-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="0af25-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="0af25-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="0af25-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="0af25-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="0af25-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="0af25-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0af25-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0af25-120">Remarks</span></span>

<span data-ttu-id="0af25-121">Die **SPropAttrArray** -Struktur wird von Eigenschaftendaten Objekten verwendet, die die [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="0af25-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="0af25-122">Sie wird auch von der MAPI-Implementierung von [IMAPIMessageSite verwendet: IUnknown](imapimessagesiteiunknown.md) , die auf strukturiertem Speicher basiert.</span><span class="sxs-lookup"><span data-stu-id="0af25-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0af25-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0af25-123">See also</span></span>



[<span data-ttu-id="0af25-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0af25-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="0af25-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0af25-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="0af25-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="0af25-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="0af25-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="0af25-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="0af25-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0af25-128">MAPI Structures</span></span>](mapi-structures.md)

