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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578262"
---
# <a name="ftsubft"></a><span data-ttu-id="77473-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="77473-103">FtSubFt</span></span>

  
  
<span data-ttu-id="77473-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77473-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77473-105">Eine 64-Bit-Ganzzahl von einem anderen subtrahiert.</span><span class="sxs-lookup"><span data-stu-id="77473-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77473-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="77473-106">Header file:</span></span>  <br/> |<span data-ttu-id="77473-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="77473-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="77473-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="77473-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="77473-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="77473-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="77473-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="77473-110">Called by:</span></span>  <br/> |<span data-ttu-id="77473-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="77473-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="77473-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77473-112">Parameters</span></span>

 <span data-ttu-id="77473-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="77473-113">_Minuend_</span></span>
  
> <span data-ttu-id="77473-114">[in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen enthält, von der der Wert in der _Subtrahend_ -Parameter ist, subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="77473-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="77473-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="77473-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="77473-116">[in] Ein **FILETIME** -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen enthält, die von dem Wert, der durch den Parameter _Minuend_ subtrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="77473-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="77473-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="77473-117">Return value</span></span>

<span data-ttu-id="77473-118">Die **FtSubFt** -Funktion gibt eine **FILETIME** -Struktur, die das Ergebnis der Subtraktion enthält.</span><span class="sxs-lookup"><span data-stu-id="77473-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="77473-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="77473-119">The two input parameters remain unchanged.</span></span> 
  

