---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Öffnet eine MAPI-Sitzung, und behält einen Verweis auf die Sitzung für den Kontomanager.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392601"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="d30a0-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="d30a0-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="d30a0-104">Öffnet eine MAPI-Sitzung, und behält einen Verweis auf die Sitzung für den Kontomanager.</span><span class="sxs-lookup"><span data-stu-id="d30a0-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d30a0-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d30a0-105">Quick info</span></span>

<span data-ttu-id="d30a0-106">Finden Sie unter [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="d30a0-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="d30a0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d30a0-107">Parameters</span></span>

<span data-ttu-id="d30a0-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="d30a0-108">_ppmsess_</span></span>
  
> <span data-ttu-id="d30a0-109">[out] Der aktuellen MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d30a0-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d30a0-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d30a0-110">Return values</span></span>

<span data-ttu-id="d30a0-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d30a0-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d30a0-112">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="d30a0-112">Remarks</span></span>

<span data-ttu-id="d30a0-113">Aufgrund von Problemen in Zirkelverweis kann nicht selbst Konto-Manager den Verweis für die MAPI-Sitzung verwalten.</span><span class="sxs-lookup"><span data-stu-id="d30a0-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d30a0-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d30a0-114">See also</span></span>

- [<span data-ttu-id="d30a0-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="d30a0-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="d30a0-116">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d30a0-116">IMAPISession : IUnknown</span></span>](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

