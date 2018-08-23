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
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583274"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="6a98a-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="6a98a-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="6a98a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a98a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a98a-105">Ruft Informationen zu was ein Speicher unterstützt werden kann, basierend auf die angegebene Auswahl.</span><span class="sxs-lookup"><span data-stu-id="6a98a-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="6a98a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a98a-106">Parameters</span></span>

 <span data-ttu-id="6a98a-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="6a98a-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="6a98a-108">[in] Selektor, der angibt, welche Funktionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a98a-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a98a-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6a98a-109">Return value</span></span>

<span data-ttu-id="6a98a-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="6a98a-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="6a98a-111">Unterstützung für Homepages in einem Speicher nicht standardmäßigen Ordners.</span><span class="sxs-lookup"><span data-stu-id="6a98a-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="6a98a-112">Dies kann zurückgegeben werden, wenn **MSCAP_SEL_FOLDER** im *MscapSelector* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6a98a-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="6a98a-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="6a98a-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="6a98a-114">Wenn eine Einschränkung ungültige Argumente wie ungültige Eigenschaften enthält, der Informationsspeicher ignoriert die ungültige Argumente und verarbeitet nur die gültigen Argumente.</span><span class="sxs-lookup"><span data-stu-id="6a98a-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="6a98a-115">Dies kann zurückgegeben werden, wenn **MSCAP_SEL_RESTRICTION** im *MscapSelector* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6a98a-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="6a98a-116">NULL</span><span class="sxs-lookup"><span data-stu-id="6a98a-116">NULL</span></span>
  
> <span data-ttu-id="6a98a-117">Jede Funktion basierend auf dem angegebenen Selektor unterstützt der Speicher nicht.</span><span class="sxs-lookup"><span data-stu-id="6a98a-117">The store does not support any capability based on the given selector.</span></span>
    

