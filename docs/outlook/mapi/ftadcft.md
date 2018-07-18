---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791761"
---
# <a name="ftadcft"></a><span data-ttu-id="500d5-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="500d5-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="500d5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="500d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="500d5-105">Fügt einer 64-Bit-Ganzzahl ohne Vorzeichen in eine andere, optional mit einem Flag ausführen.</span><span class="sxs-lookup"><span data-stu-id="500d5-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="500d5-106">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="500d5-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="500d5-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="500d5-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="500d5-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="500d5-108">Called by:</span></span>  <br/> |<span data-ttu-id="500d5-109">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="500d5-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="500d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="500d5-110">Parameters</span></span>

 <span data-ttu-id="500d5-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="500d5-111">_ft1_</span></span>
  
> <span data-ttu-id="500d5-112">[in] Ein [FILETIME](filetime.md) -Struktur, die enthält die erste 64-Bit-Ganzzahl hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="500d5-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="500d5-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="500d5-113">_ft2_</span></span>
  
> <span data-ttu-id="500d5-114">[in] Ein FILETIME-Struktur, die enthält die zweite 64-Bit-Ganzzahl hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="500d5-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="500d5-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="500d5-115">_pwCarry_</span></span>
  
> <span data-ttu-id="500d5-116">[eingehend, ausgehend, optional] Führen bei der Eingabe ein Zeiger auf die eingehenden Kennzeichnung.</span><span class="sxs-lookup"><span data-stu-id="500d5-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="500d5-117">Bei der Ausgabe einen Zeiger auf das Ergebnis sind für das Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="500d5-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="500d5-118">Dieser Parameter kann NULL sein, wenn das Ergebnis sind nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="500d5-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="500d5-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="500d5-119">Return value</span></span>

<span data-ttu-id="500d5-120">Die **FtAdcFt** -Funktion gibt eine **FILETIME** -Struktur, die die Summe der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="500d5-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="500d5-121">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="500d5-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="500d5-122">Wenn **PwCarry** ungleich NULL ist, werden für die Summe das Ergebnis ausführen enthält 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="500d5-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="500d5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="500d5-123">Remarks</span></span>

<span data-ttu-id="500d5-124">Die **FtAdcFt** -Funktion ist identisch mit **FtAddFt** , wenn _PwCarry_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="500d5-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="500d5-125">Wenn _PwCarry_ nicht NULL ist, und zeigt auf 0, **FtAdcFt** gibt den gleichen **FILETIME** -Wert, den **FtAddFt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="500d5-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="500d5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="500d5-126">See also</span></span>



[<span data-ttu-id="500d5-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="500d5-127">FtAddFt</span></span>](ftaddft.md)

