---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d960207e05b33efe55886166ff1322f7f4eedce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586200"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="4b7f5-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="4b7f5-103">SizedDtblLabel</span></span>

<span data-ttu-id="4b7f5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b7f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b7f5-105">Erstellt eine benannte Struktur, die eine [DTBLLABEL](dtbllabel.md) -Struktur für die Beschreibung ein Label-Steuerelement und das zugeordnete Beschriftung an einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="4b7f5-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b7f5-106">In der Headerdatei angegeben:</span><span class="sxs-lookup"><span data-stu-id="4b7f5-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="4b7f5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b7f5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4b7f5-108">Verwandte Struktur</span><span class="sxs-lookup"><span data-stu-id="4b7f5-108">Related structure</span></span>  <br/> |<span data-ttu-id="4b7f5-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="4b7f5-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="4b7f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b7f5-110">Parameters</span></span>

<span data-ttu-id="4b7f5-111">_n_</span><span class="sxs-lookup"><span data-stu-id="4b7f5-111">_n_</span></span>
  
> <span data-ttu-id="4b7f5-112">Länge der Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="4b7f5-112">Length of the label.</span></span> <span data-ttu-id="4b7f5-113">Dazu gehört das letzte Zeichen NULL.</span><span class="sxs-lookup"><span data-stu-id="4b7f5-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="4b7f5-114">_u_</span><span class="sxs-lookup"><span data-stu-id="4b7f5-114">_u_</span></span>
  
> <span data-ttu-id="4b7f5-115">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b7f5-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b7f5-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4b7f5-116">Remarks</span></span>

<span data-ttu-id="4b7f5-117">Das Makro **SizedDtblLabel** können Sie eine Beschriftung anzeigen Tabelle definieren, wenn die Anzahl der Zeichen in der Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4b7f5-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="4b7f5-118">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="4b7f5-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="4b7f5-119">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblLabel** als Zeiger Struktur **DTBLLABEL** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="4b7f5-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="4b7f5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b7f5-120">See also</span></span>

- [<span data-ttu-id="4b7f5-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="4b7f5-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="4b7f5-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="4b7f5-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

