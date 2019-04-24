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
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327972"
---
# <a name="ftnegft"></a><span data-ttu-id="15ccd-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="15ccd-103">FtNegFt</span></span>

  
  
<span data-ttu-id="15ccd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15ccd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15ccd-105">Berechnet die beiden Komplemente einer unsignierten 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="15ccd-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15ccd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="15ccd-106">Header file:</span></span>  <br/> |<span data-ttu-id="15ccd-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="15ccd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="15ccd-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="15ccd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="15ccd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="15ccd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="15ccd-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="15ccd-110">Called by:</span></span>  <br/> |<span data-ttu-id="15ccd-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="15ccd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="15ccd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="15ccd-112">Parameters</span></span>

 <span data-ttu-id="15ccd-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="15ccd-113">_ft_</span></span>
  
> <span data-ttu-id="15ccd-114">in Eine [FILETIME](filetime.md) -Struktur mit der unsignierten 64-Bit-Ganzzahl, für die die Komplemente der beiden berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15ccd-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15ccd-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15ccd-115">Return value</span></span>

<span data-ttu-id="15ccd-116">Die **FtNegFt** -Funktion gibt \*\*\*\* eine FILETIME-Struktur zurück, die die Komplemente der ganzen Zahl enthält.</span><span class="sxs-lookup"><span data-stu-id="15ccd-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="15ccd-117">Der Eingabeparameter bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="15ccd-117">The input parameter remains unchanged.</span></span> 
  

