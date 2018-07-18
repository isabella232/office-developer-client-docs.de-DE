---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Erstellt eine Kopie der Enumerator, verwenden die gleichen zeitliche Beschränkung jedoch festlegen des Cursors an den Anfang des den Enumerator.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790951"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="07e7a-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="07e7a-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="07e7a-104">Erstellt eine Kopie der Enumerator, verwenden die gleichen zeitliche Beschränkung jedoch festlegen des Cursors an den Anfang des den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="07e7a-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="07e7a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="07e7a-105">Quick info</span></span>

<span data-ttu-id="07e7a-106">Finden Sie unter [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="07e7a-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="07e7a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="07e7a-107">Parameters</span></span>

<span data-ttu-id="07e7a-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="07e7a-108">_ppclone_</span></span>
  
> <span data-ttu-id="07e7a-109">[out] Ein Zeiger auf Zeiger auf die Kopie der [IEnumFBBlock](ienumfbblock.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="07e7a-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="07e7a-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="07e7a-110">Return values</span></span>

|<span data-ttu-id="07e7a-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="07e7a-111">**HRESULT**</span></span>|<span data-ttu-id="07e7a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07e7a-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07e7a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="07e7a-113">S_OK</span></span>  <br/> |<span data-ttu-id="07e7a-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="07e7a-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="07e7a-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="07e7a-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="07e7a-116">Es ist nicht genügend Speicherplatz für die Kopie.</span><span class="sxs-lookup"><span data-stu-id="07e7a-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07e7a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07e7a-117">See also</span></span>

- [<span data-ttu-id="07e7a-118">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="07e7a-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="07e7a-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="07e7a-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="07e7a-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="07e7a-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="07e7a-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="07e7a-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="07e7a-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="07e7a-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

