---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429705"
---
# <a name="ftadcft"></a><span data-ttu-id="0fb44-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="0fb44-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="0fb44-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fb44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fb44-105">Fügt eine unsignierte 64-Bit-Ganzzahl zu einem anderen hinzu, optional mit einem Carry-Flag.</span><span class="sxs-lookup"><span data-stu-id="0fb44-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fb44-106">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0fb44-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="0fb44-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fb44-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="0fb44-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0fb44-108">Called by:</span></span>  <br/> |<span data-ttu-id="0fb44-109">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0fb44-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="0fb44-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fb44-110">Parameters</span></span>

 <span data-ttu-id="0fb44-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="0fb44-111">_ft1_</span></span>
  
> <span data-ttu-id="0fb44-112">in Eine [FILETIME](filetime.md) -Struktur, die die erste nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fb44-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="0fb44-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="0fb44-113">_ft2_</span></span>
  
> <span data-ttu-id="0fb44-114">in Eine fileTIME-Struktur, die die zweite nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fb44-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="0fb44-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="0fb44-115">_pwCarry_</span></span>
  
> <span data-ttu-id="0fb44-116">[in, out, optional] Bei Eingabe ein Zeiger auf die eingehende Carry-Kennzeichnung.</span><span class="sxs-lookup"><span data-stu-id="0fb44-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="0fb44-117">Bei Ausgabe ein Zeiger auf das Carry-Ergebnis für den Zusatz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="0fb44-118">Dieser Parameter kann NULL sein, wenn das Carry-Ergebnis nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0fb44-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0fb44-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fb44-119">Return value</span></span>

<span data-ttu-id="0fb44-120">Die **FtAdcFt** -Funktion gibt \*\*\*\* eine FILETIME-Struktur zurück, die die Summe der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="0fb44-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="0fb44-121">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="0fb44-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="0fb44-122">Wenn **pwCarry** ungleich NULL ist, enthält es das Carry-Ergebnis für die Summe, entweder 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="0fb44-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0fb44-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fb44-123">Remarks</span></span>

<span data-ttu-id="0fb44-124">Die **FtAdcFt** -Funktion ist identisch mit **FtAddFt** , wenn _pwCarry_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="0fb44-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="0fb44-125">Wenn _pwCarry_ nicht NULL ist und auf 0 zeigt, gibt **FtAdcFt** den gleichen **FILETIME** -Wert zurück, der **FtAddFt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0fb44-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0fb44-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb44-126">See also</span></span>



[<span data-ttu-id="0fb44-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="0fb44-127">FtAddFt</span></span>](ftaddft.md)

