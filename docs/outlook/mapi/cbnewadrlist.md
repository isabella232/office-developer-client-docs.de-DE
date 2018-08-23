---
title: CbNewADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CbNewADRLIST
api_type:
- COM
ms.assetid: 9ec1bbaa-7707-4239-9994-21ad1116430b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 898876863223aefa868fd37deced2948bd5a5694
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569750"
---
# <a name="cbnewadrlist"></a><span data-ttu-id="e4a8b-103">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="e4a8b-103">CbNewADRLIST</span></span>

  
  
<span data-ttu-id="e4a8b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4a8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4a8b-105">Berechnet die Anzahl von Bytes, die für eine neue [ADRLIST](adrlist.md) -Struktur, die eine angegebene Anzahl von Empfängern, dargestellt durch [ADRENTRY](adrentry.md) Strukturen enthält zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-105">Computes the number of bytes that should be allocated for a new [ADRLIST](adrlist.md) structure that contains a specified number of recipients represented by [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4a8b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e4a8b-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4a8b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4a8b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e4a8b-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="e4a8b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e4a8b-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="e4a8b-109">**ADRLIST**</span></span> <br/> |
   
```cpp
CbNewADRLIST (_centries)
```

## <a name="parameters"></a><span data-ttu-id="e4a8b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4a8b-110">Parameters</span></span>

 <span data-ttu-id="e4a8b-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="e4a8b-111">__centries_</span></span>
  
> <span data-ttu-id="e4a8b-112">Anzahl der **ADRENTRY** Strukturen, die in der neuen **ADRLIST** -Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e4a8b-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4a8b-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4a8b-113">See also</span></span>



[<span data-ttu-id="e4a8b-114">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e4a8b-114">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="e4a8b-115">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="e4a8b-115">ADRENTRY</span></span>](adrentry.md)


[<span data-ttu-id="e4a8b-116">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="e4a8b-116">Macros Related to Structures</span></span>](macros-related-to-structures.md)

