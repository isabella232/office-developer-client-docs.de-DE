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
# <a name="ftsubft"></a><span data-ttu-id="13b4b-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="13b4b-103">FtSubFt</span></span>

  
  
<span data-ttu-id="13b4b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b4b-105">Subtrahiert eine unsignierte 64-Bit-Ganzzahl von einem anderen.</span><span class="sxs-lookup"><span data-stu-id="13b4b-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13b4b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="13b4b-106">Header file:</span></span>  <br/> |<span data-ttu-id="13b4b-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="13b4b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="13b4b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="13b4b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="13b4b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="13b4b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="13b4b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="13b4b-110">Called by:</span></span>  <br/> |<span data-ttu-id="13b4b-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="13b4b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="13b4b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13b4b-112">Parameters</span></span>

 <span data-ttu-id="13b4b-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="13b4b-113">_Minuend_</span></span>
  
> <span data-ttu-id="13b4b-114">in Eine [FILETIME](filetime.md) -Struktur, die die unsignierte 64-Bit-Ganzzahl enthält, aus der der Wert im _Subtrahend_ -Parameter subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="13b4b-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="13b4b-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="13b4b-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="13b4b-116">in Eine **FILETIME** -Struktur mit der unsignierten 64-Bit-Ganzzahl, die von dem vom _Minuend_ -Parameter angegebenen Wert subtrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="13b4b-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="13b4b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13b4b-117">Return value</span></span>

<span data-ttu-id="13b4b-118">Die **FtSubFt** -Funktion gibt \*\*\*\* eine FILETIME-Struktur zurück, die das Ergebnis der Subtraktion enthält.</span><span class="sxs-lookup"><span data-stu-id="13b4b-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="13b4b-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="13b4b-119">The two input parameters remain unchanged.</span></span> 
  

