---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427773"
---
# <a name="fbadentrylist"></a><span data-ttu-id="d0f2f-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="d0f2f-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="d0f2f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0f2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0f2f-105">Überprüft eine Liste der MAPI-Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="d0f2f-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0f2f-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="d0f2f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d0f2f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d0f2f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d0f2f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d0f2f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0f2f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d0f2f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d0f2f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d0f2f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d0f2f-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d0f2f-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="d0f2f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0f2f-112">Parameters</span></span>

 <span data-ttu-id="d0f2f-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="d0f2f-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="d0f2f-114">[in] Zeiger auf eine [ENTRYLIST-Struktur,](entrylist.md) die ein Array von Eintragsbezeichnern enthält, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0f2f-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d0f2f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0f2f-115">Return value</span></span>

<span data-ttu-id="d0f2f-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d0f2f-116">TRUE</span></span> 
  
> <span data-ttu-id="d0f2f-117">Mindestens eine der aufgeführten Eintragsbezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d0f2f-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="d0f2f-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d0f2f-118">FALSE</span></span> 
  
> <span data-ttu-id="d0f2f-119">Alle aufgeführten Eintragsbezeichner sind gültig.</span><span class="sxs-lookup"><span data-stu-id="d0f2f-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0f2f-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0f2f-120">Remarks</span></span>

<span data-ttu-id="d0f2f-121">Die **FBadEntryList-Funktion** bestimmt, ob die Eintragsbezeichnerliste ordnungsgemäß generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d0f2f-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="d0f2f-122">Ein Beispiel für einen ungültigen Bezeichner ist ein Bezeichner, für den der Arbeitsspeicher falsch zugewiesen wurde, oder ein Bezeichner mit einer falschen Größe.</span><span class="sxs-lookup"><span data-stu-id="d0f2f-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

