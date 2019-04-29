---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Gibt von der IOlkAccount-Schnittstelle zugewiesene Arbeitsspeicher frei.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406199"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="a5340-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="a5340-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="a5340-104">Gibt von der [IOlkAccount](iolkaccount.md) -Schnittstelle zugewiesene Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="a5340-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a5340-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a5340-105">Quick info</span></span>

<span data-ttu-id="a5340-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a5340-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="a5340-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5340-107">Parameters</span></span>

<span data-ttu-id="a5340-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="a5340-108">_pv_</span></span>
  
> <span data-ttu-id="a5340-109">in Ein Zeiger auf den zu speichernden Speicher.</span><span class="sxs-lookup"><span data-stu-id="a5340-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a5340-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a5340-110">Return values</span></span>

<span data-ttu-id="a5340-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a5340-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5340-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5340-112">Remarks</span></span>

<span data-ttu-id="a5340-113">Verwenden Sie diese Methode, um den von [IOlkAccount:: getprop](iolkaccount-getprop.md) reservierten Arbeitsspeicher freizugeben (wenn der Wert der angegebenen Account-Eigenschaft ein binary-oder String-Typ ist) und [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a5340-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5340-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5340-114">See also</span></span>

- [<span data-ttu-id="a5340-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="a5340-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="a5340-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="a5340-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

