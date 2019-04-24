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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328035"
---
# <a name="freepadrlist"></a><span data-ttu-id="ba884-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="ba884-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="ba884-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba884-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba884-105">Zerstört eine [ADRLIST](adrlist.md) -Struktur und gibt zugeordneten Arbeitsspeicher frei, einschließlich des Arbeitsspeichers, der für alle Elementarrays und-Strukturen reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="ba884-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba884-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ba884-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba884-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ba884-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ba884-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ba884-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba884-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba884-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ba884-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ba884-110">Called by:</span></span>  <br/> |<span data-ttu-id="ba884-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ba884-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="ba884-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba884-112">Parameters</span></span>

 <span data-ttu-id="ba884-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="ba884-113">_padrlist_</span></span>
  
> <span data-ttu-id="ba884-114">in Zeiger auf die **ADRLIST** -Struktur, die zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba884-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ba884-115">Return value</span><span class="sxs-lookup"><span data-stu-id="ba884-115">Return value</span></span>

<span data-ttu-id="ba884-116">None.</span><span class="sxs-lookup"><span data-stu-id="ba884-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ba884-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ba884-117">Notes to callers</span></span>

<span data-ttu-id="ba884-118">Im Rahmen der Implementierung von **FreePadrlist**ruft MAPI die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um jeden Eintrag in der **ADRLIST** -Struktur freizugeben, bevor die gesamte Struktur freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba884-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="ba884-119">Daher müssen alle diese Einträge den Zuordnungsregeln für die [ADRLIST](adrlist.md) -Struktur unter Verwendung eines einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) -Aufrufs für die einzelnen Elementarrays und-Strukturen gefolgt sein.</span><span class="sxs-lookup"><span data-stu-id="ba884-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="ba884-120">Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** -und **SRowSet** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="ba884-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba884-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ba884-121">MFCMAPI reference</span></span>

<span data-ttu-id="ba884-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ba884-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba884-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ba884-123">**File**</span></span>|<span data-ttu-id="ba884-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ba884-124">**Function**</span></span>|<span data-ttu-id="ba884-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ba884-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba884-126">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="ba884-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ba884-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="ba884-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="ba884-128">MFCMAPI verwendet die **FreePadrlist** -Methode, um eine ADRLIST-Struktur freizugeben, die zum Hinzufügen einer einmaligen Adresse zu einer Nachricht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba884-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba884-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba884-129">See also</span></span>



[<span data-ttu-id="ba884-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ba884-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

