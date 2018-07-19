---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791759"
---
# <a name="ftmuldw"></a><span data-ttu-id="e63a7-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="e63a7-103">FtMulDw</span></span>

  
  
<span data-ttu-id="e63a7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e63a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e63a7-105">64-Bit-Ganzzahl ohne Vorzeichen durch eine 32-Bit-Ganzzahl ohne Vorzeichen multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e63a7-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e63a7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e63a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="e63a7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e63a7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e63a7-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e63a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e63a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e63a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e63a7-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e63a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="e63a7-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e63a7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="e63a7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e63a7-112">Parameters</span></span>

 <span data-ttu-id="e63a7-113">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="e63a7-113">_Multiplier_</span></span>
  
> <span data-ttu-id="e63a7-114">[in] Ein Wort, Double-Wert, der den 32-Bit-Ganzzahl ohne Vorzeichen Multiplikator enthält.</span><span class="sxs-lookup"><span data-stu-id="e63a7-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="e63a7-115">_Multiplikand_</span><span class="sxs-lookup"><span data-stu-id="e63a7-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="e63a7-116">[in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen, mit dem im Parameter _Multiplikator_ multipliziert werden enthält.</span><span class="sxs-lookup"><span data-stu-id="e63a7-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e63a7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e63a7-117">Return value</span></span>

<span data-ttu-id="e63a7-118">Die **FtMulDw** -Funktion gibt eine **FILETIME** -Struktur, die das Produkt von zwei Ganzzahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="e63a7-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="e63a7-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="e63a7-119">The two input parameters remain unchanged.</span></span> 
  

