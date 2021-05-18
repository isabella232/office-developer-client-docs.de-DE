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
# <a name="scduppropset"></a><span data-ttu-id="f342c-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="f342c-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="f342c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f342c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f342c-105">Dupliziert ein Eigenschaftswertarray in einem einzelnen Block MAPI-Speicher, der die Vorgänge der [Funktionen ScCopyProps](sccopyprops.md) und [ScCountProps](sccountprops.md) kombiniert.</span><span class="sxs-lookup"><span data-stu-id="f342c-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f342c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f342c-106">Header file:</span></span>  <br/> |<span data-ttu-id="f342c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f342c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f342c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f342c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f342c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f342c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f342c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f342c-110">Called by:</span></span>  <br/> |<span data-ttu-id="f342c-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f342c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="f342c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f342c-112">Parameters</span></span>

 <span data-ttu-id="f342c-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="f342c-113">_cprop_</span></span>
  
> <span data-ttu-id="f342c-114">[in] Anzahl der Eigenschaftswerte im Array, das durch den  _rgprop-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="f342c-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="f342c-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="f342c-115">_rgprop_</span></span>
  
> <span data-ttu-id="f342c-116">[in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die eigenschaftswerte definieren, die dupliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f342c-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="f342c-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f342c-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f342c-118">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher für das duplizierte Array verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f342c-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="f342c-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="f342c-119">_prgprop_</span></span>
  
> <span data-ttu-id="f342c-120">[out] Zeiger auf die Ausgangsposition im Arbeitsspeicher, an der das zurückgegebene duplizierte Array von **SPropValue-Strukturen** gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f342c-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f342c-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f342c-121">Return value</span></span>

<span data-ttu-id="f342c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f342c-122">S_OK</span></span> 
  
> <span data-ttu-id="f342c-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f342c-123">The call succeeded and has returned the expected value or values.</span></span>
    

