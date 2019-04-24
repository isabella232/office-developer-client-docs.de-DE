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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360690"
---
# <a name="screlocprops"></a><span data-ttu-id="1d104-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="1d104-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="1d104-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d104-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d104-105">Passt die Zeiger in einem [SPropValue](spropvalue.md) -Array an, nachdem das Array und seine Daten kopiert oder an einen neuen Speicherort verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="1d104-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d104-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1d104-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d104-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1d104-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1d104-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1d104-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1d104-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1d104-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1d104-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1d104-110">Called by:</span></span>  <br/> |<span data-ttu-id="1d104-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1d104-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="1d104-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d104-112">Parameters</span></span>

 <span data-ttu-id="1d104-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="1d104-113">_cprop_</span></span>
  
> <span data-ttu-id="1d104-114">in Die Anzahl der Eigenschaften im Array, auf die durch den _rgprop_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1d104-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1d104-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="1d104-115">_rgprop_</span></span>
  
> <span data-ttu-id="1d104-116">in Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, für die Zeiger angepasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d104-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="1d104-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="1d104-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="1d104-118">in Zeiger auf die ursprüngliche Basisadresse des Arrays, auf das durch den _rgprop_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1d104-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1d104-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="1d104-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="1d104-120">in Zeiger auf die neue Basisadresse des Arrays, auf das durch den _rgprop_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1d104-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1d104-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="1d104-121">_pcb_</span></span>
  
> <span data-ttu-id="1d104-122">[in, out] Optionaler Zeiger auf die Größe des vom _pvBaseNew_ -Parameter angegebenen Arrays in Byte.</span><span class="sxs-lookup"><span data-stu-id="1d104-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="1d104-123">Wenn dies nicht der Fall ist, wird der _PCB_ -Parameter auf die im _PVD_ -Parameter gespeicherte Anzahl von Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1d104-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d104-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d104-124">Return value</span></span>

<span data-ttu-id="1d104-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d104-125">S_OK</span></span>
  
> <span data-ttu-id="1d104-126">Zeiger wurden erfolgreich angepasst.</span><span class="sxs-lookup"><span data-stu-id="1d104-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="1d104-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1d104-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="1d104-128">Ein oder beide Parameter waren ungültig, oder es wurde ein unbekannter Eigenschaftentyp gefunden.</span><span class="sxs-lookup"><span data-stu-id="1d104-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d104-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d104-129">Remarks</span></span>

<span data-ttu-id="1d104-130">Die **ScRelocProps** -Funktion wird davon ausgegangen, dass das Eigenschafts Wertarray, für das Zeiger angepasst wurden, ursprünglich in einem einzelnen Aufruf zugeordnet wurde, der einem Aufruf der **ScCopyProps** -Funktion ähnelt.</span><span class="sxs-lookup"><span data-stu-id="1d104-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="1d104-131">Wenn eine Clientanwendung oder ein Dienstanbieter mit einem Eigenschaftswert arbeitet, der aus nicht zusammengestellten Speicherblöcken erstellt wurde, sollte er [ScCopyProps](sccopyprops.md) verwenden, um stattdessen Eigenschaften zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1d104-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="1d104-132">**ScRelocProps** wird verwendet, um die Gültigkeit von Zeigern in einem [SPropValue](spropvalue.md) -Array zu behalten.</span><span class="sxs-lookup"><span data-stu-id="1d104-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="1d104-133">Führen Sie die folgenden Schritte aus, um die Gültigkeit von Zeiger beim Schreiben eines solchen Arrays in und von einem Datenträger zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="1d104-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="1d104-134">Bevor Sie das Array und die Daten auf einen Datenträger schreiben, rufen Sie **ScRelocProps** auf dem Array mit dem _pvBaseNew_ -Parameter auf, der auf einen Standardwert 0 (null) zeigt.</span><span class="sxs-lookup"><span data-stu-id="1d104-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="1d104-135">Nachdem Sie das Array und die Daten von einem Datenträger gelesen haben, rufen Sie **ScRelocProps** im Array mit dem Parameter _pvBaseOld_ auf, der dem gleichen Standardwert entspricht, der in Schritt 1 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d104-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="1d104-136">Das Array und die Daten müssen in einen mit einer einzelnen Zuordnung erstellten Puffer eingelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1d104-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="1d104-137">Der _PCB_ -Parameter für **ScRelocProps** ist optional.</span><span class="sxs-lookup"><span data-stu-id="1d104-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1d104-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d104-138">See also</span></span>



[<span data-ttu-id="1d104-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1d104-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1d104-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="1d104-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="1d104-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="1d104-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="1d104-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="1d104-142">ScRelocNotifications</span></span>](screlocnotifications.md)

