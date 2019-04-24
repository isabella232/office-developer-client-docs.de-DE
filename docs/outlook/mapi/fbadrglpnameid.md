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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341034"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="53d12-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="53d12-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="53d12-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53d12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53d12-105">Überprüft ein Array von Strukturen, die benannte Eigenschaften beschreiben und deren Zuordnung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="53d12-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53d12-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="53d12-106">Header file:</span></span>  <br/> |<span data-ttu-id="53d12-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="53d12-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="53d12-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="53d12-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="53d12-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="53d12-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="53d12-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="53d12-110">Called by:</span></span>  <br/> |<span data-ttu-id="53d12-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="53d12-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="53d12-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="53d12-112">Parameters</span></span>

 <span data-ttu-id="53d12-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="53d12-113">_lppNameId_</span></span>
  
> <span data-ttu-id="53d12-114">in Zeiger auf ein Array von [MAPINAMEID](mapinameid.md) -Strukturen, die die benannten Eigenschaften beschreiben.</span><span class="sxs-lookup"><span data-stu-id="53d12-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="53d12-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="53d12-115">_cNames_</span></span>
  
> <span data-ttu-id="53d12-116">in Die Anzahl der benannten Eigenschaftsstrukturen im Array, auf die durch den _lppNameId_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="53d12-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="53d12-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53d12-117">Return value</span></span>

<span data-ttu-id="53d12-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="53d12-118">TRUE</span></span> 
  
> <span data-ttu-id="53d12-119">Mindestens eine der angegebenen Strukturen für den Eigenschaftennamen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="53d12-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="53d12-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="53d12-120">FALSE</span></span> 
  
> <span data-ttu-id="53d12-121">Die angegebenen Strukturen für den Eigenschaftennamen sind alle gültig.</span><span class="sxs-lookup"><span data-stu-id="53d12-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53d12-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53d12-122">Remarks</span></span>

<span data-ttu-id="53d12-123">Die **FBadRglpNameID** -Funktion kann verwendet werden, wenn Sie einen Aufruf von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md)einrichten.</span><span class="sxs-lookup"><span data-stu-id="53d12-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

