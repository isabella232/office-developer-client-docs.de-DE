---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791766"
---
# <a name="ftaddft"></a><span data-ttu-id="f945f-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="f945f-103">FtAddFt</span></span>

  
  
<span data-ttu-id="f945f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f945f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f945f-105">Fügt einer 64-Bit-Ganzzahl ohne Vorzeichen in eine andere.</span><span class="sxs-lookup"><span data-stu-id="f945f-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f945f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f945f-106">Header file:</span></span>  <br/> |<span data-ttu-id="f945f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f945f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f945f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f945f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f945f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f945f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f945f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f945f-110">Called by:</span></span>  <br/> |<span data-ttu-id="f945f-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f945f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="f945f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f945f-112">Parameters</span></span>

 <span data-ttu-id="f945f-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="f945f-113">_Addend1_</span></span>
  
> <span data-ttu-id="f945f-114">[in] Ein [FILETIME](filetime.md) -Struktur, die enthält die erste 64-Bit-Ganzzahl hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f945f-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="f945f-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="f945f-115">_Addend2_</span></span>
  
> <span data-ttu-id="f945f-116">[in] Ein **FILETIME** -Struktur, die enthält die zweite 64-Bit-Ganzzahl hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f945f-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f945f-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f945f-117">Return value</span></span>

<span data-ttu-id="f945f-118">Die **FtAddFt** -Funktion gibt eine **FILETIME** -Struktur, die die Summe der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="f945f-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="f945f-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="f945f-119">The two input parameters remain unchanged.</span></span> 
  

