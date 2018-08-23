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
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583995"
---
# <a name="ftmuldw"></a><span data-ttu-id="1cf0a-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="1cf0a-103">FtMulDw</span></span>

  
  
<span data-ttu-id="1cf0a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cf0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cf0a-105">64-Bit-Ganzzahl ohne Vorzeichen durch eine 32-Bit-Ganzzahl ohne Vorzeichen multipliziert.</span><span class="sxs-lookup"><span data-stu-id="1cf0a-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cf0a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1cf0a-106">Header file:</span></span>  <br/> |<span data-ttu-id="1cf0a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1cf0a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1cf0a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1cf0a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1cf0a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1cf0a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1cf0a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1cf0a-110">Called by:</span></span>  <br/> |<span data-ttu-id="1cf0a-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1cf0a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="1cf0a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cf0a-112">Parameters</span></span>

 <span data-ttu-id="1cf0a-113">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="1cf0a-113">_Multiplier_</span></span>
  
> <span data-ttu-id="1cf0a-114">[in] Ein Wort, Double-Wert, der den 32-Bit-Ganzzahl ohne Vorzeichen Multiplikator enthält.</span><span class="sxs-lookup"><span data-stu-id="1cf0a-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="1cf0a-115">_Multiplikand_</span><span class="sxs-lookup"><span data-stu-id="1cf0a-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="1cf0a-116">[in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen, mit dem im Parameter _Multiplikator_ multipliziert werden enthält.</span><span class="sxs-lookup"><span data-stu-id="1cf0a-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1cf0a-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1cf0a-117">Return value</span></span>

<span data-ttu-id="1cf0a-118">Die **FtMulDw** -Funktion gibt eine **FILETIME** -Struktur, die das Produkt von zwei Ganzzahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="1cf0a-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="1cf0a-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="1cf0a-119">The two input parameters remain unchanged.</span></span> 
  

