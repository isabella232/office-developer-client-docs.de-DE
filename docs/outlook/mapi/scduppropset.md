---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406017"
---
# <a name="scduppropset"></a><span data-ttu-id="98019-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="98019-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="98019-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98019-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98019-105">Dupliziert ein Eigenschafts Wertarray in einem einzelnen MAPI-Blockspeicher, der die Vorgänge der [ScCopyProps](sccopyprops.md) -und [ScCountProps](sccountprops.md) -Funktionen kombiniert.</span><span class="sxs-lookup"><span data-stu-id="98019-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98019-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="98019-106">Header file:</span></span>  <br/> |<span data-ttu-id="98019-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="98019-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="98019-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="98019-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98019-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98019-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98019-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="98019-110">Called by:</span></span>  <br/> |<span data-ttu-id="98019-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="98019-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="98019-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98019-112">Parameters</span></span>

 <span data-ttu-id="98019-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="98019-113">_cprop_</span></span>
  
> <span data-ttu-id="98019-114">in Die Anzahl der Eigenschaftswerte im durch den _rgprop_ -Parameter angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="98019-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="98019-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="98019-115">_rgprop_</span></span>
  
> <span data-ttu-id="98019-116">in Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaftswerte definieren, die dupliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98019-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="98019-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="98019-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="98019-118">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Zuweisen von Arbeitsspeicher für das duplizierte Array verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98019-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="98019-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="98019-119">_prgprop_</span></span>
  
> <span data-ttu-id="98019-120">Out Zeiger auf die Anfangsposition im Arbeitsspeicher, in der das zurückgegebene duplizierte Array von **SPropValue** -Strukturen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="98019-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98019-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98019-121">Return value</span></span>

<span data-ttu-id="98019-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="98019-122">S_OK</span></span> 
  
> <span data-ttu-id="98019-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="98019-123">The call succeeded and has returned the expected value or values.</span></span>
    

