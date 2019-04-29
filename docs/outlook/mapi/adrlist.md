---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415915"
---
# <a name="adrlist"></a><span data-ttu-id="a955d-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="a955d-103">ADRLIST</span></span>

<span data-ttu-id="a955d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a955d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a955d-105">Beschreibt NULL oder mehr Eigenschaften, die zu einem oder mehreren Empfängern gehören.</span><span class="sxs-lookup"><span data-stu-id="a955d-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a955d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a955d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a955d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a955d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a955d-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="a955d-108">Related macros:</span></span>  <br/> |<span data-ttu-id="a955d-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="a955d-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="a955d-110">Members</span><span class="sxs-lookup"><span data-stu-id="a955d-110">Members</span></span>

<span data-ttu-id="a955d-111">**Zentriert**</span><span class="sxs-lookup"><span data-stu-id="a955d-111">**cEntries**</span></span>
  
> <span data-ttu-id="a955d-112">Die Anzahl der Einträge im vom **aEntries** -Element angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="a955d-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="a955d-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="a955d-113">**aEntries**</span></span>
  
> <span data-ttu-id="a955d-114">Array von [Miet](adrentry.md) Strukturen, eine Struktur für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="a955d-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a955d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a955d-115">Remarks</span></span>

<span data-ttu-id="a955d-116">Eine **ADRLIST** -Struktur enthält eine oder mehrere **Miet** Strukturen, die jeweils die Eigenschaften eines Empfängers beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a955d-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="a955d-117">Ein Empfänger kann nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a955d-117">A recipient can be unresolved.</span></span> <span data-ttu-id="a955d-118">Dies bedeutet, dass es in seinem Array von Eigenschaftswerten keine Eintrags-ID gibt.</span><span class="sxs-lookup"><span data-stu-id="a955d-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="a955d-119">Ein aufgelöster Empfänger bedeutet, dass die **\_PR** -Eintrags-Eigenschaft ([PidTagEntryId](pidtagentryid-canonical-property.md)) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a955d-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="a955d-120">In der Regel haben aufgelöste Empfänger auch eine e-Mail-Adresse der **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a955d-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="a955d-121">Die e-Mail-Adresse ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a955d-121">However, the email address is not required.</span></span> <span data-ttu-id="a955d-122">**ADRLIST** -Strukturen werden zum Beispiel verwendet, um die Empfängerliste für eine ausgehende Nachricht und MAPI zum Anzeigen der Einträge im Adressbuch zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a955d-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="a955d-123">**ADRLIST** -Strukturen ähneln [SRowSet](srowset.md) Strukturen der Strukturen für die Darstellung von Zeilen in Tabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a955d-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="a955d-124">Tatsächlich sind diese beiden Strukturen so konzipiert, dass Sie synonym verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a955d-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="a955d-125">Beide enthalten ein Array von Strukturen, die eine Gruppe von Eigenschaften und die Anzahl der Werte im Array beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a955d-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="a955d-126">Während in der **ADRLIST** -Struktur das Array die [Miet](adrentry.md) Strukturen enthält, enthält das Array in der **SRowSet** -Struktur [SRow](srow.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a955d-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="a955d-127">**Miet** Strukturen und **SRow** -Strukturen sind im Layout identisch.</span><span class="sxs-lookup"><span data-stu-id="a955d-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="a955d-128">Da **ADRLIST** -und **SRowSet** -Strukturen denselben Zuordnungsregeln folgen, kann eine **SRowSet** -Struktur, die aus der Inhaltstabelle eines Adressbuch Containers abgerufen wird, in eine **ADRLIST** -Struktur umgewandelt und unverändert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a955d-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="a955d-129">Die folgende Abbildung zeigt das Layout einer **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a955d-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="a955d-130">**ADRLIST-Komponenten**</span><span class="sxs-lookup"><span data-stu-id="a955d-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="a955d-131">![ADRLIST-Komponenten] (media/amapi_18.gif "ADRLIST-Komponenten")</span><span class="sxs-lookup"><span data-stu-id="a955d-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="a955d-132">Die **Miet** -und [SPropValue](spropvalue.md) -Teile in einer **ADRLIST** -Struktur müssen unabhängig von den anderen Teilen reserviert und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a955d-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="a955d-133">Das heißt, jede **SPropValue** -Struktur muss einzeln zugeordnet werden, nachdem der Speicher für die **Miet** Struktur reserviert und freigegeben wurde, bevor die **Miet** Struktur freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a955d-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="a955d-134">Durch diese Unabhängigkeit im Umgang mit Arbeitsspeicher können Empfänger und einzelne Empfänger Eigenschaften in der Adressliste frei hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a955d-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="a955d-135">Die [MAPIAllocateBuffer](mapiallocatebuffer.md) -und [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktionen müssen verwendet werden, um die **ADRLIST** -Struktur und alle zugehörigen Komponenten zuzuweisen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a955d-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="a955d-136">Wenn eine Empfängerliste zu umfangreich ist, um Sie in den Arbeitsspeicher zu integrieren, können Clients die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode aufrufen, um mit einer Teilmenge der Liste zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a955d-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="a955d-137">In dieser Situation sollten Clients nicht die allgemeinen Dialogfelder des Adressbuchs verwenden.</span><span class="sxs-lookup"><span data-stu-id="a955d-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="a955d-138">Weitere Informationen zum Zuweisen von Arbeitsspeicher für **Miet** Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="a955d-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a955d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a955d-139">See also</span></span>

- [<span data-ttu-id="a955d-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="a955d-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="a955d-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="a955d-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="a955d-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="a955d-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="a955d-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="a955d-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="a955d-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a955d-144">MAPI Structures</span></span>](mapi-structures.md)

