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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791774"
---
# <a name="ftnegft"></a><span data-ttu-id="ca115-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="ca115-103">FtNegFt</span></span>

  
  
<span data-ttu-id="ca115-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca115-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca115-105">Berechnet die beiden Komplement eine 64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ca115-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca115-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ca115-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca115-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ca115-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ca115-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ca115-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca115-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ca115-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ca115-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ca115-110">Called by:</span></span>  <br/> |<span data-ttu-id="ca115-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ca115-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="ca115-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca115-112">Parameters</span></span>

 <span data-ttu-id="ca115-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="ca115-113">_ft_</span></span>
  
> <span data-ttu-id="ca115-114">[in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen für die die beiden Ergänzung berechnet enthält.</span><span class="sxs-lookup"><span data-stu-id="ca115-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca115-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ca115-115">Return value</span></span>

<span data-ttu-id="ca115-116">Die **FtNegFt** -Funktion gibt eine **FILETIME** -Struktur, die die beiden Ergänzung der ganzen Zahl enthält.</span><span class="sxs-lookup"><span data-stu-id="ca115-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="ca115-117">Der Eingabeparameter bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="ca115-117">The input parameter remains unchanged.</span></span> 
  

