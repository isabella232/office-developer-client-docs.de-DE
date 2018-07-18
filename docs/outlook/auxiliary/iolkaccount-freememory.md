---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Durch die Schnittstelle IOlkAccount Arbeitsspeicher frei.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791031"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="73cdb-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="73cdb-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="73cdb-104">Durch die Schnittstelle [IOlkAccount](iolkaccount.md) Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="73cdb-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="73cdb-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="73cdb-105">Quick info</span></span>

<span data-ttu-id="73cdb-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="73cdb-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="73cdb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73cdb-107">Parameters</span></span>

<span data-ttu-id="73cdb-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="73cdb-108">_pv_</span></span>
  
> <span data-ttu-id="73cdb-109">[in] Ein Zeiger auf den Speicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73cdb-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="73cdb-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="73cdb-110">Return values</span></span>

<span data-ttu-id="73cdb-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="73cdb-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73cdb-112">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="73cdb-112">Remarks</span></span>

<span data-ttu-id="73cdb-113">Verwenden Sie diese Methode, um Arbeitsspeicher freizugeben, die von [IOlkAccount::GetProp](iolkaccount-getprop.md) (wenn der Wert der Eigenschaft angegebene Konto einen Typ Binär oder eine Zeichenfolge ist) und [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="73cdb-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="73cdb-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73cdb-114">See also</span></span>

- [<span data-ttu-id="73cdb-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="73cdb-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="73cdb-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="73cdb-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

