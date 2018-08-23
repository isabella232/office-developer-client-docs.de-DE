---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589238"
---
# <a name="ftnegft"></a><span data-ttu-id="c0ed6-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="c0ed6-103">FtNegFt</span></span>

  
  
<span data-ttu-id="c0ed6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0ed6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0ed6-105">Berechnet die beiden Komplement eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c0ed6-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0ed6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c0ed6-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0ed6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c0ed6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c0ed6-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c0ed6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0ed6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0ed6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0ed6-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c0ed6-110">Called by:</span></span>  <br/> |<span data-ttu-id="c0ed6-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c0ed6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="c0ed6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0ed6-112">Parameters</span></span>

 <span data-ttu-id="c0ed6-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="c0ed6-113">_ft_</span></span>
  
> <span data-ttu-id="c0ed6-114">[in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen für die die beiden Ergänzung berechnet enthält.</span><span class="sxs-lookup"><span data-stu-id="c0ed6-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0ed6-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c0ed6-115">Return value</span></span>

<span data-ttu-id="c0ed6-116">Die **FtNegFt** -Funktion gibt eine **FILETIME** -Struktur, die die beiden Ergänzung der ganzen Zahl enthält.</span><span class="sxs-lookup"><span data-stu-id="c0ed6-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="c0ed6-117">Der Eingabeparameter bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="c0ed6-117">The input parameter remains unchanged.</span></span> 
  

