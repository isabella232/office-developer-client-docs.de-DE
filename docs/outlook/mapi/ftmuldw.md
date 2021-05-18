---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406346"
---
# <a name="ftmuldw"></a><span data-ttu-id="c5793-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="c5793-103">FtMulDw</span></span>

  
  
<span data-ttu-id="c5793-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5793-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5793-105">Multipliziert eine nicht signierte ganzzahlige 64-Bit-Zahl mit einer nicht signierten 32-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="c5793-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5793-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c5793-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5793-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c5793-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c5793-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c5793-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c5793-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5793-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c5793-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c5793-110">Called by:</span></span>  <br/> |<span data-ttu-id="c5793-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c5793-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="c5793-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5793-112">Parameters</span></span>

 <span data-ttu-id="c5793-113">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="c5793-113">_Multiplier_</span></span>
  
> <span data-ttu-id="c5793-114">[in] Ein Doppelwort, das den nicht signierten 32-Bit-Ganzzahlmultiplikator enthält.</span><span class="sxs-lookup"><span data-stu-id="c5793-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="c5793-115">_Multiplikation_</span><span class="sxs-lookup"><span data-stu-id="c5793-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="c5793-116">[in] Eine [FILETIME-Struktur,](filetime.md) die die nicht signierte ganzzahlige 64-Bit-Zahl enthält, die mit dem Wert im  _Multiplikatorparameter multipliziert werden_ soll.</span><span class="sxs-lookup"><span data-stu-id="c5793-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c5793-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5793-117">Return value</span></span>

<span data-ttu-id="c5793-118">Die **FtMulDw-Funktion** gibt eine **FILETIME-Struktur** zurück, die das Produkt der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="c5793-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="c5793-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="c5793-119">The two input parameters remain unchanged.</span></span> 
  

