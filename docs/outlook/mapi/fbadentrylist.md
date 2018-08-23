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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582910"
---
# <a name="fbadentrylist"></a><span data-ttu-id="93efd-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="93efd-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="93efd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93efd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93efd-105">Eine Liste der MAPI-Eintragsbezeichner überprüft.</span><span class="sxs-lookup"><span data-stu-id="93efd-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93efd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="93efd-106">Header file:</span></span>  <br/> |<span data-ttu-id="93efd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="93efd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="93efd-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="93efd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93efd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93efd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93efd-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="93efd-110">Called by:</span></span>  <br/> |<span data-ttu-id="93efd-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="93efd-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="93efd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="93efd-112">Parameters</span></span>

 <span data-ttu-id="93efd-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="93efd-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="93efd-114">[in] Zeiger auf eine [ENTRYLIST](entrylist.md) -Struktur, die ein Array von Eintragsbezeichner überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="93efd-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93efd-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="93efd-115">Return value</span></span>

<span data-ttu-id="93efd-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="93efd-116">TRUE</span></span> 
  
> <span data-ttu-id="93efd-117">Mindestens eines der aufgelisteten-Eintragsbezeichner sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="93efd-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="93efd-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="93efd-118">FALSE</span></span> 
  
> <span data-ttu-id="93efd-119">Alle der aufgelisteten-Eintragsbezeichner sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="93efd-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93efd-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="93efd-120">Remarks</span></span>

<span data-ttu-id="93efd-121">Die **FBadEntryList** -Funktion bestimmt, ob die Liste den Eintrag Bezeichner ordnungsgemäß generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="93efd-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="93efd-122">Ein Beispiel für einen ungültigen Bezeichner ist eine für welche Speicher falsch zugewiesen wurde oder einen Bezeichner, der eine falsche Größe.</span><span class="sxs-lookup"><span data-stu-id="93efd-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

