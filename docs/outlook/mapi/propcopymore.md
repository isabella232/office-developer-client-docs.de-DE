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
ms.openlocfilehash: 635525a1c2c3234d724534d225eb07022afc9956
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592122"
---
# <a name="propcopymore"></a><span data-ttu-id="6615f-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="6615f-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="6615f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6615f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6615f-105">Kopiert einen einzelnen Eigenschaftswert von einem Quellspeicherort in einen Zielspeicherort.</span><span class="sxs-lookup"><span data-stu-id="6615f-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6615f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6615f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6615f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6615f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6615f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6615f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6615f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6615f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6615f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6615f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6615f-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6615f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="6615f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6615f-112">Parameters</span></span>

 <span data-ttu-id="6615f-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="6615f-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="6615f-114">[out] Zeiger auf den Speicherort, zu dem diese Funktion eine [SPropValue](spropvalue.md) -Struktur definieren den kopierten Eigenschaftswert schreibt.</span><span class="sxs-lookup"><span data-stu-id="6615f-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="6615f-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="6615f-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="6615f-116">[in] Zeiger auf die [SPropValue](spropvalue.md) -Struktur, die Wert der Eigenschaft kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6615f-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="6615f-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="6615f-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="6615f-118">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die verwendet werden, um zusätzliche Speicher ist Zielspeicherort nicht groß genug für die Eigenschaft kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6615f-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="6615f-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="6615f-119">_lpvObject_</span></span>
  
> <span data-ttu-id="6615f-120">[in] Zeiger auf ein Objekt für die **MAPIAllocateMore** Speicherplatz bei Bedarf reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6615f-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6615f-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6615f-121">Return value</span></span>

<span data-ttu-id="6615f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6615f-122">S_OK</span></span>
  
> <span data-ttu-id="6615f-123">Die einzelnen Eigenschaftswert wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="6615f-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="6615f-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6615f-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="6615f-125">Unbekannte Eigenschaft vom Typ aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6615f-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6615f-126">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6615f-126">Remarks</span></span>

<span data-ttu-id="6615f-127">Eine Clientanwendung oder Dienstanbieter kann die Funktion **PropCopyMore** verwenden, um eine Eigenschaft aus einer Tabelle zu kopieren, der freigegeben werden, damit er an anderer Stelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="6615f-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="6615f-128">**PropCopyMore** muss kein Speicher zugewiesen werden, wenn der Wert der Eigenschaft kopiert eines Typs, beispielsweise PT_STRING8, ist, die nicht in einer Struktur [SPropValue](spropvalue.md) passen.</span><span class="sxs-lookup"><span data-stu-id="6615f-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="6615f-129">Für diese Eigenschaften großen weist die Funktion Speicher, die mithilfe der [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die ein Zeiger in der _LpfAllocMore_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6615f-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="6615f-130">Injudicious Verwendung von **PropCopyMore** Fragmente Speicher; Erwägen Sie die [ScCopyProps](sccopyprops.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6615f-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

