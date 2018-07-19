---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791769"
---
# <a name="ftsubft"></a><span data-ttu-id="ee308-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="ee308-103">FtSubFt</span></span>

  
  
<span data-ttu-id="ee308-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee308-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee308-105">Eine 64-Bit-Ganzzahl von einem anderen subtrahiert.</span><span class="sxs-lookup"><span data-stu-id="ee308-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee308-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ee308-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee308-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ee308-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ee308-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ee308-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee308-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee308-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee308-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ee308-110">Called by:</span></span>  <br/> |<span data-ttu-id="ee308-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ee308-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="ee308-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee308-112">Parameters</span></span>

 <span data-ttu-id="ee308-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="ee308-113">_Minuend_</span></span>
  
> <span data-ttu-id="ee308-114">[in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen enthält, von der der Wert in der _Subtrahend_ -Parameter ist, subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee308-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="ee308-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="ee308-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="ee308-116">[in] Ein **FILETIME** -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen enthält, die von dem Wert, der durch den Parameter _Minuend_ subtrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee308-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee308-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee308-117">Return value</span></span>

<span data-ttu-id="ee308-118">Die **FtSubFt** -Funktion gibt eine **FILETIME** -Struktur, die das Ergebnis der Subtraktion enthält.</span><span class="sxs-lookup"><span data-stu-id="ee308-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="ee308-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="ee308-119">The two input parameters remain unchanged.</span></span> 
  

