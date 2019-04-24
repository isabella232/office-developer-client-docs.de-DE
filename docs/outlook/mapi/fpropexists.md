---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327272"
---
# <a name="fpropexists"></a><span data-ttu-id="dd1cf-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="dd1cf-103">FPropExists</span></span>

  
  
<span data-ttu-id="dd1cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd1cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd1cf-105">Sucht nach einem bestimmten Property-Tag in einer [IMAPIProp](imapipropiunknown.md) -Schnittstelle oder einer von **IMAPIProp**abgeleiteten Schnittstelle wie [IMessage](imessageimapiprop.md) oder [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="dd1cf-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd1cf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dd1cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd1cf-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="dd1cf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dd1cf-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dd1cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd1cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd1cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd1cf-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dd1cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd1cf-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="dd1cf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="dd1cf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd1cf-112">Parameters</span></span>

 <span data-ttu-id="dd1cf-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="dd1cf-113">_pobj_</span></span>
  
> <span data-ttu-id="dd1cf-114">in Zeiger auf die **IMAPIProp** -Schnittstelle oder-Schnittstelle, die von **IMAPIProp** abgeleitet ist, in der nach dem Property-Tag gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd1cf-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="dd1cf-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="dd1cf-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="dd1cf-116">in Eigenschaftentag, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd1cf-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd1cf-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd1cf-117">Return value</span></span>

<span data-ttu-id="dd1cf-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd1cf-118">TRUE</span></span> 
  
> <span data-ttu-id="dd1cf-119">Eine Übereinstimmung für das angegebene Property-Tag wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="dd1cf-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="dd1cf-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd1cf-120">FALSE</span></span> 
  
> <span data-ttu-id="dd1cf-121">Eine Übereinstimmung für das angegebene Property-Tag wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="dd1cf-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd1cf-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd1cf-122">Remarks</span></span>

<span data-ttu-id="dd1cf-123">Wenn das Property-Tag im _ulPropTag_ -Parameter den Typ PT_UNSPECIFIED hat, sucht die **FPropExists** -Funktion nach einer Übereinstimmung, die nur auf dem Eigenschaftenbezeichner basiert.</span><span class="sxs-lookup"><span data-stu-id="dd1cf-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="dd1cf-124">Andernfalls ist die Übereinstimmung für das gesamte Property-Tag, einschließlich des Typs.</span><span class="sxs-lookup"><span data-stu-id="dd1cf-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

