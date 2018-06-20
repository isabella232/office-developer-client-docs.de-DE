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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792609"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="f57d6-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="f57d6-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="f57d6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f57d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f57d6-105">Ruft Informationen zu was ein Speicher unterstützt werden kann, basierend auf die angegebene Auswahl.</span><span class="sxs-lookup"><span data-stu-id="f57d6-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="f57d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f57d6-106">Parameters</span></span>

 <span data-ttu-id="f57d6-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="f57d6-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="f57d6-108">[in] Selektor, der angibt, welche Funktionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f57d6-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f57d6-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f57d6-109">Return value</span></span>

<span data-ttu-id="f57d6-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="f57d6-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="f57d6-111">Unterstützung für Homepages in einem Speicher nicht standardmäßigen Ordners.</span><span class="sxs-lookup"><span data-stu-id="f57d6-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="f57d6-112">Dies kann zurückgegeben werden, wenn **MSCAP_SEL_FOLDER** im *MscapSelector* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f57d6-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="f57d6-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="f57d6-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="f57d6-114">Wenn eine Einschränkung ungültige Argumente wie ungültige Eigenschaften enthält, der Informationsspeicher ignoriert die ungültige Argumente und verarbeitet nur die gültigen Argumente.</span><span class="sxs-lookup"><span data-stu-id="f57d6-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="f57d6-115">Dies kann zurückgegeben werden, wenn **MSCAP_SEL_RESTRICTION** im *MscapSelector* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f57d6-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="f57d6-116">NULL</span><span class="sxs-lookup"><span data-stu-id="f57d6-116">NULL</span></span>
  
> <span data-ttu-id="f57d6-117">Jede Funktion basierend auf dem angegebenen Selektor unterstützt der Speicher nicht.</span><span class="sxs-lookup"><span data-stu-id="f57d6-117">The store does not support any capability based on the given selector.</span></span>
    

