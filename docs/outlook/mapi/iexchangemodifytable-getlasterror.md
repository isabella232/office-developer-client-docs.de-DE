---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792060"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="6f485-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6f485-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="6f485-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f485-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f485-105">Gibt Informationen zu den letzten aufgetretenen Fehler in einem Table-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6f485-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="6f485-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f485-106">Parameters</span></span>

 <span data-ttu-id="6f485-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="6f485-107">_hResult_</span></span>
  
> <span data-ttu-id="6f485-108">[in] Der Rückgabewert von der Methode, die nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6f485-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="6f485-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f485-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6f485-110">[in] Nicht verwendet, auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f485-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="6f485-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="6f485-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6f485-112">[out] Verweist auf eine MAPI- [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für ein Table-Objekt aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6f485-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6f485-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f485-113">See also</span></span>



[<span data-ttu-id="6f485-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f485-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="6f485-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6f485-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="6f485-116">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6f485-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

