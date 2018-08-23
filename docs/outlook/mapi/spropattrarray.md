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
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577681"
---
# <a name="spropattrarray"></a><span data-ttu-id="99fc3-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="99fc3-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="99fc3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99fc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99fc3-105">Enthält eine Liste der Attribute für die Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="99fc3-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99fc3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="99fc3-106">Header file:</span></span>  <br/> |<span data-ttu-id="99fc3-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="99fc3-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="99fc3-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="99fc3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="99fc3-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="99fc3-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="99fc3-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="99fc3-110">Members</span></span>

 <span data-ttu-id="99fc3-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="99fc3-111">**cValues**</span></span>
  
> <span data-ttu-id="99fc3-112">Anzahl der Attribute im **aPropAttr** -Member.</span><span class="sxs-lookup"><span data-stu-id="99fc3-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="99fc3-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="99fc3-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="99fc3-114">Ein Array von Eigenschaftsattribute.</span><span class="sxs-lookup"><span data-stu-id="99fc3-114">An array of property attributes.</span></span> <span data-ttu-id="99fc3-115">Gültige Werte für Attribute sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="99fc3-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="99fc3-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="99fc3-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="99fc3-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="99fc3-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="99fc3-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="99fc3-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="99fc3-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="99fc3-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99fc3-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="99fc3-120">Remarks</span></span>

<span data-ttu-id="99fc3-121">Die Struktur **SPropAttrArray** wird vom Daten Property-Objekten, die implementiert werden die [IPropData: IMAPIProp](ipropdataimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="99fc3-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="99fc3-122">Darüber hinaus wird von der MAPI-Implementierung der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) also basierend auf strukturierter Speicher.</span><span class="sxs-lookup"><span data-stu-id="99fc3-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99fc3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99fc3-123">See also</span></span>



[<span data-ttu-id="99fc3-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="99fc3-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="99fc3-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99fc3-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="99fc3-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="99fc3-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="99fc3-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="99fc3-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="99fc3-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="99fc3-128">MAPI Structures</span></span>](mapi-structures.md)

