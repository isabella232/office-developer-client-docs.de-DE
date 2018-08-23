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
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570436"
---
# <a name="fpropexists"></a><span data-ttu-id="63e2a-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="63e2a-103">FPropExists</span></span>

  
  
<span data-ttu-id="63e2a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63e2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63e2a-105">Sucht nach einem bestimmten Eigenschaftentag in eine [IMAPIProp](imapipropiunknown.md) oder einer Schnittstelle abgeleitet **IMAPIProp**wie [IMessage](imessageimapiprop.md) oder [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="63e2a-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63e2a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="63e2a-106">Header file:</span></span>  <br/> |<span data-ttu-id="63e2a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="63e2a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="63e2a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="63e2a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="63e2a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="63e2a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="63e2a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="63e2a-110">Called by:</span></span>  <br/> |<span data-ttu-id="63e2a-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="63e2a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="63e2a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63e2a-112">Parameters</span></span>

 <span data-ttu-id="63e2a-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="63e2a-113">_pobj_</span></span>
  
> <span data-ttu-id="63e2a-114">[in] Zeiger auf die **IMAPIProp** Schnittstelle oder Schnittstelle abgeleitet **IMAPIProp** innerhalb für das Eigenschafts-Tag gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="63e2a-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="63e2a-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="63e2a-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="63e2a-116">[in] Eigenschaftentag für gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="63e2a-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63e2a-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="63e2a-117">Return value</span></span>

<span data-ttu-id="63e2a-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="63e2a-118">TRUE</span></span> 
  
> <span data-ttu-id="63e2a-119">Eine Übereinstimmung für das Tag für die angegebene Eigenschaft gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="63e2a-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="63e2a-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="63e2a-120">FALSE</span></span> 
  
> <span data-ttu-id="63e2a-121">Eine Übereinstimmung für das Tag für die angegebene Eigenschaft wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="63e2a-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63e2a-122">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="63e2a-122">Remarks</span></span>

<span data-ttu-id="63e2a-123">Wenn das Eigenschafts-Tag im Parameter _UlPropTag_ PT_UNSPECIFIED aufweist, sucht die **FPropExists** Funktion für eine Übereinstimmung nur anhand der Eigenschaftenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="63e2a-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="63e2a-124">Andernfalls wird die Übereinstimmung für das gesamte Eigenschafts-Tag, einschließlich der Art ein.</span><span class="sxs-lookup"><span data-stu-id="63e2a-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

