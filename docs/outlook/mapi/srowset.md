---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795640"
---
# <a name="srowset"></a><span data-ttu-id="95af9-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="95af9-103">SRowSet</span></span>

  
  
<span data-ttu-id="95af9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95af9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95af9-105">Enthält ein Array von [SRow](srow.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="95af9-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="95af9-106">Jede **SRow** Struktur beschreibt eine Zeile aus einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="95af9-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95af9-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="95af9-107">Header file:</span></span>  <br/> |<span data-ttu-id="95af9-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95af9-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="95af9-109">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="95af9-109">Related macros:</span></span>  <br/> |<span data-ttu-id="95af9-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="95af9-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="95af9-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="95af9-111">Members</span></span>

 <span data-ttu-id="95af9-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="95af9-112">**cRows**</span></span>
  
> <span data-ttu-id="95af9-113">Anzahl der **SRow** Strukturen im **aRow** -Member.</span><span class="sxs-lookup"><span data-stu-id="95af9-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="95af9-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="95af9-114">**aRow**</span></span>
  
> <span data-ttu-id="95af9-115">Array von Strukturen **SRow** .</span><span class="sxs-lookup"><span data-stu-id="95af9-115">Array of **SRow** structures.</span></span> <span data-ttu-id="95af9-116">Es ist eine Struktur für jede Zeile in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="95af9-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="95af9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95af9-117">Remarks</span></span>

<span data-ttu-id="95af9-118">Eine Struktur **' srowset '** wird verwendet, um mehrere Zeilen von Daten aus einer Tabelle zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="95af9-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="95af9-119">**SRowSet** Strukturen werden in der [IAddrBook](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)und [IMAPITable](imapitableiunknown.md) -Schnittstellenmethoden, zusätzlich zu den folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="95af9-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="95af9-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="95af9-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="95af9-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="95af9-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="95af9-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="95af9-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="95af9-123">**SRowSet** Strukturen definiert sind identisch mit [ADRLIST](adrlist.md) -Strukturen, die die Zeilen einer Tabelle Empfänger und die Einträge in einer Adressliste sein dürfen die gleiche behandelt.</span><span class="sxs-lookup"><span data-stu-id="95af9-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="95af9-124">**SRowSet** Strukturen und **ADRLIST** Strukturen können an Methoden wie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) und [IAddrBook::Address](iaddrbook-address.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="95af9-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="95af9-125">Darüber hinaus sind die Regeln für die Zuweisung von virtuellem Speicher für **SRowSet** Strukturen die gleichen wie bei **ADRLIST** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="95af9-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="95af9-126">Zusammenfassend lässt sich sagen, muss jede [SPropValue](spropvalue.md) Struktur im Array zum Festlegen von der **LpProps** Mitglied jede Zeile in der Zeile gezeigt separat mithilfe [MAPIAllocateBuffer](mapiallocatebuffer.md)zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="95af9-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="95af9-127">Jede Eigenschaft Wert Struktur muss auch using [MAPIFreeBuffer](mapifreebuffer.md) vor der Freigabe der **SRowSet** -Struktur, sodass keine Verweise auf die zugewiesenen **SPropValue** Strukturen verloren freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95af9-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="95af9-128">Eine Zeile werden reservierte Speicher kann dann beibehalten und außerhalb des Kontexts der Struktur **SRowSet** wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="95af9-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="95af9-129">Weitere Informationen dazu, wie der Speicher für **SRowSet** Strukturen zugewiesen werden sollen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="95af9-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95af9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95af9-130">See also</span></span>



[<span data-ttu-id="95af9-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="95af9-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="95af9-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="95af9-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="95af9-133">SRow</span><span class="sxs-lookup"><span data-stu-id="95af9-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="95af9-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="95af9-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="95af9-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="95af9-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="95af9-136">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="95af9-136">MAPI Structures</span></span>](mapi-structures.md)

