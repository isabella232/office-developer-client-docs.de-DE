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
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791657"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="8b58c-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="8b58c-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="8b58c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8b58c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8b58c-105">Ein Array von Strukturen, die beschreiben, benannte Eigenschaften überprüft und deren Zuordnung überprüft.</span><span class="sxs-lookup"><span data-stu-id="8b58c-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b58c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8b58c-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b58c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="8b58c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="8b58c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8b58c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8b58c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8b58c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8b58c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8b58c-110">Called by:</span></span>  <br/> |<span data-ttu-id="8b58c-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8b58c-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="8b58c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b58c-112">Parameters</span></span>

 <span data-ttu-id="8b58c-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="8b58c-113">_lppNameId_</span></span>
  
> <span data-ttu-id="8b58c-114">[in] Zeiger auf ein Array von [MAPINAMEID](mapinameid.md) -Strukturen, die die benannten Eigenschaften beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8b58c-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="8b58c-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="8b58c-115">_cNames_</span></span>
  
> <span data-ttu-id="8b58c-116">[in] Anzahl der benannten Eigenschaft Strukturen im Array auf den durch den Parameter _LppNameId_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="8b58c-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8b58c-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8b58c-117">Return value</span></span>

<span data-ttu-id="8b58c-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="8b58c-118">TRUE</span></span> 
  
> <span data-ttu-id="8b58c-119">Eine oder mehrere der angegebenen Eigenschaft Name Strukturen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8b58c-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="8b58c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="8b58c-120">FALSE</span></span> 
  
> <span data-ttu-id="8b58c-121">Die angegebene Eigenschaft Name Strukturen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="8b58c-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b58c-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b58c-122">Remarks</span></span>

<span data-ttu-id="8b58c-123">Die **FBadRglpNameID** -Funktion kann verwendet werden, wenn für einen Anruf an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) oder [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)einrichten.</span><span class="sxs-lookup"><span data-stu-id="8b58c-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

