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
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407256"
---
# <a name="srowset"></a><span data-ttu-id="44f44-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="44f44-103">SRowSet</span></span>

  
  
<span data-ttu-id="44f44-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f44-105">Enthält ein Array von [SRow](srow.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="44f44-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="44f44-106">Jede **SRow** -Struktur beschreibt eine Zeile aus einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="44f44-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44f44-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="44f44-107">Header file:</span></span>  <br/> |<span data-ttu-id="44f44-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="44f44-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="44f44-109">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="44f44-109">Related macros:</span></span>  <br/> |<span data-ttu-id="44f44-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="44f44-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="44f44-111">Members</span><span class="sxs-lookup"><span data-stu-id="44f44-111">Members</span></span>

 <span data-ttu-id="44f44-112">**Krähen**</span><span class="sxs-lookup"><span data-stu-id="44f44-112">**cRows**</span></span>
  
> <span data-ttu-id="44f44-113">Die Anzahl der **SRow** -Strukturen im **aRow** -Element.</span><span class="sxs-lookup"><span data-stu-id="44f44-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="44f44-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="44f44-114">**aRow**</span></span>
  
> <span data-ttu-id="44f44-115">Array von **SRow** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="44f44-115">Array of **SRow** structures.</span></span> <span data-ttu-id="44f44-116">Es gibt eine Struktur für jede Zeile in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="44f44-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="44f44-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44f44-117">Remarks</span></span>

<span data-ttu-id="44f44-118">Eine **SRowSet** -Struktur wird verwendet, um mehrere Datenzeilen aus einer Tabelle zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="44f44-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="44f44-119">**SRowSet** -Strukturen werden in den [IAddrBook](iaddrbookimapiprop.md)-, [ITableData](itabledataiunknown.md)-und [IMAPITable](imapitableiunknown.md) -Schnittstellenmethoden zusätzlich zu den folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="44f44-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="44f44-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="44f44-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="44f44-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="44f44-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="44f44-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="44f44-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="44f44-123">**SRowSet** -Strukturen werden genauso definiert wie [ADRLIST](adrlist.md) -Strukturen, damit die Zeilen einer Empfängertabelle und die Einträge in einer Adressliste gleich behandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="44f44-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="44f44-124">Sowohl **SRowSet** -Strukturen als auch **ADRLIST** -Strukturen können an Methoden wie [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) und [IAddrBook:: Address](iaddrbook-address.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="44f44-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="44f44-125">Außerdem sind die Regeln für die Speicherbelegung für **SRowSet** -Strukturen die gleichen wie für **ADRLIST** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="44f44-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="44f44-126">Zusammenfassend muss jede [SPropValue](spropvalue.md) -Struktur im Array, auf die durch das **lpProps** -Element jeder Zeile im Zeilensatz verwiesen wird, separat mithilfe von [MAPIAllocateBuffer](mapiallocatebuffer.md)zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="44f44-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="44f44-127">Jede Eigenschaftswert Struktur muss auch mithilfe von [mapifreebufferfreigegeben](mapifreebuffer.md) vor der Zuordnung der **SRowSet** -Struktur freigegeben werden, sodass Zeiger auf die zugeordneten **SPropValue** -Strukturen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="44f44-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="44f44-128">Der zugewiesene Arbeitsspeicher einer Zeile kann dann beibehalten und außerhalb des Kontexts der **SRowSet** -Struktur wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44f44-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="44f44-129">Weitere Informationen zur Zuordnung des Speichers für **SRowSet** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="44f44-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44f44-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44f44-130">See also</span></span>



[<span data-ttu-id="44f44-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="44f44-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="44f44-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="44f44-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="44f44-133">SRow</span><span class="sxs-lookup"><span data-stu-id="44f44-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="44f44-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="44f44-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="44f44-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="44f44-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="44f44-136">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="44f44-136">MAPI Structures</span></span>](mapi-structures.md)

