---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Ruft das nächste Konto im Enumerator ab.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321896"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="7e9eb-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="7e9eb-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="7e9eb-104">Ruft das nächste Konto im Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="7e9eb-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7e9eb-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7e9eb-105">Quick info</span></span>

<span data-ttu-id="7e9eb-106">Siehe [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="7e9eb-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="7e9eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e9eb-107">Parameters</span></span>

<span data-ttu-id="7e9eb-108">_ppUnk_</span><span class="sxs-lookup"><span data-stu-id="7e9eb-108">_ppunk_</span></span>
  
> <span data-ttu-id="7e9eb-109">in Ein Zeiger auf eine **IUnknown** -Schnittstelle, die der Client Abfragen kann, um eine [IOlkAccount](iolkaccount.md) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e9eb-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7e9eb-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7e9eb-110">Return values</span></span>

|<span data-ttu-id="7e9eb-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7e9eb-111">**HRESULT**</span></span>|<span data-ttu-id="7e9eb-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e9eb-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e9eb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e9eb-113">S_OK</span></span>  <br/> |<span data-ttu-id="7e9eb-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7e9eb-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="7e9eb-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7e9eb-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="7e9eb-116">Der Enumerator hat das Ende erreicht.</span><span class="sxs-lookup"><span data-stu-id="7e9eb-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e9eb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e9eb-117">Remarks</span></span>

<span data-ttu-id="7e9eb-118">Die von *ppUnk* angegebene Schnittstelle erbt von **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="7e9eb-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="7e9eb-119">Der Client kann diese Schnittstelle Abfragen (mithilfe von **IUnknown:: QueryInterface**), um einen Zeiger auf eine **IOlkAccount** -Schnittstelle abzurufen und Informationen für dieses Konto abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7e9eb-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e9eb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e9eb-120">See also</span></span>

- [<span data-ttu-id="7e9eb-121">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="7e9eb-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="7e9eb-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="7e9eb-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="7e9eb-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="7e9eb-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="7e9eb-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="7e9eb-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

