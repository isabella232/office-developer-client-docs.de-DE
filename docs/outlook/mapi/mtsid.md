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
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793288"
---
# <a name="mtsid"></a><span data-ttu-id="0278a-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="0278a-103">MTSID</span></span>

  
  
<span data-ttu-id="0278a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0278a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0278a-105">Enthält einen Eintrag Bezeichner für x. 400-Nachricht Transport System (MTS).</span><span class="sxs-lookup"><span data-stu-id="0278a-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0278a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0278a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0278a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0278a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0278a-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="0278a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="0278a-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="0278a-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="0278a-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="0278a-110">Members</span></span>

 <span data-ttu-id="0278a-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="0278a-111">**cb**</span></span>
  
> <span data-ttu-id="0278a-112">Anzahl der Bytes im Array vom **AbEntry** Member beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0278a-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="0278a-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="0278a-113">**abEntry**</span></span>
  
> <span data-ttu-id="0278a-114">Byte-Array, das MTS Eintrags-ID-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0278a-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0278a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0278a-115">Remarks</span></span>

<span data-ttu-id="0278a-116">Die Struktur **MTSID** wird nur für x. 400-Zuordnungen der MAPI-Eintragsbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="0278a-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="0278a-117">Es entspricht der MAPI- [FLATENTRY](flatentry.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0278a-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="0278a-118">Ein Bezeichner MTS hat das gleiche Format wie ein MAPI-Eintrags-ID oder eine binäre Eigenschaft-Wert.</span><span class="sxs-lookup"><span data-stu-id="0278a-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="0278a-119">MTS-IDs können für das Abbrechen Zurückgestellte Nachrichten besonders nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="0278a-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0278a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0278a-120">See also</span></span>



[<span data-ttu-id="0278a-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="0278a-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="0278a-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="0278a-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="0278a-123">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0278a-123">MAPI Structures</span></span>](mapi-structures.md)

