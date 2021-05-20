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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431596"
---
# <a name="builddisplaytable"></a><span data-ttu-id="9cf37-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="9cf37-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="9cf37-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cf37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cf37-105">Erstellt eine Anzeigetabelle aus den Eigenschaftenseitendaten, die in einer oder mehreren [DTPAGE-Strukturen enthalten](dtpage.md) sind.</span><span class="sxs-lookup"><span data-stu-id="9cf37-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cf37-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9cf37-106">Header file:</span></span>  <br/> |<span data-ttu-id="9cf37-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9cf37-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9cf37-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9cf37-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9cf37-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9cf37-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9cf37-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9cf37-110">Called by:</span></span>  <br/> |<span data-ttu-id="9cf37-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9cf37-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9cf37-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cf37-112">Parameters</span></span>

 <span data-ttu-id="9cf37-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="9cf37-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="9cf37-114">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cf37-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="9cf37-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="9cf37-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="9cf37-116">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cf37-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="9cf37-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="9cf37-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="9cf37-118">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cf37-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="9cf37-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="9cf37-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="9cf37-120">Nicht verwendet; sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9cf37-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="9cf37-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="9cf37-121">_hInstance_</span></span>
  
> <span data-ttu-id="9cf37-122">[in] Eine Instanz eines MAPI-Objekts, aus dem **BuildDisplayTable** Ressourcen abruft.</span><span class="sxs-lookup"><span data-stu-id="9cf37-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="9cf37-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="9cf37-123">_cPages_</span></span>
  
> <span data-ttu-id="9cf37-124">[in] Anzahl der [DTPAGE-Strukturen](dtpage.md) im Array, auf die der  _lpPage-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="9cf37-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="9cf37-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="9cf37-125">_lpPage_</span></span>
  
> <span data-ttu-id="9cf37-126">[in] Zeiger auf ein Array von **DTPAGE-Strukturen,** die Informationen über die zu erstellende Anzeigetabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="9cf37-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="9cf37-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9cf37-127">_ulFlags_</span></span>
  
> <span data-ttu-id="9cf37-128">[in] Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="9cf37-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="9cf37-129">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9cf37-129">The following flag can be set:</span></span>
    
<span data-ttu-id="9cf37-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9cf37-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9cf37-131">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="9cf37-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9cf37-132">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="9cf37-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="9cf37-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9cf37-133">_lppTable_</span></span>
  
> <span data-ttu-id="9cf37-134">[out] Zeiger auf einen Zeiger auf die Anzeigetabelle, die die [IMAPITable-Schnittstelle verfügbar](imapitableiunknown.md) macht.</span><span class="sxs-lookup"><span data-stu-id="9cf37-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="9cf37-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="9cf37-135">_lppTblData_</span></span>
  
> <span data-ttu-id="9cf37-136">[in, out] Zeiger auf einen Zeiger auf ein Tabellendatenobjekt, das die [ITableData-Schnittstelle](itabledataiunknown.md) in der im  _lppTable-Parameter_ zurückgegebenen Tabelle verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="9cf37-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="9cf37-137">Wenn kein Tabellendatenobjekt gewünscht wird,  _sollte lppTblData_ auf NULL anstelle eines Zeigerwerts festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9cf37-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9cf37-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cf37-138">Return value</span></span>

<span data-ttu-id="9cf37-139">Keine</span><span class="sxs-lookup"><span data-stu-id="9cf37-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cf37-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9cf37-140">Remarks</span></span>

<span data-ttu-id="9cf37-141">MAPI verwendet die Funktionen, auf die  _von lpAllocateBuffer_,  _lpAllocateMore_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation, insbesondere zum Zuordnen von Arbeitsspeicher für Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="9cf37-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9cf37-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9cf37-142">Notes to callers</span></span>

<span data-ttu-id="9cf37-143">Alles Mögliche wird aus der Dialogressource gelesen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="9cf37-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="9cf37-144">Der Seitentitel, d. h. das  _ulbLpszLabel-Element_ der [DTBLPAGE-Struktur,](dtblpage.md) liest aus dem Dialogfeldtitel in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9cf37-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="9cf37-145">Alle Steuerelementtitel, d. h.  _die ulbLpszLabel-Elemente_ anderer Steuerelementstrukturen lesen aus dem Steuerelementtext in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9cf37-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="9cf37-146">**BuildDisplayTable** überschreibt alles, was in den Eingabesteuerelementstrukturen übergeben wird, mit Informationen aus der Dialogressource, was bedeutet, dass der Aufrufer von **BuildDisplayTable** Seiten- oder Steuerelementtitel nicht dynamisch angeben kann.</span><span class="sxs-lookup"><span data-stu-id="9cf37-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="9cf37-147">Anrufer, die dies tun müssen, können **buildDisplayTable** das  _Tabellendatenobjekt in lppTableData_ zurückgeben und Zeilen ändern. oder sie können die Anzeigetabelle stattdessen in einem Tabellendatenobjekt von Hand erstellen.</span><span class="sxs-lookup"><span data-stu-id="9cf37-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="9cf37-148">Wenn  _lppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter dafür verantwortlich, das Tabellendatenobjekt frei zu machen, wenn es mit der Anzeigetabelle abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9cf37-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

