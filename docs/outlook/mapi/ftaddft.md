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
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328007"
---
# <a name="ftaddft"></a><span data-ttu-id="0a8aa-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="0a8aa-103">FtAddFt</span></span>

  
  
<span data-ttu-id="0a8aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a8aa-105">Fügt eine unsignierte 64-Bit-Ganzzahl zu einem anderen hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a8aa-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a8aa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0a8aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a8aa-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0a8aa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0a8aa-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0a8aa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0a8aa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0a8aa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0a8aa-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0a8aa-110">Called by:</span></span>  <br/> |<span data-ttu-id="0a8aa-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0a8aa-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="0a8aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a8aa-112">Parameters</span></span>

 <span data-ttu-id="0a8aa-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="0a8aa-113">_Addend1_</span></span>
  
> <span data-ttu-id="0a8aa-114">in Eine [FILETIME](filetime.md) -Struktur, die die erste nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a8aa-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="0a8aa-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="0a8aa-115">_Addend2_</span></span>
  
> <span data-ttu-id="0a8aa-116">in Eine **FILETIME** -Struktur, die die zweite nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a8aa-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0a8aa-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a8aa-117">Return value</span></span>

<span data-ttu-id="0a8aa-118">Die **FtAddFt** -Funktion gibt \*\*\*\* eine FILETIME-Struktur zurück, die die Summe der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="0a8aa-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="0a8aa-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="0a8aa-119">The two input parameters remain unchanged.</span></span> 
  

