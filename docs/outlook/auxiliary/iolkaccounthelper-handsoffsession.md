---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Gibt das MAPI-Sitzung-Objekt, das von IOlkAccountHelper::GetMapiSession zurückgegeben wurde.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791081"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="66a9c-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="66a9c-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="66a9c-104">Gibt das MAPI-Sitzung-Objekt, das von - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="66a9c-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="66a9c-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="66a9c-105">Quick info</span></span>

<span data-ttu-id="66a9c-106">Finden Sie unter [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="66a9c-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="66a9c-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="66a9c-107">Return values</span></span>

|<span data-ttu-id="66a9c-108">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="66a9c-108">**HRESULT**</span></span>|<span data-ttu-id="66a9c-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66a9c-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66a9c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="66a9c-110">S_OK</span></span>  <br/> |<span data-ttu-id="66a9c-111">Wenn die Implementierung von **IOlkAccountHelper** eigene MAPI-Sitzung, die in **IOlkAccountHelper::GetMapiSession**zurückgegeben wird erstellt, müssen Sie hier die Sitzung freigeben und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="66a9c-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="66a9c-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="66a9c-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="66a9c-113">Wenn die Implementierung von **IOlkAccountHelper** eigene MAPI-Sitzung nicht selbst erstellt haben, müssen Sie nur E_NOTIMPL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="66a9c-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="66a9c-114">In diesem Fall ist dies der einzige unterstützte Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="66a9c-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66a9c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66a9c-115">See also</span></span>

- [<span data-ttu-id="66a9c-116">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="66a9c-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="66a9c-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="66a9c-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

