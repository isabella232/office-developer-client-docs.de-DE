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
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414977"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="35515-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="35515-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="35515-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35515-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35515-105">Ruft erweiterte Informationen zum letzten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="35515-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="35515-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35515-106">Parameters</span></span>

 <span data-ttu-id="35515-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="35515-107">_hResult_</span></span>
  
>  <span data-ttu-id="35515-108">in Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="35515-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="35515-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35515-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="35515-110">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="35515-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="35515-111">Dies muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="35515-111">This must be 0.</span></span> 
    
 <span data-ttu-id="35515-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="35515-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="35515-113">Out Zeiger auf die **MAPIERROR** -Struktur, die die erweiterten Informationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="35515-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="35515-114">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="35515-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="35515-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35515-115">See also</span></span>



[<span data-ttu-id="35515-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="35515-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="35515-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="35515-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

