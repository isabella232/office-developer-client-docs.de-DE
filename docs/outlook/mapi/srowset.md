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
# <a name="srowset"></a><span data-ttu-id="93275-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="93275-103">SRowSet</span></span>

  
  
<span data-ttu-id="93275-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93275-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93275-105">Enthält ein Array von [SRow-Strukturen.](srow.md)</span><span class="sxs-lookup"><span data-stu-id="93275-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="93275-106">Jede **SRow-Struktur** beschreibt eine Zeile aus einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="93275-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93275-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="93275-107">Header file:</span></span>  <br/> |<span data-ttu-id="93275-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93275-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="93275-109">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="93275-109">Related macros:</span></span>  <br/> |<span data-ttu-id="93275-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="93275-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="93275-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="93275-111">Members</span></span>

 <span data-ttu-id="93275-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="93275-112">**cRows**</span></span>
  
> <span data-ttu-id="93275-113">Anzahl der **SRow-Strukturen** im **aRow-Element.**</span><span class="sxs-lookup"><span data-stu-id="93275-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="93275-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="93275-114">**aRow**</span></span>
  
> <span data-ttu-id="93275-115">Array von **SRow-Strukturen.**</span><span class="sxs-lookup"><span data-stu-id="93275-115">Array of **SRow** structures.</span></span> <span data-ttu-id="93275-116">Es gibt eine Struktur für jede Zeile in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="93275-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="93275-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93275-117">Remarks</span></span>

<span data-ttu-id="93275-118">Eine **SRowSet-Struktur** wird verwendet, um mehrere Datenzeilen aus einer Tabelle zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="93275-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="93275-119">**SRowSet-Strukturen** werden zusätzlich zu den folgenden Funktionen in den [Schnittstellenmethoden IAddrBook,](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)und [IMAPITable](imapitableiunknown.md) verwendet:</span><span class="sxs-lookup"><span data-stu-id="93275-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="93275-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="93275-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="93275-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="93275-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="93275-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="93275-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="93275-123">**SRowSet-Strukturen** sind identisch mit [ADRLIST-Strukturen](adrlist.md) definiert, damit die Zeilen einer Empfängertabelle und die Einträge in einer Adressliste gleich behandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="93275-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="93275-124">**Sowohl SRowSet-Strukturen** als auch **ADRLIST-Strukturen** können an Methoden wie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) und [IAddrBook::Address übergeben werden.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="93275-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="93275-125">Außerdem sind die Regeln für die Speicherzuweisung für **SRowSet-Strukturen** mit den Regeln für **ADRLIST-Strukturen** identisch.</span><span class="sxs-lookup"><span data-stu-id="93275-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="93275-126">Zusammenfassend muss jede [SPropValue-Struktur](spropvalue.md) im Array, auf die das **lpProps-Mitglied** jeder Zeile im Zeilensatz verweist, mithilfe von [MAPIAllocateBuffer](mapiallocatebuffer.md)separat zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="93275-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="93275-127">Jede Eigenschaftswertstruktur muss auch mit [MAPIFreeBuffer](mapifreebuffer.md) vor der Deallocation der **SRowSet-Struktur** zugeordnet werden, damit Zeiger auf die zugewiesenen **SPropValue-Strukturen** nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="93275-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="93275-128">Der zugewiesene Speicher einer Zeile kann dann außerhalb des Kontexts der **SRowSet-Struktur beibehalten und wiederverwendet** werden.</span><span class="sxs-lookup"><span data-stu-id="93275-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="93275-129">Weitere Informationen dazu, wie der Arbeitsspeicher für **SRowSet-Strukturen** zugewiesen werden soll, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="93275-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93275-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93275-130">See also</span></span>



[<span data-ttu-id="93275-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="93275-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="93275-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="93275-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="93275-133">SRow</span><span class="sxs-lookup"><span data-stu-id="93275-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="93275-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="93275-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="93275-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="93275-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="93275-136">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="93275-136">MAPI Structures</span></span>](mapi-structures.md)

