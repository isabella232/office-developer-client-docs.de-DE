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
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791746"
---
# <a name="fpropexists"></a><span data-ttu-id="b50c1-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="b50c1-103">FPropExists</span></span>

  
  
<span data-ttu-id="b50c1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b50c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b50c1-105">Sucht nach einem bestimmten Eigenschaftentag in eine [IMAPIProp](imapipropiunknown.md) oder einer Schnittstelle abgeleitet **IMAPIProp**wie [IMessage](imessageimapiprop.md) oder [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b50c1-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b50c1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b50c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="b50c1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b50c1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b50c1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b50c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b50c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b50c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b50c1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b50c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="b50c1-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b50c1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="b50c1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b50c1-112">Parameters</span></span>

 <span data-ttu-id="b50c1-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="b50c1-113">_pobj_</span></span>
  
> <span data-ttu-id="b50c1-114">[in] Zeiger auf die **IMAPIProp** Schnittstelle oder Schnittstelle abgeleitet **IMAPIProp** innerhalb für das Eigenschafts-Tag gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b50c1-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="b50c1-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="b50c1-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="b50c1-116">[in] Eigenschaftentag für gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b50c1-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b50c1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b50c1-117">Return value</span></span>

<span data-ttu-id="b50c1-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="b50c1-118">TRUE</span></span> 
  
> <span data-ttu-id="b50c1-119">Eine Übereinstimmung für das Tag für die angegebene Eigenschaft gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="b50c1-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="b50c1-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="b50c1-120">FALSE</span></span> 
  
> <span data-ttu-id="b50c1-121">Eine Übereinstimmung für das Tag für die angegebene Eigenschaft wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b50c1-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b50c1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b50c1-122">Remarks</span></span>

<span data-ttu-id="b50c1-123">Wenn das Eigenschafts-Tag im Parameter _UlPropTag_ PT_UNSPECIFIED aufweist, sucht die **FPropExists** Funktion für eine Übereinstimmung nur anhand der Eigenschaftenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b50c1-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="b50c1-124">Andernfalls wird die Übereinstimmung für das gesamte Eigenschafts-Tag, einschließlich der Art ein.</span><span class="sxs-lookup"><span data-stu-id="b50c1-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

