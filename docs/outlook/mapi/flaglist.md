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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412975"
---
# <a name="flaglist"></a><span data-ttu-id="54899-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="54899-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="54899-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54899-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54899-105">Enthält eine Liste der Flags, die verwendet werden, um den Status von Adresseinträgen während des Namensauflösungsprozesses anzugeben.</span><span class="sxs-lookup"><span data-stu-id="54899-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54899-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="54899-106">Header file:</span></span>  <br/> |<span data-ttu-id="54899-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54899-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="54899-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="54899-108">Members</span></span>

 <span data-ttu-id="54899-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="54899-109">**cFlags**</span></span>
  
> <span data-ttu-id="54899-110">Anzahl der MAPI-definierten Flags in der Liste.</span><span class="sxs-lookup"><span data-stu-id="54899-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="54899-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="54899-111">**ulFlags**</span></span>
  
> <span data-ttu-id="54899-112">Ein Array von Kennzeichen, das den Status des Namensauflösungsvorgangs für einen Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="54899-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="54899-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="54899-113">The following flags can be set:</span></span>
    
<span data-ttu-id="54899-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="54899-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="54899-115">Der Empfänger wurde aufgelöst, jedoch nicht in einen eindeutigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="54899-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="54899-116">Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger zu beheben.</span><span class="sxs-lookup"><span data-stu-id="54899-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="54899-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="54899-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="54899-118">Der Empfänger wurde in einen eindeutigen Eintragsbezeichner aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="54899-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="54899-119">Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger zu beheben.</span><span class="sxs-lookup"><span data-stu-id="54899-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="54899-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="54899-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="54899-121">Der Eintrag wurde nicht aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="54899-121">The entry has not been resolved.</span></span> <span data-ttu-id="54899-122">Andere Adressbuchcontainer sollten versuchen, diesen Empfänger zu beheben.</span><span class="sxs-lookup"><span data-stu-id="54899-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54899-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54899-123">Remarks</span></span>

<span data-ttu-id="54899-124">Die **FLAGLIST-Struktur** wird als Parameter für [IABContainer::ResolveNames verwendet.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="54899-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="54899-125">Jeder der zu auflösende Empfänger ist in einer [ADRLIST-Struktur](adrlist.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="54899-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="54899-126">Wenn der Adressbuchcontainer versucht, jeden Empfänger zu beheben, legt er das entsprechende Flag im entsprechenden Eintrag in der **FLAGLIST-Struktur** fest.</span><span class="sxs-lookup"><span data-stu-id="54899-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="54899-127">Alle Einträge in der **FLAGLIST-Struktur** befinden sich in der gleichen Reihenfolge wie die Einträge in der **ADRLIST-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="54899-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="54899-128">Dies erleichtert das Zuordnen einer Kennzeichnungseinstellung zu einem Empfänger.</span><span class="sxs-lookup"><span data-stu-id="54899-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54899-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54899-129">See also</span></span>



[<span data-ttu-id="54899-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="54899-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="54899-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="54899-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="54899-132">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="54899-132">MAPI Structures</span></span>](mapi-structures.md)

