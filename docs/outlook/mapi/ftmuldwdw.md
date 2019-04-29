---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412912"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="7a85a-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="7a85a-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="7a85a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a85a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a85a-105">Multipliziert eine unsignierte 32-Bit-Ganzzahl mit einer anderen.</span><span class="sxs-lookup"><span data-stu-id="7a85a-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a85a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7a85a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a85a-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="7a85a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7a85a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7a85a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7a85a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7a85a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7a85a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7a85a-110">Called by:</span></span>  <br/> |<span data-ttu-id="7a85a-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7a85a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="7a85a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a85a-112">Parameters</span></span>

 <span data-ttu-id="7a85a-113">_Multiplikand_</span><span class="sxs-lookup"><span data-stu-id="7a85a-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="7a85a-114">in Ein Doppelwort, das die nicht signierte 32-Bit-Ganzzahl enthält, die mit dem Wert im _Multiplikatorparameter_ multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a85a-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="7a85a-115">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="7a85a-115">_Multiplier_</span></span>
  
> <span data-ttu-id="7a85a-116">in Ein Doppelwort, das den unsignierten ganzzahligen Multiplikations Wert 32-Bit enthält.</span><span class="sxs-lookup"><span data-stu-id="7a85a-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a85a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a85a-117">Return value</span></span>

<span data-ttu-id="7a85a-118">Die **FtMulDwDw** -Funktion gibt [](filetime.md) eine FILETIME-Struktur zurück, die das Produkt der beiden ganzen Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="7a85a-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="7a85a-119">Die beiden Eingabeparameter bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="7a85a-119">The two input parameters remain unchanged.</span></span> 
  

