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
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341069"
---
# <a name="fbadentrylist"></a><span data-ttu-id="42ad4-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="42ad4-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="42ad4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42ad4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42ad4-105">Überprüft eine Liste von MAPI-Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="42ad4-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42ad4-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="42ad4-106">Header file:</span></span>  <br/> |<span data-ttu-id="42ad4-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="42ad4-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="42ad4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="42ad4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42ad4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42ad4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42ad4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="42ad4-110">Called by:</span></span>  <br/> |<span data-ttu-id="42ad4-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="42ad4-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="42ad4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42ad4-112">Parameters</span></span>

 <span data-ttu-id="42ad4-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="42ad4-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="42ad4-114">in Zeiger auf eine [entrylist](entrylist.md) -Struktur, die ein Array von Eintrags-IDs enthält, die validiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42ad4-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42ad4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42ad4-115">Return value</span></span>

<span data-ttu-id="42ad4-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="42ad4-116">TRUE</span></span> 
  
> <span data-ttu-id="42ad4-117">Mindestens einer der aufgeführten Eintragsbezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="42ad4-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="42ad4-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="42ad4-118">FALSE</span></span> 
  
> <span data-ttu-id="42ad4-119">Alle aufgeführten Eintragsbezeichner sind gültig.</span><span class="sxs-lookup"><span data-stu-id="42ad4-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42ad4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42ad4-120">Remarks</span></span>

<span data-ttu-id="42ad4-121">Die **FBadEntryList** -Funktion bestimmt, ob die Eintrags-ID-Liste ordnungsgemäß generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="42ad4-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="42ad4-122">Ein Beispiel für einen ungültigen Bezeichner ist einer, für den der Arbeitsspeicher falsch zugeordnet wurde, oder ein Bezeichner mit einer falschen Größe.</span><span class="sxs-lookup"><span data-stu-id="42ad4-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

