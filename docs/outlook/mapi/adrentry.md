---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791292"
---
# <a name="adrentry"></a><span data-ttu-id="523be-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="523be-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="523be-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="523be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="523be-105">NULL oder mehrere Eigenschaften, die an einen Empfänger gehören beschrieben.</span><span class="sxs-lookup"><span data-stu-id="523be-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="523be-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="523be-106">Header file:</span></span>  <br/> |<span data-ttu-id="523be-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="523be-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="523be-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="523be-108">Members</span></span>

 <span data-ttu-id="523be-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="523be-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="523be-110">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="523be-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="523be-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="523be-111">**cValues**</span></span>
  
> <span data-ttu-id="523be-112">Anzahl der Eigenschaften im Array Wert-Eigenschaft auf den vom **RgPropVals** Member verwiesen.</span><span class="sxs-lookup"><span data-stu-id="523be-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="523be-113">Der **cValues** -Member kann 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="523be-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="523be-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="523be-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="523be-115">Zeiger auf ein Wertearray-Eigenschaft, beschreibt die Eigenschaften für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="523be-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="523be-116">Der **RgPropVals** -Member kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="523be-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="523be-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="523be-117">Remarks</span></span>

<span data-ttu-id="523be-118">Eine Struktur **ADRENTRY** beschreibt die Eigenschaften, die an einen einzelnen Empfänger gehören.</span><span class="sxs-lookup"><span data-stu-id="523be-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="523be-119">Die folgenden: Eigenschaften, die in der Regel verwendet werden, um einen Empfänger zu beschreiben</span><span class="sxs-lookup"><span data-stu-id="523be-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="523be-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="523be-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="523be-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="523be-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="523be-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="523be-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="523be-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="523be-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="523be-124">Wenn eine Eintrags-ID oder **PR_ENTRYID** -Eigenschaft im Array [SPropValue](spropvalue.md) für einen Empfänger angezeigt wird, bedeutet dies, dass der Empfänger aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="523be-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="523be-125">Clients rufen Sie die [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode, um sicherzustellen, dass alle Empfänger in der Empfängerliste von ausgehenden Nachrichten behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="523be-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="523be-126">Nur aufgelösten Empfänger können mit Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="523be-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="523be-127">**ADRENTRY** Strukturen werden in der Regel kombiniert, um ein Array für das **aEntries** Mitglied einer [ADRLIST](adrlist.md) -Struktur zu bilden.</span><span class="sxs-lookup"><span data-stu-id="523be-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="523be-128">**ADRENTRY** Strukturen und [SRow](srow.md) Strukturen sind identisch, da beide Mitglied reserviert, ein Array von Eigenschaftswerten und die Anzahl der Werte im Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="523be-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="523be-129">Während **ADRENTRY** Strukturen kombiniert werden, um das **aEntries** Mitglied einer **ADRLIST** -Struktur zu bilden, werden **SRow** Strukturen kombiniert, um die **aRow** Mitglied einer [SRowSet](srowset.md) Struktur bilden.</span><span class="sxs-lookup"><span data-stu-id="523be-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="523be-130">Beide Arten von Strukturen führen Sie die gleichen Allocation-Regeln, sagen, dass eine **SRowSet** -Struktur, die aus der Inhaltstabelle einer Adressbuchcontainer abgerufen wird auf eine **ADRLIST** -Struktur umgewandelt und verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="523be-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="523be-131">Eine Struktur **ADRENTRY** kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="523be-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="523be-132">Beispielsweise kann eine **ADRENTRY** -Struktur, die in der **ADRLIST** -Struktur, die auf das durch den Parameter _LppAdrList_ in einem Aufruf von **IAddrBook::Address** enthalten ist leer sein, wenn ein Empfänger entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="523be-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="523be-133">Weitere Informationen zur Verwendung von Arbeitsspeicher für **ADRENTRY** Strukturen, finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="523be-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="523be-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="523be-134">See also</span></span>



[<span data-ttu-id="523be-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="523be-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="523be-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="523be-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="523be-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="523be-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="523be-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="523be-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="523be-139">SRow</span><span class="sxs-lookup"><span data-stu-id="523be-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="523be-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="523be-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="523be-141">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="523be-141">MAPI Structures</span></span>](mapi-structures.md)

