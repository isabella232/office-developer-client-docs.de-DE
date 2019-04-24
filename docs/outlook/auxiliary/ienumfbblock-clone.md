---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Erstellt eine Kopie des Enumerators, wobei dieselbe Zeiteinschränkung verwendet wird, der Cursor jedoch auf den Anfang des Enumerators festgelegt wird.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317598"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="55c3e-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="55c3e-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="55c3e-104">Erstellt eine Kopie des Enumerators, wobei dieselbe Zeiteinschränkung verwendet wird, der Cursor jedoch auf den Anfang des Enumerators festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="55c3e-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="55c3e-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="55c3e-105">Quick info</span></span>

<span data-ttu-id="55c3e-106">Siehe [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="55c3e-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="55c3e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55c3e-107">Parameters</span></span>

<span data-ttu-id="55c3e-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="55c3e-108">_ppclone_</span></span>
  
> <span data-ttu-id="55c3e-109">Out Ein Zeiger auf die Kopie der [IEnumFBBlock](ienumfbblock.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="55c3e-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="55c3e-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="55c3e-110">Return values</span></span>

|<span data-ttu-id="55c3e-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="55c3e-111">**HRESULT**</span></span>|<span data-ttu-id="55c3e-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="55c3e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55c3e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="55c3e-113">S_OK</span></span>  <br/> |<span data-ttu-id="55c3e-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="55c3e-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="55c3e-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="55c3e-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="55c3e-116">Es ist nicht genügend Arbeitsspeicher für die Kopie vorhanden.</span><span class="sxs-lookup"><span data-stu-id="55c3e-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55c3e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c3e-117">See also</span></span>

- [<span data-ttu-id="55c3e-118">Konstanten (frei/gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="55c3e-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="55c3e-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="55c3e-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="55c3e-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="55c3e-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="55c3e-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="55c3e-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="55c3e-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="55c3e-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

