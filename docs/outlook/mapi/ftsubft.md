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
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408418"
---
# <a name="ftsubft"></a><span data-ttu-id="e2693-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="e2693-103">FtSubFt</span></span>

  
  
<span data-ttu-id="e2693-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2693-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2693-105">Subtrahiert eine nicht signierte ganzzahlige 64-Bit-Zahl von einer anderen.</span><span class="sxs-lookup"><span data-stu-id="e2693-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2693-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e2693-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2693-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e2693-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e2693-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e2693-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2693-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2693-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2693-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e2693-110">Called by:</span></span>  <br/> |<span data-ttu-id="e2693-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e2693-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="e2693-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2693-112">Parameters</span></span>

 <span data-ttu-id="e2693-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="e2693-113">_Minuend_</span></span>
  
> <span data-ttu-id="e2693-114">[in] Eine [FILETIME-Struktur,](filetime.md) die die nicht signierte ganzzahlige 64-Bit-Zahl enthält, von der der Wert im  _Subtrahend-Parameter subtrahend subtrahiert_ werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2693-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="e2693-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="e2693-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="e2693-116">[in] Eine **FILETIME-Struktur,** die die nicht signierte ganzzahlige 64-Bit-Zahl enthält, die vom durch den  _Parameter Minuend angegebenen Wert subtrahiert_ wird.</span><span class="sxs-lookup"><span data-stu-id="e2693-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2693-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2693-117">Return value</span></span>

<span data-ttu-id="e2693-118">Die **FtSubFt-Funktion** gibt eine **FILETIME-Struktur** zurück, die das Ergebnis der Subtraktion enthält.</span><span class="sxs-lookup"><span data-stu-id="e2693-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="e2693-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="e2693-119">The two input parameters remain unchanged.</span></span> 
  

