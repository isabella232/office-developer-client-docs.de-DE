---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 241fac608552036e4706956cbe79524aaedacec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576848"
---
# <a name="screlocprops"></a><span data-ttu-id="2416e-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="2416e-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="2416e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2416e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2416e-105">Passt die Zeiger in ein Array [SPropValue](spropvalue.md) , nachdem das Array und seine Daten kopiert oder an einen neuen Speicherort verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="2416e-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2416e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2416e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2416e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2416e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2416e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2416e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2416e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2416e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2416e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2416e-110">Called by:</span></span>  <br/> |<span data-ttu-id="2416e-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2416e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="2416e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2416e-112">Parameters</span></span>

 <span data-ttu-id="2416e-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="2416e-113">_cprop_</span></span>
  
> <span data-ttu-id="2416e-114">[in] Anzahl der Eigenschaften im Array auf den durch den Parameter _Rgprop_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="2416e-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="2416e-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="2416e-115">_rgprop_</span></span>
  
> <span data-ttu-id="2416e-116">[in] Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die für die Zeiger sind angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="2416e-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="2416e-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="2416e-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="2416e-118">[in] Zeiger auf die ursprüngliche Basisadresse des Arrays auf den durch den Parameter _Rgprop_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="2416e-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="2416e-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="2416e-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="2416e-120">[in] Zeiger auf die neue Basisadresse des Arrays auf den durch den Parameter _Rgprop_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="2416e-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="2416e-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="2416e-121">_pcb_</span></span>
  
> <span data-ttu-id="2416e-122">[in, out] Optional Zeiger auf die Größe des durch den Parameter _PvBaseNew_ angegebenen Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2416e-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="2416e-123">Wenn nicht NULL-Wert der _pcb_ -Parameter wird festgelegt, um die Anzahl von Bytes, die im Parameter _PvD_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2416e-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2416e-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2416e-124">Return value</span></span>

<span data-ttu-id="2416e-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="2416e-125">S_OK</span></span>
  
> <span data-ttu-id="2416e-126">Zeiger wurden erfolgreich angepasst.</span><span class="sxs-lookup"><span data-stu-id="2416e-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="2416e-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2416e-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="2416e-128">Einer oder beide Parameter war ungültig oder eine unbekannte Eigenschaftentyp aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2416e-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2416e-129">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="2416e-129">Remarks</span></span>

<span data-ttu-id="2416e-130">Die Funktion **ScRelocProps** wirkt sich auf der Annahme, die das Wertearray-Eigenschaft für das Zeiger angepasst werden in einem einzigen Aufruf ähnlich einem Aufruf der Funktion **ScCopyProps** ursprünglich belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="2416e-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="2416e-131">Wenn eine Clientanwendung oder Service Provider-Eigenschaft den Wert funktionsfähig ist, die aus getrennten Blöcke des Arbeitsspeichers erstellt wird, sollte [ScCopyProps](sccopyprops.md) zum Kopieren von Eigenschaften stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2416e-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="2416e-132">**ScRelocProps** wird verwendet, um die Gültigkeit der Zeiger in ein Array [SPropValue](spropvalue.md) verwalten.</span><span class="sxs-lookup"><span data-stu-id="2416e-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="2416e-133">Um den Zeiger Gültigkeit darzustellen, wenn ein solches Array zu schreiben und Lesen Sie es von einem Datenträger, führen Sie die folgenden Vorgänge aus:</span><span class="sxs-lookup"><span data-stu-id="2416e-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="2416e-134">Rufen Sie **ScRelocProps** vor dem Schreiben das Array und die Daten auf einem Datenträger, auf dem Array mit dem _PvBaseNew_ -Parameter für die Instanz auf einige Standardwert 0 (null), zeigen.</span><span class="sxs-lookup"><span data-stu-id="2416e-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="2416e-135">Nach dem Lesen der Array und Daten von einem Datenträger, rufen Sie **ScRelocProps** für das Array mit dem Parameter _PvBaseOld_ , der dem in Schritt 1 verwendeten standard Wert gleich ist.</span><span class="sxs-lookup"><span data-stu-id="2416e-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="2416e-136">Das Array und die Daten müssen in einen Puffer mit einer einzelnen Reservierung erstellt gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="2416e-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="2416e-137">Der Parameter _pcb_ **ScRelocProps** ist optional.</span><span class="sxs-lookup"><span data-stu-id="2416e-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2416e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2416e-138">See also</span></span>



[<span data-ttu-id="2416e-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2416e-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2416e-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="2416e-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="2416e-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="2416e-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="2416e-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="2416e-142">ScRelocNotifications</span></span>](screlocnotifications.md)

