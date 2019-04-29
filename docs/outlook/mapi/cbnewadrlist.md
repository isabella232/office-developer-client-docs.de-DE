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
ms.openlocfilehash: 885cf53de45cfde4079cc2a0e7bfdca09f72b962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404316"
---
# <a name="cbnewadrlist"></a><span data-ttu-id="9b02f-103">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="9b02f-103">CbNewADRLIST</span></span>

  
  
<span data-ttu-id="9b02f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b02f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b02f-105">Berechnet die Anzahl der Bytes, die für eine neue [ADRLIST](adrlist.md) -Struktur reserviert werden sollen, die eine angegebene Anzahl von Empfängern enthält, die durch die [Miet](adrentry.md) Strukturen repräsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b02f-105">Computes the number of bytes that should be allocated for a new [ADRLIST](adrlist.md) structure that contains a specified number of recipients represented by [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b02f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9b02f-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b02f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9b02f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9b02f-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="9b02f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9b02f-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="9b02f-109">**ADRLIST**</span></span> <br/> |
   
```cpp
CbNewADRLIST (_centries)
```

## <a name="parameters"></a><span data-ttu-id="9b02f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b02f-110">Parameters</span></span>

 <span data-ttu-id="9b02f-111">__Zentrierungen_</span><span class="sxs-lookup"><span data-stu-id="9b02f-111">__centries_</span></span>
  
> <span data-ttu-id="9b02f-112">Die Anzahl der **Miet** Strukturen, die in die neue **ADRLIST** -Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b02f-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9b02f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b02f-113">See also</span></span>



[<span data-ttu-id="9b02f-114">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9b02f-114">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9b02f-115">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="9b02f-115">ADRENTRY</span></span>](adrentry.md)


[<span data-ttu-id="9b02f-116">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="9b02f-116">Macros Related to Structures</span></span>](macros-related-to-structures.md)

