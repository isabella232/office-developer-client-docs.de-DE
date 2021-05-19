---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434830"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="3f3a5-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="3f3a5-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="3f3a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f3a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f3a5-105">Überprüft ein Array von Strukturen, die benannte Eigenschaften beschreiben, und überprüft deren Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f3a5-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="3f3a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f3a5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="3f3a5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="3f3a5-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3f3a5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f3a5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f3a5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f3a5-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3f3a5-110">Called by:</span></span>  <br/> |<span data-ttu-id="3f3a5-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3f3a5-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="3f3a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f3a5-112">Parameters</span></span>

 <span data-ttu-id="3f3a5-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="3f3a5-113">_lppNameId_</span></span>
  
> <span data-ttu-id="3f3a5-114">[in] Zeiger auf ein Array von [MAPINAMEID-Strukturen,](mapinameid.md) die die benannten Eigenschaften beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="3f3a5-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="3f3a5-115">_cNames_</span></span>
  
> <span data-ttu-id="3f3a5-116">[in] Anzahl der benannten Eigenschaftenstrukturen im Array, auf die der  _lppNameId-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f3a5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f3a5-117">Return value</span></span>

<span data-ttu-id="3f3a5-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="3f3a5-118">TRUE</span></span> 
  
> <span data-ttu-id="3f3a5-119">Mindestens eine der angegebenen Eigenschaftennamensstrukturen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="3f3a5-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f3a5-120">FALSE</span></span> 
  
> <span data-ttu-id="3f3a5-121">Die angegebenen Eigenschaftennamensstrukturen sind alle gültig.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f3a5-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f3a5-122">Remarks</span></span>

<span data-ttu-id="3f3a5-123">Die **FBadRglpNameID-Funktion** kann beim Einrichten eines Aufrufs von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

