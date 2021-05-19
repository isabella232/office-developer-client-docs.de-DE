---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435173"
---
# <a name="mtsid"></a><span data-ttu-id="de0ed-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="de0ed-103">MTSID</span></span>

  
  
<span data-ttu-id="de0ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de0ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de0ed-105">Enthält eine X.400 Message Transport System (MTS)-Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="de0ed-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de0ed-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="de0ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="de0ed-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de0ed-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="de0ed-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="de0ed-108">Related macros:</span></span>  <br/> |<span data-ttu-id="de0ed-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="de0ed-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="de0ed-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="de0ed-110">Members</span></span>

 <span data-ttu-id="de0ed-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="de0ed-111">**cb**</span></span>
  
> <span data-ttu-id="de0ed-112">Anzahl der Bytes im array, das vom **abEntry-Element beschrieben** wird.</span><span class="sxs-lookup"><span data-stu-id="de0ed-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="de0ed-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="de0ed-113">**abEntry**</span></span>
  
> <span data-ttu-id="de0ed-114">Bytearray, das die MTS-Eintrags-ID-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="de0ed-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de0ed-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de0ed-115">Remarks</span></span>

<span data-ttu-id="de0ed-116">Die **MTSID-Struktur** wird nur für X.400-Zuordnungen von MAPI-Eintragsbezeichnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="de0ed-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="de0ed-117">Sie entspricht der MAPI [FLATENTRY-Struktur.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="de0ed-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="de0ed-118">Ein MTS-Bezeichner hat das gleiche Format wie ein MAPI-Eintragsbezeichner oder ein binärer Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="de0ed-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="de0ed-119">MTS-Bezeichner können besonders nützlich sein, um verzögerte Nachrichten abgesagt zu haben.</span><span class="sxs-lookup"><span data-stu-id="de0ed-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de0ed-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de0ed-120">See also</span></span>



[<span data-ttu-id="de0ed-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="de0ed-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="de0ed-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="de0ed-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="de0ed-123">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="de0ed-123">MAPI Structures</span></span>](mapi-structures.md)

