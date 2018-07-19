---
title: Verwalten des Arbeitsspeichers für ADRLIST und SRowSet Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab582b869fb5a53d7ac4e97e039d9bde4a4f0430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792927"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="5960c-103">Verwalten des Arbeitsspeichers für ADRLIST und SRowSet Strukturen"</span><span class="sxs-lookup"><span data-stu-id="5960c-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="5960c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5960c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5960c-105">Die Anforderung für einen Puffer mit einem einzigen Aufruf **MAPIAllocateBuffer** möglichst alle Speicher wird bei Verwendung der Adressliste oder **ADRLIST**, und die Zeile Set oder **SRowSet**, Strukturen nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="5960c-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="5960c-106">Diese zwei Strukturen sind Ausnahmen für die standard-Regeln für das zuordnen und Freigeben von Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5960c-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="5960c-107">Enthalten mehrere Ebenen von Strukturen, und aktivieren einzelne Mitglieder hinzugefügt oder entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5960c-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="5960c-108">Aus diesem Grund muss jede Eigenschaft eine separate Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="5960c-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="5960c-109">Wobei die meisten Strukturen mit einem einzigen Aufruf **MAPIFreeBuffer**, jeden einzelnen Eintrag in einer **ADRLIST** oder **SRowSet** freigegeben werden, muss mit einem eigenen Aufruf **MAPIFreeBuffer** oder einem einzigen Aufruf von **FreeProws** oder **freigegeben werden FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="5960c-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="5960c-110">Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)und [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="5960c-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="5960c-111">**FreeProws** und **FreePadrlist** sind Funktionen zur Vereinfachung der die Freigabe dieser Datenstrukturen MAPI bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5960c-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="5960c-112">Weitere Informationen finden Sie unter [FreeProws](freeprows.md) und [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="5960c-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="5960c-113">**FreePadrlist** frei der Arbeitsspeicher für die **ADRLIST** -Struktur sowie alle zugehörigen Speicher für die Struktur Mitglieder; **FreeProws** führt den gleichen Wert für die **SRowSet** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5960c-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="5960c-114">Das folgende Diagramm zeigt das Layout der **ADRLIST** -Datenstruktur, der angibt, der separate Arbeitsspeicher Zuweisungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5960c-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="5960c-115">Die grauen Felder anzeigen Arbeitsspeicher, die reserviert und mit einem einzigen Aufruf freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="5960c-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="5960c-116">**ADRLIST-Speicherzuweisung**</span><span class="sxs-lookup"><span data-stu-id="5960c-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="5960c-117">![ADRLIST-speicherzuweisung] (media/amapi_52.gif "ADRLIST-speicherzuweisung")</span><span class="sxs-lookup"><span data-stu-id="5960c-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5960c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5960c-118">See also</span></span>

- [<span data-ttu-id="5960c-119">Verwalten von Arbeitsspeicher in MAPI</span><span class="sxs-lookup"><span data-stu-id="5960c-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

