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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581979"
---
# <a name="scduppropset"></a><span data-ttu-id="185c1-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="185c1-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="185c1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="185c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="185c1-105">Array-Eigenschaft ein Wert in einem Block MAPI-Speicher die Vorgänge der Funktionen [ScCopyProps](sccopyprops.md) und [ScCountProps](sccountprops.md) kombinieren dupliziert.</span><span class="sxs-lookup"><span data-stu-id="185c1-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="185c1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="185c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="185c1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="185c1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="185c1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="185c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="185c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="185c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="185c1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="185c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="185c1-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="185c1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="185c1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="185c1-112">Parameters</span></span>

 <span data-ttu-id="185c1-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="185c1-113">_cprop_</span></span>
  
> <span data-ttu-id="185c1-114">[in] Anzahl der-Eigenschaftswerte im Array durch den Parameter _Rgprop_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="185c1-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="185c1-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="185c1-115">_rgprop_</span></span>
  
> <span data-ttu-id="185c1-116">[in] Zeiger auf ein Array von [SPropValue](spropvalue.md) Strukturen definieren die Eigenschaftswerte dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="185c1-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="185c1-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="185c1-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="185c1-118">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher für das duplizierte Array verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="185c1-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="185c1-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="185c1-119">_prgprop_</span></span>
  
> <span data-ttu-id="185c1-120">[out] Zeiger auf die Ausgangsposition im Arbeitsspeicher, in dem das duplizierte zurückgegebene Array von **SPropValue** -Strukturen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="185c1-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="185c1-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="185c1-121">Return value</span></span>

<span data-ttu-id="185c1-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="185c1-122">S_OK</span></span> 
  
> <span data-ttu-id="185c1-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="185c1-123">The call succeeded and has returned the expected value or values.</span></span>
    

