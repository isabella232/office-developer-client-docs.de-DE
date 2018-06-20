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
ms.openlocfilehash: b821394f32a938f4878ee93e685aafbeb0786597
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791386"
---
# <a name="builddisplaytable"></a><span data-ttu-id="028af-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="028af-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="028af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="028af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="028af-105">Erstellt eine zeigt die Tabelle aus der Eigenschaftendaten-Seite, die in eine oder mehrere [DTPAGE](dtpage.md) Strukturen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="028af-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="028af-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="028af-106">Header file:</span></span>  <br/> |<span data-ttu-id="028af-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="028af-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="028af-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="028af-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="028af-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="028af-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="028af-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="028af-110">Called by:</span></span>  <br/> |<span data-ttu-id="028af-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="028af-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="028af-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="028af-112">Parameters</span></span>

 <span data-ttu-id="028af-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="028af-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="028af-114">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="028af-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="028af-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="028af-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="028af-116">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="028af-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="028af-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="028af-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="028af-118">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="028af-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="028af-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="028af-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="028af-120">Nicht verwendete; sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="028af-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="028af-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="028af-121">_hInstance_</span></span>
  
> <span data-ttu-id="028af-122">[in] Eine Instanz eines MAPI-Objekts aus dem **BuildDisplayTable** Ressourcen abruft.</span><span class="sxs-lookup"><span data-stu-id="028af-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="028af-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="028af-123">_cPages_</span></span>
  
> <span data-ttu-id="028af-124">[in] Anzahl der [DTPAGE](dtpage.md) Strukturen im Array auf den durch den Parameter _LpPage_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="028af-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="028af-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="028af-125">_lpPage_</span></span>
  
> <span data-ttu-id="028af-126">[in] Zeiger auf ein Array von **DTPAGE** -Strukturen, die enthalten Informationen zu den Seiten des Display-Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="028af-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="028af-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="028af-127">_ulFlags_</span></span>
  
> <span data-ttu-id="028af-128">[in] Bitmaske der Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="028af-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="028af-129">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="028af-129">The following flag can be set:</span></span>
    
<span data-ttu-id="028af-130">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="028af-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="028af-131">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="028af-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="028af-132">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="028af-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="028af-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="028af-133">_lppTable_</span></span>
  
> <span data-ttu-id="028af-134">[out] Zeiger auf einen Zeiger auf die Tabelle anzeigen, die die [IMAPITable](imapitableiunknown.md) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="028af-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="028af-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="028af-135">_lppTblData_</span></span>
  
> <span data-ttu-id="028af-136">[in, out] Zeiger auf einen Zeiger auf eine Tabelle Datenobjekt Verfügbarmachen der [ITableData](itabledataiunknown.md) -Schnittstelle in der Tabelle, die in der _LppTable_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="028af-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="028af-137">Keine Tabelle Datenobjekt gewünscht wird, sollte _LppTblData_ anstatt einen Zeigerwert auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="028af-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="028af-138">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="028af-138">Return value</span></span>

<span data-ttu-id="028af-139">Keine</span><span class="sxs-lookup"><span data-stu-id="028af-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="028af-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="028af-140">Remarks</span></span>

<span data-ttu-id="028af-141">MAPI verwendet, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen, um Funktionen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="028af-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="028af-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="028af-142">Notes to callers</span></span>

<span data-ttu-id="028af-143">Alles möglich aus die Ressource lesen ist, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="028af-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="028af-144">Titel der Seite, die, die _UlbLpszLabel_ Member der [DTBLPAGE](dtblpage.md) -Struktur aus dem Dialogfeldtitel in der Ressource lesen.</span><span class="sxs-lookup"><span data-stu-id="028af-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="028af-145">Alle Steuerelement Titel, der, die _UlbLpszLabel_ Mitglieder der anderen Steuerstrukturen Lesen aus dem Steuerelementtext in der Ressource.</span><span class="sxs-lookup"><span data-stu-id="028af-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="028af-146">**BuildDisplayTable** überschreibt Suchzeichenfolge übergeben in die Strukturen Eingabesteuerelement mit Informationen über die Ressource, was bedeutet, dass der Aufrufer **BuildDisplayTable** dynamisch Seite oder ein Steuerelement Titel angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="028af-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="028af-147">Anrufer, die werden müssen, die **BuildDisplayTable** haben, können das Table-Datenobjekt in _LppTableData_ zurückgeben und ändern Sie Zeilen darin; oder sie können die Anzeige Tabelle stattdessen manuell in einem Table-Datenobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="028af-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="028af-148">Wenn _LppTableData_ nicht auf NULL festgelegt ist, ist der Anbieter verantwortlich für die Freigabe des Tabellenobjekts Daten Beendigung mit der Tabelle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="028af-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

