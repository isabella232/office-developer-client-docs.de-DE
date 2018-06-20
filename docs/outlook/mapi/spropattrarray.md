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
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795608"
---
# <a name="spropattrarray"></a><span data-ttu-id="dcea8-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="dcea8-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="dcea8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcea8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcea8-105">Enthält eine Liste der Attribute für die Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="dcea8-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcea8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dcea8-106">Header file:</span></span>  <br/> |<span data-ttu-id="dcea8-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="dcea8-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="dcea8-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="dcea8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="dcea8-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="dcea8-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="dcea8-110">Members</span><span class="sxs-lookup"><span data-stu-id="dcea8-110">Members</span></span>

 <span data-ttu-id="dcea8-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="dcea8-111">**cValues**</span></span>
  
> <span data-ttu-id="dcea8-112">Anzahl der Attribute im **aPropAttr** -Member.</span><span class="sxs-lookup"><span data-stu-id="dcea8-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="dcea8-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="dcea8-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="dcea8-114">Ein Array von Eigenschaftsattribute.</span><span class="sxs-lookup"><span data-stu-id="dcea8-114">An array of property attributes.</span></span> <span data-ttu-id="dcea8-115">Gültige Werte für Attribute sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dcea8-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="dcea8-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="dcea8-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="dcea8-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="dcea8-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="dcea8-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="dcea8-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="dcea8-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="dcea8-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dcea8-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcea8-120">Remarks</span></span>

<span data-ttu-id="dcea8-121">Die Struktur **SPropAttrArray** wird vom Daten Property-Objekten, die implementiert werden die [IPropData: IMAPIProp](ipropdataimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dcea8-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="dcea8-122">Darüber hinaus wird von der MAPI-Implementierung der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) also basierend auf strukturierter Speicher.</span><span class="sxs-lookup"><span data-stu-id="dcea8-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dcea8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcea8-123">See also</span></span>



[<span data-ttu-id="dcea8-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dcea8-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="dcea8-125">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcea8-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="dcea8-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="dcea8-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="dcea8-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="dcea8-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="dcea8-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="dcea8-128">MAPI Structures</span></span>](mapi-structures.md)

