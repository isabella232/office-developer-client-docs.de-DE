---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409258"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="40c5a-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="40c5a-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="40c5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40c5a-105">Ruft Informationen darüber ab, was ein Informationsspeicher basierend auf der angegebenen Auswahl unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="40c5a-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="40c5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40c5a-106">Parameters</span></span>

 <span data-ttu-id="40c5a-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="40c5a-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="40c5a-108">in Selector, der angibt, welche Funktionen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40c5a-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40c5a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40c5a-109">Return value</span></span>

<span data-ttu-id="40c5a-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="40c5a-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="40c5a-111">Unterstützung für Ordner-Homepages in einem nicht standardmäßigen Speicher.</span><span class="sxs-lookup"><span data-stu-id="40c5a-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="40c5a-112">Dies kann zurückgegeben werden, wenn **MSCAP_SEL_FOLDER** in *mscapSelector* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="40c5a-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="40c5a-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="40c5a-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="40c5a-114">Wenn eine Einschränkung ungültige Argumente wie ungültige Eigenschaften enthält, ignoriert der Speicher die ungültigen Argumente und verarbeitet nur die gültigen Argumente.</span><span class="sxs-lookup"><span data-stu-id="40c5a-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="40c5a-115">Dies kann zurückgegeben werden, wenn **MSCAP_SEL_RESTRICTION** in *mscapSelector* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="40c5a-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="40c5a-116">NULL</span><span class="sxs-lookup"><span data-stu-id="40c5a-116">NULL</span></span>
  
> <span data-ttu-id="40c5a-117">Der Informationsspeicher unterstützt keine Funktionen basierend auf der angegebenen Auswahl.</span><span class="sxs-lookup"><span data-stu-id="40c5a-117">The store does not support any capability based on the given selector.</span></span>
    

