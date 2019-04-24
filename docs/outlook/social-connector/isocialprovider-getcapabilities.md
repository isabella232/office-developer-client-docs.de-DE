---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge ab, die die Anbieter Funktionen beschreibt.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285764"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="bc240-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="bc240-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="bc240-104">Ruft eine Zeichenfolge ab, die die Anbieter Funktionen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bc240-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="bc240-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc240-105">Parameters</span></span>

<span data-ttu-id="bc240-106">_result_</span><span class="sxs-lookup"><span data-stu-id="bc240-106">_result_</span></span>
  
> <span data-ttu-id="bc240-107">Out Eine XML-Zeichenfolge, die die Funktionen eines Outlook Social Connector (OSC)-Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc240-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc240-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc240-108">Remarks</span></span>

<span data-ttu-id="bc240-109">Die zurückgegebene _Ergebnis_ -XML-Zeichenfolge muss der Schema Definition für das **Capabilities** -Element entsprechen, wie im XML-Schema für osc-Anbieter Erweiterbarkeit definiert.</span><span class="sxs-lookup"><span data-stu-id="bc240-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="bc240-110">Der Anbieter muss eine _Ergebnis_ Zeichenfolge zurückgeben, damit nachfolgende Aufrufe vom osc an den Anbieter ordnungsgemäß ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="bc240-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc240-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc240-111">See also</span></span>

- [<span data-ttu-id="bc240-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc240-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

