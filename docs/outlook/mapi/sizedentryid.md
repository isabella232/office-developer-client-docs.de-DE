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
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405709"
---
# <a name="sizedentryid"></a><span data-ttu-id="2db83-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="2db83-103">SizedENTRYID</span></span>

<span data-ttu-id="2db83-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2db83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2db83-105">Erstellt eine benannte [ENTRYID-Struktur,](entryid.md) die ein **ab-Element** einer angegebenen Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="2db83-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2db83-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2db83-106">Header file:</span></span>  <br/> |<span data-ttu-id="2db83-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2db83-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2db83-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="2db83-108">Related structure:</span></span>  <br/> |<span data-ttu-id="2db83-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="2db83-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="2db83-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2db83-110">Parameters</span></span>

<span data-ttu-id="2db83-111">_ _cb_</span><span class="sxs-lookup"><span data-stu-id="2db83-111">_ _cb_</span></span>
  
> <span data-ttu-id="2db83-112">Anzahl der Bytes im **ab-Element** der neuen Struktur.</span><span class="sxs-lookup"><span data-stu-id="2db83-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="2db83-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="2db83-113">_ _name_</span></span>
  
> <span data-ttu-id="2db83-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="2db83-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2db83-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2db83-115">Remarks</span></span>

<span data-ttu-id="2db83-116">Mit **dem Makro SizedENTRYID** können Sie einen Eintragsbezeichner definieren, nachdem die Anforderungen an die Arraylänge bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="2db83-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="2db83-117">Verwenden Sie dieses Makro, um einen Eintragsbezeichner mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2db83-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="2db83-118">Führen Sie die folgende Gliederung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedENTRYID** als Zeiger auf eine **ENTRYID-Struktur** resultiert:</span><span class="sxs-lookup"><span data-stu-id="2db83-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="2db83-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2db83-119">See also</span></span>

- [<span data-ttu-id="2db83-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2db83-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="2db83-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="2db83-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

