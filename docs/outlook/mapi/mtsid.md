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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342770"
---
# <a name="mtsid"></a><span data-ttu-id="1cd30-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="1cd30-103">MTSID</span></span>

  
  
<span data-ttu-id="1cd30-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd30-105">Enthält eine MTS-Eintrags-ID (X. 400-Nachrichtentransportsystem).</span><span class="sxs-lookup"><span data-stu-id="1cd30-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1cd30-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1cd30-106">Header file:</span></span>  <br/> |<span data-ttu-id="1cd30-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1cd30-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1cd30-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="1cd30-108">Related macros:</span></span>  <br/> |<span data-ttu-id="1cd30-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="1cd30-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="1cd30-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="1cd30-110">Members</span></span>

 <span data-ttu-id="1cd30-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="1cd30-111">**cb**</span></span>
  
> <span data-ttu-id="1cd30-112">Die Anzahl der Bytes im vom **abEntry** -Element beschriebenen Array.</span><span class="sxs-lookup"><span data-stu-id="1cd30-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="1cd30-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="1cd30-113">**abEntry**</span></span>
  
> <span data-ttu-id="1cd30-114">Bytearray, das die MTS-Eintrags-ID-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="1cd30-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cd30-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cd30-115">Remarks</span></span>

<span data-ttu-id="1cd30-116">Die **MTSID** -Struktur wird nur für X. 400-ZUORDNUNGEN von MAPI-Eintrags Bezeichnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cd30-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="1cd30-117">Es entspricht der MAPI- [FLATENTRY](flatentry.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1cd30-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="1cd30-118">Ein MTS-Bezeichner hat das gleiche Format wie eine MAPI-Eintrags-ID oder einen binären Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="1cd30-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="1cd30-119">MTS-IDs können besonders nützlich sein, wenn verzögerte Nachrichten abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="1cd30-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1cd30-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cd30-120">See also</span></span>



[<span data-ttu-id="1cd30-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="1cd30-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="1cd30-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="1cd30-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="1cd30-123">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1cd30-123">MAPI Structures</span></span>](mapi-structures.md)

