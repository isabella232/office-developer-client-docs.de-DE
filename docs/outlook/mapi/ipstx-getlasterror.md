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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592591"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="c467e-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c467e-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="c467e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c467e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c467e-105">Ruft Informationen über den letzten Fehler erweitert.</span><span class="sxs-lookup"><span data-stu-id="c467e-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="c467e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c467e-106">Parameters</span></span>

 <span data-ttu-id="c467e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c467e-107">_hResult_</span></span>
  
>  <span data-ttu-id="c467e-108">[in] Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c467e-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="c467e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c467e-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="c467e-110">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="c467e-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="c467e-111">Dies muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="c467e-111">This must be 0.</span></span> 
    
 <span data-ttu-id="c467e-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c467e-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="c467e-113">[out] Zeiger auf die **MAPIERROR** -Struktur, die erweiterte Informationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="c467e-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="c467e-114">Finden Sie unter mapidefs.h für die Definition des **LPMAPIERROR**Typs.</span><span class="sxs-lookup"><span data-stu-id="c467e-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c467e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c467e-115">See also</span></span>



[<span data-ttu-id="c467e-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="c467e-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="c467e-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="c467e-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

