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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299545"
---
# <a name="getinstance"></a><span data-ttu-id="7f9d9-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="7f9d9-103">GetInstance</span></span>

  
  
<span data-ttu-id="7f9d9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f9d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f9d9-105">Kopiert einen Wert in einer mehrwertigen Eigenschaft in eine einwertige Eigenschaft desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="7f9d9-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f9d9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7f9d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f9d9-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="7f9d9-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="7f9d9-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7f9d9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7f9d9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7f9d9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7f9d9-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7f9d9-110">Called by:</span></span>  <br/> |<span data-ttu-id="7f9d9-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7f9d9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="7f9d9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f9d9-112">Parameters</span></span>

 <span data-ttu-id="7f9d9-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="7f9d9-113">_pvalMv_</span></span>
  
> <span data-ttu-id="7f9d9-114">in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die eine mehrwertige Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="7f9d9-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="7f9d9-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="7f9d9-115">_pvalSv_</span></span>
  
> <span data-ttu-id="7f9d9-116">in Zeiger auf eine einwertige Eigenschaft zum Empfangen von Daten.</span><span class="sxs-lookup"><span data-stu-id="7f9d9-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="7f9d9-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="7f9d9-117">_uliInst_</span></span>
  
> <span data-ttu-id="7f9d9-118">in Die Instanznummer, also das Arrayelement, des Werts, der aus der vom _pvalMv_ -Parameter angegebenen Struktur kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="7f9d9-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7f9d9-119">Return value</span><span class="sxs-lookup"><span data-stu-id="7f9d9-119">Return value</span></span>

<span data-ttu-id="7f9d9-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f9d9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f9d9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f9d9-121">Remarks</span></span>

<span data-ttu-id="7f9d9-122">Wenn der kopierte Wert für den zugewiesenen Speicher zu umfangreich \*\*\*\* ist, kopiert die GetInstance-Funktion nur Zeiger, anstatt neuen Speicher zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f9d9-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

