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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429488"
---
# <a name="fpropexists"></a><span data-ttu-id="6e783-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="6e783-103">FPropExists</span></span>

  
  
<span data-ttu-id="6e783-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e783-105">Sucht nach einem bestimmten Eigenschaftstag in einer [IMAPIProp-Schnittstelle](imapipropiunknown.md) oder einer Schnittstelle, die von **IMAPIProp** abgeleitet ist, z. B. [IMessage](imessageimapiprop.md) oder [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="6e783-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e783-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6e783-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e783-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6e783-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6e783-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6e783-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6e783-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6e783-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6e783-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6e783-110">Called by:</span></span>  <br/> |<span data-ttu-id="6e783-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6e783-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="6e783-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e783-112">Parameters</span></span>

 <span data-ttu-id="6e783-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="6e783-113">_pobj_</span></span>
  
> <span data-ttu-id="6e783-114">[in] Zeiger auf die VON IMAPIProp abgeleitete **IMAPIProp-Schnittstelle,** in der nach dem Eigenschaftstag gesucht werden soll. </span><span class="sxs-lookup"><span data-stu-id="6e783-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="6e783-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="6e783-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="6e783-116">[in] Eigenschaftstag, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e783-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e783-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e783-117">Return value</span></span>

<span data-ttu-id="6e783-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="6e783-118">TRUE</span></span> 
  
> <span data-ttu-id="6e783-119">Es wurde eine Übereinstimmung für das angegebene Eigenschaftstag gefunden.</span><span class="sxs-lookup"><span data-stu-id="6e783-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="6e783-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="6e783-120">FALSE</span></span> 
  
> <span data-ttu-id="6e783-121">Eine Übereinstimmung für das angegebene Eigenschaftstag wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6e783-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e783-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e783-122">Remarks</span></span>

<span data-ttu-id="6e783-123">Wenn das Eigenschaftstag im  _ulPropTag-Parameter_ den Typ PT_UNSPECIFIED hat, sucht die **FPropExists-Funktion** nach einer Übereinstimmung, die nur auf dem Eigenschaftenbezeichner basiert.</span><span class="sxs-lookup"><span data-stu-id="6e783-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="6e783-124">Andernfalls gilt die Übereinstimmung für das gesamte Eigenschaftstag, einschließlich des Typs.</span><span class="sxs-lookup"><span data-stu-id="6e783-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

