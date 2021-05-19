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
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421088"
---
# <a name="screlocprops"></a><span data-ttu-id="0a296-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="0a296-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="0a296-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a296-105">Passt die Zeiger in einem [SPropValue-Array](spropvalue.md) an, nachdem das Array und seine Daten kopiert oder an einen neuen Speicherort verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="0a296-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a296-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0a296-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a296-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a296-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0a296-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0a296-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0a296-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0a296-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0a296-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0a296-110">Called by:</span></span>  <br/> |<span data-ttu-id="0a296-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0a296-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="0a296-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a296-112">Parameters</span></span>

 <span data-ttu-id="0a296-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="0a296-113">_cprop_</span></span>
  
> <span data-ttu-id="0a296-114">[in] Anzahl der Eigenschaften im Array, auf die der  _rgprop-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="0a296-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0a296-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="0a296-115">_rgprop_</span></span>
  
> <span data-ttu-id="0a296-116">[in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) für die Zeiger angepasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0a296-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="0a296-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="0a296-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="0a296-118">[in] Zeiger auf die ursprüngliche Basisadresse des Arrays, auf das der  _rgprop-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="0a296-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0a296-119">_pvBaseNeu_</span><span class="sxs-lookup"><span data-stu-id="0a296-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="0a296-120">[in] Zeiger auf die neue Basisadresse des Arrays, auf das der  _rgprop-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="0a296-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0a296-121">_leiterplatte_</span><span class="sxs-lookup"><span data-stu-id="0a296-121">_pcb_</span></span>
  
> <span data-ttu-id="0a296-122">[in, out] Optionaler Zeiger auf die Größe des durch den  _parameter pvBaseNew_ angegebenen Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0a296-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="0a296-123">Wenn nicht NULL, wird der  _Parameter "pcb"_ auf die Anzahl der Bytes festgelegt, die im  _pvD-Parameter gespeichert_ sind.</span><span class="sxs-lookup"><span data-stu-id="0a296-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0a296-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a296-124">Return value</span></span>

<span data-ttu-id="0a296-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a296-125">S_OK</span></span>
  
> <span data-ttu-id="0a296-126">Zeiger wurden erfolgreich angepasst.</span><span class="sxs-lookup"><span data-stu-id="0a296-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="0a296-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0a296-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="0a296-128">Ein oder beide Parameter waren ungültig, oder es wurde ein unbekannter Eigenschaftstyp gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a296-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a296-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a296-129">Remarks</span></span>

<span data-ttu-id="0a296-130">Die **ScRelocProps-Funktion** arbeitet unter der Annahme, dass das Eigenschaftswertarray, für das Zeiger angepasst werden, ursprünglich in einem einzigen Aufruf zugeordnet wurde, der einem Aufruf der **ScCopyProps-Funktion** ähnelt.</span><span class="sxs-lookup"><span data-stu-id="0a296-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="0a296-131">Wenn eine Clientanwendung oder ein Dienstanbieter mit einem Eigenschaftswert arbeitet, der aus nicht gemeinsamen Speicherblöcken erstellt wird, sollte [scCopyProps](sccopyprops.md) zum Kopieren von Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a296-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="0a296-132">**ScRelocProps** wird verwendet, um die Gültigkeit von Zeigern in einem [SPropValue-Array zu](spropvalue.md) erhalten.</span><span class="sxs-lookup"><span data-stu-id="0a296-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="0a296-133">Führen Sie die folgenden Vorgänge aus, um die Gültigkeit von Zeigern beim Schreiben eines solchen Arrays auf einen Datenträger zu erhalten und es von einem Datenträger aus zu lesen:</span><span class="sxs-lookup"><span data-stu-id="0a296-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="0a296-134">Rufen Sie **scRelocProps** auf dem Array auf, bevor Sie das Array und die Daten auf einen Datenträger schreiben, z. B. mit dem  _pvBaseNew-Parameter,_ der auf einen Standardwert null verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="0a296-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="0a296-135">Nachdem Sie das Array und die Daten von einem Datenträger gelesen haben, rufen Sie **ScRelocProps** auf dem Array auf,  _deren pvBaseOld-Parameter_ dem gleichen Standardwert entspricht, der in Schritt 1 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a296-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="0a296-136">Das Array und die Daten müssen in einen Puffer gelesen werden, der mit einer einzigen Zuordnung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0a296-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="0a296-137">Der  _Parameter "pcb"_ für **ScRelocProps** ist optional.</span><span class="sxs-lookup"><span data-stu-id="0a296-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0a296-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a296-138">See also</span></span>



[<span data-ttu-id="0a296-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0a296-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0a296-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="0a296-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="0a296-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="0a296-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="0a296-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="0a296-142">ScRelocNotifications</span></span>](screlocnotifications.md)

