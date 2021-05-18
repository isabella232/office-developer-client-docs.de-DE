---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408642"
---
# <a name="freepadrlist"></a><span data-ttu-id="ab60e-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="ab60e-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="ab60e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab60e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab60e-105">Zerstört eine [ADRLIST-Struktur](adrlist.md) und gibt den zugeordneten Arbeitsspeicher frei, einschließlich des für alle Memberarrays und -strukturen zugewiesenen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="ab60e-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab60e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ab60e-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab60e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ab60e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ab60e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ab60e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab60e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab60e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab60e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ab60e-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab60e-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ab60e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="ab60e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab60e-112">Parameters</span></span>

 <span data-ttu-id="ab60e-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="ab60e-113">_padrlist_</span></span>
  
> <span data-ttu-id="ab60e-114">[in] Zeiger auf die zu zerstörende **ADRLIST-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="ab60e-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab60e-115">Return value</span><span class="sxs-lookup"><span data-stu-id="ab60e-115">Return value</span></span>

<span data-ttu-id="ab60e-116">None.</span><span class="sxs-lookup"><span data-stu-id="ab60e-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab60e-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ab60e-117">Notes to callers</span></span>

<span data-ttu-id="ab60e-118">Im Rahmen der Implementierung von **FreePadrlist** ruft MAPI die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um jeden Eintrag in der **ADRLIST-Struktur** frei zu geben, bevor die vollständige Struktur frei wird.</span><span class="sxs-lookup"><span data-stu-id="ab60e-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="ab60e-119">Daher müssen alle diese Einträge die Zuweisungsregeln für die [ADRLIST-Struktur](adrlist.md) befolgt haben, indem sie einen individuellen [MAPIAllocateBuffer-Aufruf](mapiallocatebuffer.md) für jedes Elementarray und jede Elementstruktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab60e-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="ab60e-120">Weitere Informationen zum Zuordnen von Arbeitsspeicher für **ADRLIST-** und **SRowSet-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="ab60e-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ab60e-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ab60e-121">MFCMAPI reference</span></span>

<span data-ttu-id="ab60e-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ab60e-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ab60e-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ab60e-123">**File**</span></span>|<span data-ttu-id="ab60e-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ab60e-124">**Function**</span></span>|<span data-ttu-id="ab60e-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ab60e-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab60e-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ab60e-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ab60e-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="ab60e-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="ab60e-128">MFCMAPI verwendet die **FreePadrlist-Methode,** um eine ADRLIST-Struktur frei zu geben, die zum Hinzufügen einer einmal verwendeten Adresse zu einer Nachricht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ab60e-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab60e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab60e-129">See also</span></span>



[<span data-ttu-id="ab60e-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ab60e-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

