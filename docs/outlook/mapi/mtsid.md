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
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585682"
---
# <a name="mtsid"></a><span data-ttu-id="4fab7-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="4fab7-103">MTSID</span></span>

  
  
<span data-ttu-id="4fab7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fab7-105">Enthält einen Eintrag Bezeichner für x. 400-Nachricht Transport System (MTS).</span><span class="sxs-lookup"><span data-stu-id="4fab7-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fab7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4fab7-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fab7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fab7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4fab7-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="4fab7-108">Related macros:</span></span>  <br/> |<span data-ttu-id="4fab7-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="4fab7-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="4fab7-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="4fab7-110">Members</span></span>

 <span data-ttu-id="4fab7-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="4fab7-111">**cb**</span></span>
  
> <span data-ttu-id="4fab7-112">Anzahl der Bytes im Array vom **AbEntry** Member beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4fab7-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="4fab7-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="4fab7-113">**abEntry**</span></span>
  
> <span data-ttu-id="4fab7-114">Byte-Array, das MTS Eintrags-ID-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="4fab7-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fab7-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4fab7-115">Remarks</span></span>

<span data-ttu-id="4fab7-116">Die Struktur **MTSID** wird nur für x. 400-Zuordnungen der MAPI-Eintragsbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fab7-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="4fab7-117">Es entspricht der MAPI- [FLATENTRY](flatentry.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fab7-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="4fab7-118">Ein Bezeichner MTS hat das gleiche Format wie ein MAPI-Eintrags-ID oder eine binäre Eigenschaft-Wert.</span><span class="sxs-lookup"><span data-stu-id="4fab7-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="4fab7-119">MTS-IDs können für das Abbrechen Zurückgestellte Nachrichten besonders nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="4fab7-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fab7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fab7-120">See also</span></span>



[<span data-ttu-id="4fab7-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="4fab7-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="4fab7-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="4fab7-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="4fab7-123">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4fab7-123">MAPI Structures</span></span>](mapi-structures.md)

