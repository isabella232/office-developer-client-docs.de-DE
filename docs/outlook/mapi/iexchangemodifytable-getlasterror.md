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
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424511"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="e326c-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e326c-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="e326c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e326c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e326c-105">Gibt Informationen zum letzten Fehler zurück, der in einem Tabellenobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e326c-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="e326c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e326c-106">Parameters</span></span>

 <span data-ttu-id="e326c-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="e326c-107">_hResult_</span></span>
  
> <span data-ttu-id="e326c-108">[in] Der Rückgabewert der methode, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e326c-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="e326c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e326c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e326c-110">[in] Nicht verwendet, auf 0 (Null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e326c-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="e326c-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="e326c-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e326c-112">[out] Zeigt auf eine [MAPI MAPIERROR-Struktur,](mapierror.md) die Informationen zum letzten Fehler enthält, der für ein Tabellenobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e326c-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e326c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e326c-113">See also</span></span>



[<span data-ttu-id="e326c-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e326c-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="e326c-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e326c-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="e326c-116">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e326c-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

