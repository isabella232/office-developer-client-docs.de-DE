---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge ab, die Anbieterfunktionen beschreibt.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408103"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="57f97-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="57f97-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="57f97-104">Ruft eine Zeichenfolge ab, die Anbieterfunktionen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="57f97-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="57f97-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="57f97-105">Parameters</span></span>

<span data-ttu-id="57f97-106">_result_</span><span class="sxs-lookup"><span data-stu-id="57f97-106">_result_</span></span>
  
> <span data-ttu-id="57f97-107">[out] Eine XML-Zeichenfolge, die die Funktionen eines Outlook Social Connector (OSC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="57f97-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57f97-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57f97-108">Remarks</span></span>

<span data-ttu-id="57f97-109">Die zurückgegebene Ergebnis-XML-Zeichenfolge muss der Schemadefinition für das **Capabilities-Element** entsprechen, wie im XML-Schema für die Erweiterbarkeit des OSC-Anbieters definiert. </span><span class="sxs-lookup"><span data-stu-id="57f97-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="57f97-110">Der Anbieter muss eine  _Ergebniszeichenfolge zurückgeben,_ damit nachfolgende Aufrufe vom OSC an den Anbieter ordnungsgemäß ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="57f97-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57f97-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57f97-111">See also</span></span>

- [<span data-ttu-id="57f97-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57f97-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

