---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Ruft das nächste Konto in den Enumerator ab.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791130"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="d6752-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="d6752-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="d6752-104">Ruft das nächste Konto in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="d6752-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d6752-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d6752-105">Quick info</span></span>

<span data-ttu-id="d6752-106">Finden Sie unter [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="d6752-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="d6752-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6752-107">Parameters</span></span>

<span data-ttu-id="d6752-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="d6752-108">_ppunk_</span></span>
  
> <span data-ttu-id="d6752-109">[in] Ein Zeiger auf eine **IUnknown** -Schnittstelle, die der Client Abfragen kann, um eine [IOlkAccount](iolkaccount.md) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6752-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d6752-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d6752-110">Return values</span></span>

|<span data-ttu-id="d6752-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="d6752-111">**HRESULT**</span></span>|<span data-ttu-id="d6752-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6752-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6752-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6752-113">S_OK</span></span>  <br/> |<span data-ttu-id="d6752-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d6752-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="d6752-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d6752-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="d6752-116">Das Ende wurde der Enumerator erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="d6752-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6752-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6752-117">Remarks</span></span>

<span data-ttu-id="d6752-118">Die angegebene *Ppunk* Schnittstelle erbt von **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="d6752-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="d6752-119">Der Client kann diese Schnittstelle (Verwendung von **QueryInterface**) Abfragen, um einen Zeiger auf eine Schnittstelle **IOlkAccount** erhalten und Abrufen oder Festlegen von Informationen für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="d6752-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6752-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6752-120">See also</span></span>

- [<span data-ttu-id="d6752-121">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="d6752-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="d6752-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="d6752-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="d6752-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="d6752-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="d6752-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="d6752-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

