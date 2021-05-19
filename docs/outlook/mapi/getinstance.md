---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418722"
---
# <a name="getinstance"></a><span data-ttu-id="ddc29-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="ddc29-103">GetInstance</span></span>

  
  
<span data-ttu-id="ddc29-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddc29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddc29-105">Kopiert einen Wert innerhalb einer mehrwertigen Eigenschaft in eine einwertige Eigenschaft desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="ddc29-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddc29-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ddc29-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddc29-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="ddc29-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="ddc29-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ddc29-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddc29-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ddc29-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ddc29-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ddc29-110">Called by:</span></span>  <br/> |<span data-ttu-id="ddc29-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ddc29-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="ddc29-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddc29-112">Parameters</span></span>

 <span data-ttu-id="ddc29-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="ddc29-113">_pvalMv_</span></span>
  
> <span data-ttu-id="ddc29-114">[in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die eine mehrwertige Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="ddc29-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="ddc29-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="ddc29-115">_pvalSv_</span></span>
  
> <span data-ttu-id="ddc29-116">[in] Zeiger auf eine einwertiger Eigenschaft zum Empfangen von Daten.</span><span class="sxs-lookup"><span data-stu-id="ddc29-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="ddc29-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="ddc29-117">_uliInst_</span></span>
  
> <span data-ttu-id="ddc29-118">[in] Die Instanznummer, d. h. das Arrayelement, des Werts, der aus der durch den  _pvalMv-Parameter_ angegebenen Struktur kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="ddc29-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ddc29-119">Return value</span><span class="sxs-lookup"><span data-stu-id="ddc29-119">Return value</span></span>

<span data-ttu-id="ddc29-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="ddc29-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddc29-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ddc29-121">Remarks</span></span>

<span data-ttu-id="ddc29-122">Wenn der kopierte Wert für den zugewiesenen Arbeitsspeicher zu groß ist, kopiert die **GetInstance-Funktion** nur Zeiger, anstatt neuen Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ddc29-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

