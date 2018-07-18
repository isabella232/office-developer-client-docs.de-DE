---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791697"
---
# <a name="flaglist"></a><span data-ttu-id="e353f-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="e353f-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="e353f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e353f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e353f-105">Enthält eine Liste von Flags verwendet, um den Status von Adresseinträge während der Namensauflösungsprozess angeben.</span><span class="sxs-lookup"><span data-stu-id="e353f-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e353f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e353f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e353f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e353f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="e353f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e353f-108">Members</span></span>

 <span data-ttu-id="e353f-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="e353f-109">**cFlags**</span></span>
  
> <span data-ttu-id="e353f-110">Anzahl der MAPI-defined Flags in der Liste.</span><span class="sxs-lookup"><span data-stu-id="e353f-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="e353f-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e353f-111">**ulFlags**</span></span>
  
> <span data-ttu-id="e353f-112">Ein Array von Flags, die den Status des Vorgangs Lösung Namen für einen Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="e353f-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="e353f-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e353f-113">The following flags can be set:</span></span>
    
<span data-ttu-id="e353f-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="e353f-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="e353f-115">Der Empfänger aufgelöst wurde, jedoch nicht für einen Eintrag Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e353f-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="e353f-116">Andere Address Book Container sollte nicht an diesen Empfänger zu beheben versuchen.</span><span class="sxs-lookup"><span data-stu-id="e353f-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="e353f-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="e353f-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="e353f-118">Der Empfänger wurde in eine eindeutige ID aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e353f-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="e353f-119">Andere Address Book Container sollte nicht an diesen Empfänger zu beheben versuchen.</span><span class="sxs-lookup"><span data-stu-id="e353f-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="e353f-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="e353f-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="e353f-121">Der Eintrag wurde nicht behoben.</span><span class="sxs-lookup"><span data-stu-id="e353f-121">The entry has not been resolved.</span></span> <span data-ttu-id="e353f-122">Andere Address Book Container sollte versuchen, diese Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="e353f-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e353f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e353f-123">Remarks</span></span>

<span data-ttu-id="e353f-124">Die Struktur **FLAGLIST** wird als Parameter für [IABContainer](iabcontainer-resolvenames.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="e353f-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="e353f-125">Einzelnen Empfänger aufgelöst werden, ist in eine [ADRLIST](adrlist.md) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="e353f-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="e353f-126">Während der Adressbuchcontainer versucht, jeden Empfänger zu beheben, legt das entsprechende Flag in den entsprechenden Eintrag in der Struktur **FLAGLIST** fest.</span><span class="sxs-lookup"><span data-stu-id="e353f-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="e353f-127">Alle Einträge in der Struktur **FLAGLIST** sind in der gleichen Reihenfolge als die Einträge in der **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e353f-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="e353f-128">Dies vereinfacht die eine Einstellung für die Kennzeichnung mit einem Empfänger zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e353f-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e353f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e353f-129">See also</span></span>



[<span data-ttu-id="e353f-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e353f-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="e353f-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e353f-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="e353f-132">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e353f-132">MAPI Structures</span></span>](mapi-structures.md)

