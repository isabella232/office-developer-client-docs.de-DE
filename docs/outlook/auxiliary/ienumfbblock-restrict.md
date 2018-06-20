---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Legt eine Beschränkung auf die Enumeration, die einen angegebenen Zeitraum.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790948"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="0e6bf-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="0e6bf-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="0e6bf-104">Legt eine Beschränkung auf die Enumeration, die einen angegebenen Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0e6bf-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="0e6bf-105">Quick info</span></span>

<span data-ttu-id="0e6bf-106">Finden Sie unter [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="0e6bf-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="0e6bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e6bf-107">Parameters</span></span>

<span data-ttu-id="0e6bf-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="0e6bf-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="0e6bf-109">[in] Die Anfangszeit die Enumeration einschränken.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="0e6bf-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="0e6bf-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="0e6bf-111">[in] Die Endzeit die Enumeration einschränken.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0e6bf-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0e6bf-112">Return values</span></span>

<span data-ttu-id="0e6bf-113">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e6bf-114">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="0e6bf-114">Remarks</span></span>

<span data-ttu-id="0e6bf-115">Diese Methode wird auch die-Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e6bf-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e6bf-116">See also</span></span>

- [<span data-ttu-id="0e6bf-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="0e6bf-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="0e6bf-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="0e6bf-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="0e6bf-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="0e6bf-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="0e6bf-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="0e6bf-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="0e6bf-121">Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="0e6bf-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

