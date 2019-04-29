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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404470"
---
# <a name="propcopymore"></a><span data-ttu-id="1f1d1-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="1f1d1-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="1f1d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f1d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f1d1-105">Kopiert einen einzelnen Eigenschaftswert von einem Quellspeicherort an einen Zielspeicherort.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f1d1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1f1d1-106">Header file:</span></span>  <br/> |<span data-ttu-id="1f1d1-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="1f1d1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1f1d1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1f1d1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1f1d1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1f1d1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1f1d1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1f1d1-110">Called by:</span></span>  <br/> |<span data-ttu-id="1f1d1-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1f1d1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="1f1d1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f1d1-112">Parameters</span></span>

 <span data-ttu-id="1f1d1-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="1f1d1-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="1f1d1-114">Out Zeiger auf den Speicherort, an den diese Funktion eine [SPropValue](spropvalue.md) -Struktur schreibt, die den kopierten Eigenschaftswert definiert.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="1f1d1-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="1f1d1-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="1f1d1-116">in Zeiger auf die [SPropValue](spropvalue.md) -Struktur, die den zu kopierenden Eigenschaftswert enthält.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="1f1d1-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="1f1d1-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="1f1d1-118">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll, wenn der Zielspeicherort nicht groß genug ist, um die zu kopierende Eigenschaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="1f1d1-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="1f1d1-119">_lpvObject_</span></span>
  
> <span data-ttu-id="1f1d1-120">in Zeiger auf ein Objekt, für das **MAPIAllocateMore** ggf. Platz reserviert.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f1d1-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f1d1-121">Return value</span></span>

<span data-ttu-id="1f1d1-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f1d1-122">S_OK</span></span>
  
> <span data-ttu-id="1f1d1-123">Der einzelne Eigenschaftswert wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="1f1d1-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f1d1-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="1f1d1-125">Ein unbekannter Eigenschafts wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f1d1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f1d1-126">Remarks</span></span>

<span data-ttu-id="1f1d1-127">Eine Clientanwendung oder ein Dienstanbieter kann die **PropCopyMore** -Funktion verwenden, um eine Eigenschaft aus einer Tabelle zu kopieren, die freigegeben werden soll, um Sie an anderer Stelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="1f1d1-128">**PropCopyMore** muss keinen Arbeitsspeicher zuweisen, es sei denn, der kopierte Eigenschaftswert ist ein Typ, wie beispielsweise PT_STRING8, der nicht in eine [SPropValue](spropvalue.md) -Struktur passt.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="1f1d1-129">Bei diesen hohen Eigenschaften weist die Funktion Speicher mithilfe der [MAPIAllocateMore](mapiallocatemore.md) -Funktion zu, an die ein Zeiger im _lpfAllocMore_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="1f1d1-130">Unüberlegte Verwendung von **PropCopyMore** -Fragmenten Verwenden Sie stattdessen die [ScCopyProps](sccopyprops.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1f1d1-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

