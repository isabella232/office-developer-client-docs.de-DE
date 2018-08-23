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
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588146"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="f75d8-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="f75d8-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="f75d8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f75d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f75d8-105">Ein Array von Strukturen, die beschreiben, benannte Eigenschaften überprüft und deren Zuordnung überprüft.</span><span class="sxs-lookup"><span data-stu-id="f75d8-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f75d8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f75d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="f75d8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f75d8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f75d8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f75d8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f75d8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f75d8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f75d8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f75d8-110">Called by:</span></span>  <br/> |<span data-ttu-id="f75d8-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f75d8-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="f75d8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f75d8-112">Parameters</span></span>

 <span data-ttu-id="f75d8-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="f75d8-113">_lppNameId_</span></span>
  
> <span data-ttu-id="f75d8-114">[in] Zeiger auf ein Array von [MAPINAMEID](mapinameid.md) -Strukturen, die die benannten Eigenschaften beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f75d8-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="f75d8-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="f75d8-115">_cNames_</span></span>
  
> <span data-ttu-id="f75d8-116">[in] Anzahl der benannten Eigenschaft Strukturen im Array auf den durch den Parameter _LppNameId_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f75d8-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f75d8-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f75d8-117">Return value</span></span>

<span data-ttu-id="f75d8-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="f75d8-118">TRUE</span></span> 
  
> <span data-ttu-id="f75d8-119">Eine oder mehrere der angegebenen Eigenschaft Name Strukturen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f75d8-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="f75d8-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="f75d8-120">FALSE</span></span> 
  
> <span data-ttu-id="f75d8-121">Die angegebene Eigenschaft Name Strukturen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="f75d8-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f75d8-122">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f75d8-122">Remarks</span></span>

<span data-ttu-id="f75d8-123">Die **FBadRglpNameID** -Funktion kann verwendet werden, wenn für einen Anruf an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)einrichten.</span><span class="sxs-lookup"><span data-stu-id="f75d8-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

