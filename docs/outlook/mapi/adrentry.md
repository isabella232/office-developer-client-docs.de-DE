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
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330226"
---
# <a name="adrentry"></a><span data-ttu-id="9a0f3-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="9a0f3-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="9a0f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a0f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a0f3-105">Beschreibt NULL oder mehr Eigenschaften, die zu einem Empfänger gehören.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a0f3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9a0f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a0f3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9a0f3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="9a0f3-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="9a0f3-108">Members</span></span>

 <span data-ttu-id="9a0f3-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="9a0f3-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="9a0f3-110">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9a0f3-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9a0f3-111">**cValues**</span></span>
  
> <span data-ttu-id="9a0f3-112">Die Anzahl der Eigenschaften im Eigenschafts Wertarray, auf die durch das **rgPropVals** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="9a0f3-113">Das **cValues** -Element kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="9a0f3-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="9a0f3-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="9a0f3-115">Zeiger auf ein Eigenschaftswert Array, das die Eigenschaften für den Empfänger beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="9a0f3-116">Das **rgPropVals** -Element kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9a0f3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a0f3-117">Remarks</span></span>

<span data-ttu-id="9a0f3-118">In einer **Miet** Struktur werden Eigenschaften beschrieben, die zu einem einzelnen Empfänger gehören.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="9a0f3-119">Zu den Eigenschaften, die in der Regel zur Beschreibung eines Empfängers verwendet werden, gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="9a0f3-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="9a0f3-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a0f3-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="9a0f3-121">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a0f3-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="9a0f3-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a0f3-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="9a0f3-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a0f3-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="9a0f3-124">Wenn im [SPropValue](spropvalue.md) -Array für einen Empfänger eine Eintrags-ID oder eine **PR_ENTRYID** -Eigenschaft angezeigt wird, bedeutet dies, dass der Empfänger aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="9a0f3-125">Clients rufen die [IAddrBook::](iaddrbook-resolvename.md) ResolveName-Methode auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste einer ausgehenden Nachricht aufgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="9a0f3-126">Nur aufgelöste Empfänger können mit Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="9a0f3-127">**Miet** Strukturen werden in der Regel kombiniert, um ein Array für das **aEntries** -Element einer [ADRLIST](adrlist.md) -Struktur zu bilden.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="9a0f3-128">**Miet** Strukturen und [SRow](srow.md) -Strukturen sind identisch, da Sie sowohl ein reserviertes Element, ein Array mit Eigenschaftswerten als auch eine Anzahl von Werten im Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="9a0f3-129">Während die **Miet** Strukturen zu dem **aEntries** -Element einer **ADRLIST** -Struktur kombiniert werden, werden **SRow** -Strukturen kombiniert, um das **aRow** -Element einer [SRowSet](srowset.md) -Struktur zu bilden.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="9a0f3-130">Beide Arten von Strukturen folgen den gleichen Zuordnungsregeln, was bedeutet, dass eine **SRowSet** -Struktur, die aus der Inhaltstabelle eines Adressbuch Containers abgerufen wird, in eine **ADRLIST** -Struktur umgewandelt und unverändert verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="9a0f3-131">Eine **Miet** Struktur kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="9a0f3-132">Beispielsweise kann eine in der **ADRLIST** -Struktur enthaltene **Miet** Struktur, auf die durch den _lppAdrList_ -Parameter in einem Aufruf von **IAddrBook:: Address** verwiesen wird, leer sein, wenn ein Empfänger entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9a0f3-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="9a0f3-133">Weitere Informationen zum Zuweisen von Arbeitsspeicher für **Miet** Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="9a0f3-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a0f3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a0f3-134">See also</span></span>



[<span data-ttu-id="9a0f3-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="9a0f3-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="9a0f3-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="9a0f3-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="9a0f3-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9a0f3-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9a0f3-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9a0f3-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9a0f3-139">SRow</span><span class="sxs-lookup"><span data-stu-id="9a0f3-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="9a0f3-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9a0f3-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="9a0f3-141">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9a0f3-141">MAPI Structures</span></span>](mapi-structures.md)

