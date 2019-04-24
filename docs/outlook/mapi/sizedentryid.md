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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282684"
---
# <a name="sizedentryid"></a><span data-ttu-id="4a5d6-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="4a5d6-103">SizedENTRYID</span></span>

<span data-ttu-id="4a5d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a5d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a5d6-105">Erstellt eine benannte [Eintrags](entryid.md) -Struktur, die ein **ab** -Element einer angegebenen Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="4a5d6-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a5d6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4a5d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a5d6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4a5d6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4a5d6-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="4a5d6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4a5d6-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="4a5d6-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="4a5d6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a5d6-110">Parameters</span></span>

<span data-ttu-id="4a5d6-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="4a5d6-111">__cb_</span></span>
  
> <span data-ttu-id="4a5d6-112">Die Anzahl der Bytes im **ab** -Element der neuen Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a5d6-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="4a5d6-113">__Name_</span><span class="sxs-lookup"><span data-stu-id="4a5d6-113">__name_</span></span>
  
> <span data-ttu-id="4a5d6-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a5d6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a5d6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a5d6-115">Remarks</span></span>

<span data-ttu-id="4a5d6-116">Mit dem **SizedENTRYID** -Makro können Sie eine Eintrags-ID definieren, nachdem die Anforderungen an die Arraylänge bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="4a5d6-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="4a5d6-117">Verwenden Sie dieses Makro, um eine Eintrags-ID mit expliziten Begrenzungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a5d6-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="4a5d6-118">Um die neue Struktur zu verwenden, die aus dem **SizedENTRYID** -Makro als Zeiger auf eine **Eintrags** -Struktur resultiert, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="4a5d6-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="4a5d6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a5d6-119">See also</span></span>

- [<span data-ttu-id="4a5d6-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4a5d6-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="4a5d6-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="4a5d6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

