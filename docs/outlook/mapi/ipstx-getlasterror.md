---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792822"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="241e7-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="241e7-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="241e7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="241e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="241e7-105">Ruft Informationen über den letzten Fehler erweitert.</span><span class="sxs-lookup"><span data-stu-id="241e7-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="241e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="241e7-106">Parameters</span></span>

 <span data-ttu-id="241e7-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="241e7-107">_hResult_</span></span>
  
>  <span data-ttu-id="241e7-108">[in] Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="241e7-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="241e7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="241e7-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="241e7-110">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="241e7-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="241e7-111">Dies muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="241e7-111">This must be 0.</span></span> 
    
 <span data-ttu-id="241e7-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="241e7-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="241e7-113">[out] Zeiger auf die **MAPIERROR** -Struktur, die erweiterte Informationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="241e7-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="241e7-114">Finden Sie unter mapidefs.h für die Definition des **LPMAPIERROR**Typs.</span><span class="sxs-lookup"><span data-stu-id="241e7-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="241e7-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="241e7-115">See also</span></span>



[<span data-ttu-id="241e7-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="241e7-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="241e7-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="241e7-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

