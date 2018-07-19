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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795595"
---
# <a name="smapiverbarray"></a><span data-ttu-id="b3f74-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="b3f74-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="b3f74-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3f74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3f74-105">Enthält ein Array von [SMAPIVerb](smapiverb.md) -Strukturen, die MAPI-Verben beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b3f74-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f74-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b3f74-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3f74-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b3f74-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b3f74-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="b3f74-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b3f74-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="b3f74-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="b3f74-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="b3f74-110">Members</span></span>

 <span data-ttu-id="b3f74-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="b3f74-111">**cForms**</span></span>
  
> <span data-ttu-id="b3f74-112">Anzahl der Verben im Array.</span><span class="sxs-lookup"><span data-stu-id="b3f74-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="b3f74-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="b3f74-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="b3f74-114">Array von MAPI-Verben.</span><span class="sxs-lookup"><span data-stu-id="b3f74-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3f74-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3f74-115">Remarks</span></span>

<span data-ttu-id="b3f74-116">Die Struktur **SMAPIVerbArray** wird als Parameter in der [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3f74-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3f74-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3f74-117">See also</span></span>



[<span data-ttu-id="b3f74-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="b3f74-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="b3f74-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b3f74-119">MAPI Structures</span></span>](mapi-structures.md)

