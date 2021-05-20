---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438820"
---
# <a name="freeprows"></a><span data-ttu-id="b19d3-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="b19d3-103">FreeProws</span></span>

  
  
<span data-ttu-id="b19d3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b19d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b19d3-105">Zerstört eine [SRowSet-Struktur](srowset.md) und gibt den zugeordneten Arbeitsspeicher frei, einschließlich des für alle Memberarrays und -strukturen zugewiesenen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="b19d3-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b19d3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b19d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="b19d3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b19d3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b19d3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b19d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b19d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b19d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b19d3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b19d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="b19d3-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b19d3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="b19d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b19d3-112">Parameters</span></span>

 <span data-ttu-id="b19d3-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="b19d3-113">_prows_</span></span>
  
> <span data-ttu-id="b19d3-114">[in] Zeiger auf die **zu zerstörende SRowSet-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="b19d3-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b19d3-115">Return value</span><span class="sxs-lookup"><span data-stu-id="b19d3-115">Return value</span></span>

<span data-ttu-id="b19d3-116">None.</span><span class="sxs-lookup"><span data-stu-id="b19d3-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b19d3-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b19d3-117">Notes to callers</span></span>

<span data-ttu-id="b19d3-118">Im Rahmen der Implementierung von **FreeProws** ruft MAPI die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um jeden Eintrag in der **SRowSet-Struktur** frei zu geben, bevor die vollständige Struktur frei wird.</span><span class="sxs-lookup"><span data-stu-id="b19d3-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="b19d3-119">Daher müssen alle diese Einträge die Zuweisungsregeln für die [SRowSet-Struktur](srowset.md) befolgt haben, indem sie einen individuellen [MAPIAllocateBuffer-Aufruf](mapiallocatebuffer.md) für jedes Elementarray und jede Elementstruktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="b19d3-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="b19d3-120">Weitere Informationen zum Zuordnen von Arbeitsspeicher für **ADRLIST-** und **SRowSet-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b19d3-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b19d3-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b19d3-121">MFCMAPI reference</span></span>

<span data-ttu-id="b19d3-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b19d3-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b19d3-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b19d3-123">**File**</span></span>|<span data-ttu-id="b19d3-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b19d3-124">**Function**</span></span>|<span data-ttu-id="b19d3-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b19d3-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b19d3-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b19d3-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b19d3-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="b19d3-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="b19d3-128">MFCMAPI verwendet die **FreeProws-Methode,** um eine SRowSet-Struktur frei zu geben, die Zeilen der zu verarbeitenden Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="b19d3-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b19d3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b19d3-129">See also</span></span>



[<span data-ttu-id="b19d3-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b19d3-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

