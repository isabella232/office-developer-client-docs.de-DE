---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Schränkt die Enumeration auf einen bestimmten Zeitraum ein.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431946"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="73e54-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="73e54-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="73e54-104">Schränkt die Enumeration auf einen bestimmten Zeitraum ein.</span><span class="sxs-lookup"><span data-stu-id="73e54-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="73e54-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="73e54-105">Quick info</span></span>

<span data-ttu-id="73e54-106">Siehe [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="73e54-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="73e54-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73e54-107">Parameters</span></span>

<span data-ttu-id="73e54-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="73e54-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="73e54-109">in Die Startzeit, um die Enumeration einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="73e54-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="73e54-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="73e54-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="73e54-111">in Die Endzeit, um die Enumeration einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="73e54-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="73e54-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="73e54-112">Return values</span></span>

<span data-ttu-id="73e54-113">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="73e54-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73e54-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73e54-114">Remarks</span></span>

<span data-ttu-id="73e54-115">Diese Methode setzt auch die Enumeration zurück.</span><span class="sxs-lookup"><span data-stu-id="73e54-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="73e54-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73e54-116">See also</span></span>

- [<span data-ttu-id="73e54-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="73e54-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="73e54-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="73e54-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="73e54-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="73e54-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="73e54-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="73e54-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="73e54-121">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="73e54-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

