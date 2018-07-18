---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Ruft die Anzahl der nächste angegebene Blöcke mit Frei/Gebucht-Daten in eine Enumeration.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790957"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="b07cd-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="b07cd-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="b07cd-104">Ruft die Anzahl der nächste angegebene Blöcke mit Frei/Gebucht-Daten in eine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b07cd-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b07cd-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b07cd-105">Quick info</span></span>

<span data-ttu-id="b07cd-106">Finden Sie unter [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="b07cd-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="b07cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b07cd-107">Parameters</span></span>

<span data-ttu-id="b07cd-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="b07cd-108">_celt_</span></span>
  
> <span data-ttu-id="b07cd-109">[in] Die Anzahl der Frei/Gebucht-Daten Bausteine in *Pblk* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b07cd-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="b07cd-110">_PBLK_</span><span class="sxs-lookup"><span data-stu-id="b07cd-110">_pblk_</span></span>
  
> <span data-ttu-id="b07cd-111">[in] Ein Zeiger auf ein Array von Frei/Gebucht-Blöcke.</span><span class="sxs-lookup"><span data-stu-id="b07cd-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="b07cd-112">Das Array ist eine Größe von *Celt* zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b07cd-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="b07cd-113">Die angeforderte Blöcke Frei/Gebucht-Informationen werden in diesem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b07cd-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="b07cd-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="b07cd-114">_pcfetch_</span></span>
  
> <span data-ttu-id="b07cd-115">[out] Die Anzahl der Frei/Gebucht-Blöcke, die tatsächlich in *Pblk* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b07cd-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b07cd-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b07cd-116">Return values</span></span>

|<span data-ttu-id="b07cd-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b07cd-117">**HRESULT**</span></span>|<span data-ttu-id="b07cd-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b07cd-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b07cd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b07cd-119">S_OK</span></span>  <br/> |<span data-ttu-id="b07cd-120">Die angeforderte Anzahl Blöcke wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b07cd-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="b07cd-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b07cd-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="b07cd-122">Die angeforderte Anzahl Blöcke wurde nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b07cd-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b07cd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b07cd-123">See also</span></span>

- [<span data-ttu-id="b07cd-124">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="b07cd-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="b07cd-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="b07cd-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="b07cd-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="b07cd-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="b07cd-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="b07cd-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="b07cd-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="b07cd-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="b07cd-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="b07cd-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

