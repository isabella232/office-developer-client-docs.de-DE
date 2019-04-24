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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328000"
---
# <a name="ftmuldw"></a><span data-ttu-id="74f54-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="74f54-103">FtMulDw</span></span>

  
  
<span data-ttu-id="74f54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74f54-105">Multipliziert eine unsignierte 64-Bit-Ganzzahl durch eine unsignierte 32-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="74f54-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74f54-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="74f54-106">Header file:</span></span>  <br/> |<span data-ttu-id="74f54-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="74f54-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="74f54-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="74f54-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="74f54-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="74f54-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="74f54-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="74f54-110">Called by:</span></span>  <br/> |<span data-ttu-id="74f54-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="74f54-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="74f54-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f54-112">Parameters</span></span>

 <span data-ttu-id="74f54-113">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="74f54-113">_Multiplier_</span></span>
  
> <span data-ttu-id="74f54-114">in Ein Doppelwort, das den unsignierten ganzzahligen Multiplikations Wert 32-Bit enthält.</span><span class="sxs-lookup"><span data-stu-id="74f54-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="74f54-115">_Multiplikand_</span><span class="sxs-lookup"><span data-stu-id="74f54-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="74f54-116">in Eine [FILETIME](filetime.md) -Struktur, die die nicht signierte 64-Bit-Ganzzahl enthält, die mit dem Wert __ im Multiplikatorparameter multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74f54-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="74f54-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74f54-117">Return value</span></span>

<span data-ttu-id="74f54-118">Die **FtMulDw** -Funktion gibt \*\*\*\* eine FILETIME-Struktur zurück, die das Produkt der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="74f54-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="74f54-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="74f54-119">The two input parameters remain unchanged.</span></span> 
  

