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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791652"
---
# <a name="fbadentrylist"></a><span data-ttu-id="fa4ff-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="fa4ff-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="fa4ff-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa4ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa4ff-105">Eine Liste der MAPI-Eintragsbezeichner überprüft.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa4ff-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fa4ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa4ff-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="fa4ff-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="fa4ff-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa4ff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa4ff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa4ff-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa4ff-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fa4ff-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="fa4ff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa4ff-112">Parameters</span></span>

 <span data-ttu-id="fa4ff-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="fa4ff-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="fa4ff-114">[in] Zeiger auf eine [ENTRYLIST](entrylist.md) -Struktur, die ein Array von Eintragsbezeichner überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa4ff-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fa4ff-115">Return value</span></span>

<span data-ttu-id="fa4ff-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="fa4ff-116">TRUE</span></span> 
  
> <span data-ttu-id="fa4ff-117">Mindestens eines der aufgelisteten-Eintragsbezeichner sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="fa4ff-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="fa4ff-118">FALSE</span></span> 
  
> <span data-ttu-id="fa4ff-119">Alle der aufgelisteten-Eintragsbezeichner sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa4ff-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa4ff-120">Remarks</span></span>

<span data-ttu-id="fa4ff-121">Die **FBadEntryList** -Funktion bestimmt, ob die Liste den Eintrag Bezeichner ordnungsgemäß generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="fa4ff-122">Ein Beispiel für einen ungültigen Bezeichner ist eine für welche Speicher falsch zugewiesen wurde oder einen Bezeichner, der eine falsche Größe.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

