---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318095"
---
# <a name="builddisplaytable"></a><span data-ttu-id="ab214-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="ab214-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="ab214-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab214-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab214-105">Erstellt eine Anzeigetabelle aus den Eigenschaftenseiten Daten, die in einer oder mehreren [DTPAGE](dtpage.md) -Strukturen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ab214-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab214-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ab214-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab214-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ab214-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ab214-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ab214-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab214-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab214-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab214-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ab214-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab214-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ab214-111">Service providers</span></span>  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a><span data-ttu-id="ab214-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab214-112">Parameters</span></span>

 <span data-ttu-id="ab214-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ab214-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ab214-114">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab214-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="ab214-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="ab214-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="ab214-116">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab214-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="ab214-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ab214-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ab214-118">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ab214-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="ab214-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="ab214-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="ab214-120">Nicht verwendete sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ab214-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="ab214-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="ab214-121">_hInstance_</span></span>
  
> <span data-ttu-id="ab214-122">in Eine Instanz eines MAPI-Objekts, aus dem **BuildDisplayTable** Ressourcen abruft.</span><span class="sxs-lookup"><span data-stu-id="ab214-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="ab214-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="ab214-123">_cPages_</span></span>
  
> <span data-ttu-id="ab214-124">in Die Anzahl der [DTPAGE](dtpage.md) -Strukturen im Array, auf die durch den _lpPage_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ab214-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="ab214-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="ab214-125">_lpPage_</span></span>
  
> <span data-ttu-id="ab214-126">in Zeiger auf ein Array von **DTPAGE** -Strukturen, die Informationen zu den darzustellenden Tabellenseiten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab214-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="ab214-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab214-127">_ulFlags_</span></span>
  
> <span data-ttu-id="ab214-128">in Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="ab214-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="ab214-129">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ab214-129">The following flag can be set:</span></span>
    
<span data-ttu-id="ab214-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab214-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ab214-131">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ab214-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ab214-132">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ab214-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ab214-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ab214-133">_lppTable_</span></span>
  
> <span data-ttu-id="ab214-134">Out Zeiger auf einen Zeiger auf die Anzeigetabelle, die die [IMAPITable](imapitableiunknown.md) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="ab214-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="ab214-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="ab214-135">_lppTblData_</span></span>
  
> <span data-ttu-id="ab214-136">[in, out] Zeiger auf einen Zeiger auf ein Tabellendaten Objekt, das die [ITableData](itabledataiunknown.md) -Schnittstelle für die im _lppTable_ -Parameter zurückgegebene Tabelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="ab214-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="ab214-137">Wenn kein Tabellendaten Objekt gewünscht wird, sollte _lppTblData_ auf NULL statt auf einen Zeigerwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ab214-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab214-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab214-138">Return value</span></span>

<span data-ttu-id="ab214-139">Keine</span><span class="sxs-lookup"><span data-stu-id="ab214-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab214-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab214-140">Remarks</span></span>

<span data-ttu-id="ab214-141">MAPI verwendet die Funktionen, auf die durch _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen, insbesondere für die Zuweisung von Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="ab214-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab214-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ab214-142">Notes to callers</span></span>

<span data-ttu-id="ab214-143">Alles mögliche wird aus der Dialog-Ressource gelesen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="ab214-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="ab214-144">Der Seitentitel, der das _ulbLpszLabel_ -Element der [DTBLPAGE](dtblpage.md) -Struktur aus dem Dialogfeldtitel in der Ressource liest.</span><span class="sxs-lookup"><span data-stu-id="ab214-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="ab214-145">Alle Steuerelement Titel das heißt, die _ulbLpszLabel_ -Elemente anderer Steuerelementstrukturen Lesen aus dem Steuerelementtext in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ab214-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="ab214-146">**BuildDisplayTable** überschreibt alles, was in den Eingabe Steuerstrukturen mit Informationen aus der Dialog-Ressource übergeben wurde, was besagt, dass der Aufrufer von **BuildDisplayTable** die Seiten-oder Steuerelement Titel nicht dynamisch angeben kann.</span><span class="sxs-lookup"><span data-stu-id="ab214-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="ab214-147">Aufrufer, die dies tun müssen, können **BuildDisplayTable** das Tabellendaten Objekt in _lppTableData_ zurückgeben und Zeilen darin ändern; Sie können stattdessen die Anzeigetabelle manuell in einem Tabellendaten Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab214-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="ab214-148">Wenn _lppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter für das Freigeben des Table-Datenobjekts verantwortlich, wenn es mit der Anzeigetabelle abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ab214-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

