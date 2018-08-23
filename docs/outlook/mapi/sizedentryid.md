---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563870"
---
# <a name="sizedentryid"></a><span data-ttu-id="cf5c5-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="cf5c5-103">SizedENTRYID</span></span>

<span data-ttu-id="cf5c5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf5c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf5c5-105">Erstellt eine benannte [ENTRYID](entryid.md) -Struktur, die ein Element **Ab** einer angegebenen Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="cf5c5-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf5c5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cf5c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf5c5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf5c5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cf5c5-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="cf5c5-108">Related structure:</span></span>  <br/> |<span data-ttu-id="cf5c5-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="cf5c5-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="cf5c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf5c5-110">Parameters</span></span>

<span data-ttu-id="cf5c5-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="cf5c5-111">__cb_</span></span>
  
> <span data-ttu-id="cf5c5-112">Die Anzahl von Bytes in die neue Struktur Mitglied **Ab** .</span><span class="sxs-lookup"><span data-stu-id="cf5c5-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="cf5c5-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="cf5c5-113">__name_</span></span>
  
> <span data-ttu-id="cf5c5-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="cf5c5-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf5c5-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="cf5c5-115">Remarks</span></span>

<span data-ttu-id="cf5c5-116">Das Makro **SizedENTRYID** können Sie eine Eintrags-ID zu definieren, nach dem Array Länge Anforderungen bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="cf5c5-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="cf5c5-117">Verwenden Sie dieses Makro mit expliziten Grenzen eines Eintrags-ID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf5c5-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="cf5c5-118">Um die neue Struktur verwenden, die als Zeiger auf eine **ENTRYID** -Struktur aus dem Makro **SizedENTRYID** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="cf5c5-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="cf5c5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf5c5-119">See also</span></span>

- [<span data-ttu-id="cf5c5-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cf5c5-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="cf5c5-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="cf5c5-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

