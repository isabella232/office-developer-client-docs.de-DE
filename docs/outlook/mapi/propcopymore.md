---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328553"
---
# <a name="propcopymore"></a><span data-ttu-id="3790f-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="3790f-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="3790f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3790f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3790f-105">Kopiert einen einzelnen Eigenschaftswert von einem Quellspeicherort an einen Zielspeicherort.</span><span class="sxs-lookup"><span data-stu-id="3790f-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3790f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3790f-106">Header file:</span></span>  <br/> |<span data-ttu-id="3790f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="3790f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3790f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3790f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3790f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3790f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3790f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3790f-110">Called by:</span></span>  <br/> |<span data-ttu-id="3790f-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3790f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="3790f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3790f-112">Parameters</span></span>

 <span data-ttu-id="3790f-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="3790f-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="3790f-114">Out Zeiger auf den Speicherort, an den diese Funktion eine [SPropValue](spropvalue.md) -Struktur schreibt, die den kopierten Eigenschaftswert definiert.</span><span class="sxs-lookup"><span data-stu-id="3790f-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="3790f-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="3790f-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="3790f-116">in Zeiger auf die [SPropValue](spropvalue.md) -Struktur, die den zu kopierenden Eigenschaftswert enthält.</span><span class="sxs-lookup"><span data-stu-id="3790f-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="3790f-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="3790f-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="3790f-118">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll, wenn der Zielspeicherort nicht groß genug ist, um die zu kopierende Eigenschaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3790f-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="3790f-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="3790f-119">_lpvObject_</span></span>
  
> <span data-ttu-id="3790f-120">in Zeiger auf ein Objekt, für das **MAPIAllocateMore** ggf. Platz reserviert.</span><span class="sxs-lookup"><span data-stu-id="3790f-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3790f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3790f-121">Return value</span></span>

<span data-ttu-id="3790f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="3790f-122">S_OK</span></span>
  
> <span data-ttu-id="3790f-123">Der einzelne Eigenschaftswert wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="3790f-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="3790f-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3790f-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="3790f-125">Ein unbekannter Eigenschafts wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3790f-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3790f-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3790f-126">Remarks</span></span>

<span data-ttu-id="3790f-127">Eine Clientanwendung oder ein Dienstanbieter kann die **PropCopyMore** -Funktion verwenden, um eine Eigenschaft aus einer Tabelle zu kopieren, die freigegeben werden soll, um Sie an anderer Stelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3790f-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="3790f-128">**PropCopyMore** muss keinen Arbeitsspeicher zuweisen, es sei denn, der kopierte Eigenschaftswert ist ein Typ, wie beispielsweise PT_STRING8, der nicht in eine [SPropValue](spropvalue.md) -Struktur passt.</span><span class="sxs-lookup"><span data-stu-id="3790f-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="3790f-129">Bei diesen hohen Eigenschaften weist die Funktion Speicher mithilfe der [MAPIAllocateMore](mapiallocatemore.md) -Funktion zu, an die ein Zeiger im _lpfAllocMore_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3790f-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="3790f-130">Unüberlegte Verwendung von **PropCopyMore** -Fragmenten Verwenden Sie stattdessen die [ScCopyProps](sccopyprops.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3790f-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

