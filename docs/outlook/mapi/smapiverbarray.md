---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433913"
---
# <a name="smapiverbarray"></a><span data-ttu-id="61b95-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="61b95-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="61b95-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61b95-105">Enthält ein Array von [SMAPIVerb-Strukturen,](smapiverb.md) die MAPI-Verben beschreiben.</span><span class="sxs-lookup"><span data-stu-id="61b95-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61b95-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="61b95-106">Header file:</span></span>  <br/> |<span data-ttu-id="61b95-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="61b95-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="61b95-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="61b95-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="61b95-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="61b95-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="61b95-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="61b95-110">Members</span></span>

 <span data-ttu-id="61b95-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="61b95-111">**cForms**</span></span>
  
> <span data-ttu-id="61b95-112">Anzahl der Verben im Array.</span><span class="sxs-lookup"><span data-stu-id="61b95-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="61b95-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="61b95-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="61b95-114">Array von MAPI-Verben.</span><span class="sxs-lookup"><span data-stu-id="61b95-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61b95-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61b95-115">Remarks</span></span>

<span data-ttu-id="61b95-116">Die **SMAPIVerbArray-Struktur** wird als Parameter in der [IMAPIFormInfo::CalcVerbSet-Methode](imapiforminfo-calcverbset.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="61b95-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61b95-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61b95-117">See also</span></span>



[<span data-ttu-id="61b95-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="61b95-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="61b95-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="61b95-119">MAPI Structures</span></span>](mapi-structures.md)

