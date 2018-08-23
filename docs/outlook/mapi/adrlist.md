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
ms.openlocfilehash: 87b91b66807ce79533029a8d5b5c4956bc4d5ce9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565767"
---
# <a name="adrlist"></a><span data-ttu-id="e46e8-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e46e8-103">ADRLIST</span></span>

<span data-ttu-id="e46e8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e46e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e46e8-105">Beschreibt NULL oder mehrere Eigenschaften, die einen oder mehrere Empfänger angehören.</span><span class="sxs-lookup"><span data-stu-id="e46e8-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e46e8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e46e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e46e8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e46e8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e46e8-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="e46e8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="e46e8-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="e46e8-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="e46e8-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="e46e8-110">Members</span></span>

<span data-ttu-id="e46e8-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="e46e8-111">**cEntries**</span></span>
  
> <span data-ttu-id="e46e8-112">Anzahl der Einträge im Array vom **aEntries** Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="e46e8-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="e46e8-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="e46e8-113">**aEntries**</span></span>
  
> <span data-ttu-id="e46e8-114">Array von [ADRENTRY](adrentry.md) Strukturen, eine Struktur für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="e46e8-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e46e8-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e46e8-115">Remarks</span></span>

<span data-ttu-id="e46e8-116">Eine **ADRLIST** -Struktur enthält ein oder mehrere **ADRENTRY** Strukturen, die die Eigenschaften eines Empfängers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e46e8-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="e46e8-117">Ein Empfänger kann nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e46e8-117">A recipient can be unresolved.</span></span> <span data-ttu-id="e46e8-118">Dies bedeutet, dass es einen Eintrag Bezeichner in dessen Array von Eigenschaftswerten fehlen.</span><span class="sxs-lookup"><span data-stu-id="e46e8-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="e46e8-119">Ein aufgelöster Empfänger bedeutet, dass die **PR\_ENTRYID** -Eigenschaft ([PidTagEntryId](pidtagentryid-canonical-property.md)) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e46e8-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="e46e8-120">Außerdem müssen in der Regel aufgelösten Empfänger eine e-Mail-Adresse die **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e46e8-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="e46e8-121">Die e-Mail-Adresse ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e46e8-121">However, the email address is not required.</span></span> <span data-ttu-id="e46e8-122">**ADRLIST** -Strukturen, beispielsweise dienen zum Beschreiben der Empfängerliste für eine ausgehende Nachricht und MAPI, um die Einträge im Adressbuch anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e46e8-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="e46e8-123">**ADRLIST** -Strukturen so oder ähnlich aus [SRowSet](srowset.md) Strukturen Strukturen für das Darstellen von Zeilen in Tabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e46e8-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="e46e8-124">Diese zwei Strukturen dienen tatsächlich, damit sie austauschbar verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e46e8-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="e46e8-125">Beide enthalten ein Array von Strukturen, die eine Gruppe von Eigenschaften und die Anzahl der Werte im Array beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e46e8-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="e46e8-126">Während der **ADRLIST** -Struktur enthält das Array [ADRENTRY](adrentry.md) Strukturen, in der Struktur **SRowSet** das Array [SRow](srow.md) Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="e46e8-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="e46e8-127">**ADRENTRY** Strukturen und **SRow** Strukturen sind in Layout identisch.</span><span class="sxs-lookup"><span data-stu-id="e46e8-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="e46e8-128">Da **ADRLIST** und **SRowSet** Strukturen dieselben Zuordnungsregeln zu befolgen, kann unverändert eine **SRowSet** -Struktur, die aus der Inhaltstabelle einer Adressbuchcontainer abgerufen wird auf eine **ADRLIST** -Struktur umgewandelt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e46e8-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="e46e8-129">Die folgende Abbildung zeigt das Layout einer **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e46e8-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="e46e8-130">**ADRLIST-Komponenten**</span><span class="sxs-lookup"><span data-stu-id="e46e8-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="e46e8-131">![ADRLIST-Komponenten] (media/amapi_18.gif "ADRLIST-Komponenten")</span><span class="sxs-lookup"><span data-stu-id="e46e8-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="e46e8-132">Die Abschnitte **ADRENTRY** und [SPropValue](spropvalue.md) in einer **ADRLIST** müssen belegt und unabhängig von den anderen Teilen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e46e8-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="e46e8-133">D. h., muss jede **SPropValue** Struktur einzeln zugeordnet werden, nachdem Speicher für die Struktur **ADRENTRY** zugewiesen wurde und freigegeben werden, bevor die Struktur **ADRENTRY** freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e46e8-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="e46e8-134">Diese Unabhängigkeit in die Behandlung von Speicher ermöglicht Empfänger und einzelne Empfängereigenschaften frei hinzugefügt oder aus der Adressliste gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e46e8-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="e46e8-135">Die Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer](mapifreebuffer.md) müssen zum Zuordnen und Freigeben der **ADRLIST** -Struktur und all seiner Teile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e46e8-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="e46e8-136">Wenn eine Empfängerliste zu groß im Arbeitsspeicher ist, können Clients die [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode eine Teilmenge der Liste entwickelt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e46e8-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="e46e8-137">Clients sollten Address Book allgemeine Dialogfelder in dieser Situation nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e46e8-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="e46e8-138">Weitere Informationen zur Verwendung von Arbeitsspeicher für **ADRENTRY** Strukturen, finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="e46e8-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e46e8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e46e8-139">See also</span></span>

- [<span data-ttu-id="e46e8-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="e46e8-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="e46e8-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="e46e8-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="e46e8-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="e46e8-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="e46e8-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e46e8-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="e46e8-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e46e8-144">MAPI Structures</span></span>](mapi-structures.md)

