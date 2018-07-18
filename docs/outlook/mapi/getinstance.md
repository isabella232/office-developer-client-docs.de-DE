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
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791796"
---
# <a name="getinstance"></a><span data-ttu-id="ee7b6-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="ee7b6-103">GetInstance</span></span>

  
  
<span data-ttu-id="ee7b6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee7b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee7b6-105">Kopiert einen Wert innerhalb einer mehrwertigen Eigenschaft zu einer einwertige Eigenschaft des gleichen Typs.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee7b6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ee7b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee7b6-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="ee7b6-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="ee7b6-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ee7b6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee7b6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee7b6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee7b6-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ee7b6-110">Called by:</span></span>  <br/> |<span data-ttu-id="ee7b6-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ee7b6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="ee7b6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee7b6-112">Parameters</span></span>

 <span data-ttu-id="ee7b6-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="ee7b6-113">_pvalMv_</span></span>
  
> <span data-ttu-id="ee7b6-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die eine mehrwertige Eigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="ee7b6-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="ee7b6-115">_pvalSv_</span></span>
  
> <span data-ttu-id="ee7b6-116">[in] Zeiger auf eine einwertige Eigenschaft Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="ee7b6-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="ee7b6-117">_uliInst_</span></span>
  
> <span data-ttu-id="ee7b6-118">[in] Die Instanz an, die ist, das Arrayelement des Werts aus der Struktur, von der _PvalMv_ -Parameter angegebene kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee7b6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee7b6-119">Return value</span></span>

<span data-ttu-id="ee7b6-120">None.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee7b6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee7b6-121">Remarks</span></span>

<span data-ttu-id="ee7b6-122">Wenn der Wert für reservierter Speicher zu groß ist, kopiert die **GetInstance** -Funktion nur Zeiger, anstatt neue Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

