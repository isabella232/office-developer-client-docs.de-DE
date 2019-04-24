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
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336939"
---
# <a name="flaglist"></a><span data-ttu-id="d9fc9-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="d9fc9-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="d9fc9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9fc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9fc9-105">Enthält eine Liste der Flags, die zum Anzeigen des Status von Adresseinträgen während des Namensauflösungsvorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9fc9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d9fc9-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9fc9-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d9fc9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="d9fc9-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="d9fc9-108">Members</span></span>

 <span data-ttu-id="d9fc9-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="d9fc9-109">**cFlags**</span></span>
  
> <span data-ttu-id="d9fc9-110">Die Anzahl der MAPI-definierten Flags in der Liste.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="d9fc9-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d9fc9-111">**ulFlags**</span></span>
  
> <span data-ttu-id="d9fc9-112">Ein Array von Flags, das den Status des Vorgangs zur Namensauflösung für einen Empfänger bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="d9fc9-113">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d9fc9-113">The following flags can be set:</span></span>
    
<span data-ttu-id="d9fc9-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="d9fc9-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="d9fc9-115">Der Empfänger wurde aufgelöst, jedoch nicht zu einer eindeutigen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="d9fc9-116">Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="d9fc9-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="d9fc9-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="d9fc9-118">Der Empfänger wurde in eine eindeutige Eintrags-ID aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="d9fc9-119">Andere Adressbuchcontainer sollten nicht versuchen, diesen Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="d9fc9-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="d9fc9-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="d9fc9-121">Der Eintrag wurde nicht aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-121">The entry has not been resolved.</span></span> <span data-ttu-id="d9fc9-122">Andere Adressbuchcontainer sollten versuchen, diesen Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9fc9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9fc9-123">Remarks</span></span>

<span data-ttu-id="d9fc9-124">Die **flaglist** -Struktur wird als Parameter für [IABContainer:: ResolveNames](iabcontainer-resolvenames.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="d9fc9-125">Jeder der zu lösenden Empfänger ist in einer [ADRLIST](adrlist.md) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="d9fc9-126">Während der Adressbuchcontainer versucht, jeden Empfänger aufzulösen, wird das entsprechende Flag im entsprechenden Eintrag in der **flaglist** -Struktur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="d9fc9-127">Alle Einträge in der Flaglist \*\*\*\* -Struktur haben dieselbe Reihenfolge wie die Einträge in der **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="d9fc9-128">Dies erleichtert das Zuordnen einer Flag-Einstellung zu einem Empfänger.</span><span class="sxs-lookup"><span data-stu-id="d9fc9-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9fc9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9fc9-129">See also</span></span>



[<span data-ttu-id="d9fc9-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d9fc9-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="d9fc9-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="d9fc9-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="d9fc9-132">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d9fc9-132">MAPI Structures</span></span>](mapi-structures.md)

