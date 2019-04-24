---
title: Verwalten von Speicher für ADRLIST- und SRowSet-Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298128"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="e796a-103">Verwalten von Speicher für ADRLIST-und SRowSet-Strukturen "</span><span class="sxs-lookup"><span data-stu-id="e796a-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="e796a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e796a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e796a-105">Die Anforderung zum Zuweisen des gesamten Speichers für einen Puffer, wann immer möglich mit einem einzelnen **MAPIAllocateBuffer** -Aufruf gilt nicht bei der Verwendung der Adressliste oder **ADRLIST**-und Zeilensatz-oder **SRowSet**-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e796a-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="e796a-106">Diese beiden Strukturen sind Ausnahmen für die Standardregeln für das zuordnen und Freigeben von Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e796a-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="e796a-107">Sie enthalten mehrere Ebenen von Strukturen und sollen das Hinzufügen oder Entfernen einzelner Elemente ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e796a-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="e796a-108">Daher muss jede Eigenschaft eine separate Zuordnung sein.</span><span class="sxs-lookup"><span data-stu-id="e796a-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="e796a-109">Wo die meisten Strukturen mit einem Aufruf von **mapifreebufferfreigegeben**freigegeben werden, muss jeder einzelne Eintrag in einer **ADRLIST** -oder **SRowSet** -Struktur mit einem eigenen Aufruf von **mapifreebufferfreigegeben** oder einem einzelnen Aufruf von **FreeProws** oder \*\* FreePadrlist\*\*.</span><span class="sxs-lookup"><span data-stu-id="e796a-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="e796a-110">Weitere Informationen finden Sie unter [mapifreebufferfreigegeben](mapifreebuffer.md), [ADRLIST](adrlist.md)und [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="e796a-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="e796a-111">**FreeProws** und **FREEPADRLIST** sind von MAPI bereitgestellte Funktionen zur Vereinfachung der Freigabe dieser Datenstrukturen.</span><span class="sxs-lookup"><span data-stu-id="e796a-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="e796a-112">Weitere Informationen finden Sie unter [FreeProws](freeprows.md) und [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="e796a-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="e796a-113">**FreePadrlist** gibt den Arbeitsspeicher für die **ADRLIST** -Struktur und den gesamten zugeordneten Arbeitsspeicher für die Strukturmember frei. **FreeProws** führt dasselbe für die **SRowSet** -Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="e796a-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="e796a-114">Das folgende Diagramm zeigt das Layout einer **ADRLIST** -Datenstruktur, die die getrennten Speicherzuordnungen angibt, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e796a-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="e796a-115">Die grauen Felder zeigen Arbeitsspeicher, der mit einem Anruf reserviert und freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e796a-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="e796a-116">**ADRLIST-Speicherzuweisung**</span><span class="sxs-lookup"><span data-stu-id="e796a-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="e796a-117">![ADRLIST-Speicherbelegung] (media/amapi_52.gif "ADRLIST-Speicherbelegung")</span><span class="sxs-lookup"><span data-stu-id="e796a-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e796a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e796a-118">See also</span></span>

- [<span data-ttu-id="e796a-119">Verwalten von Speicher in MAPI</span><span class="sxs-lookup"><span data-stu-id="e796a-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

