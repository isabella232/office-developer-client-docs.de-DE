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
ms.openlocfilehash: 2c5d4ec8381d6614cc2bc92fb0a762b068a97a81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791755"
---
# <a name="freepadrlist"></a><span data-ttu-id="f1958-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="f1958-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="f1958-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1958-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1958-105">Löscht eine [ADRLIST](adrlist.md) -Struktur und zugehörige Speicher, einschließlich des Speichers für alle Member Arrays und Strukturen frei.</span><span class="sxs-lookup"><span data-stu-id="f1958-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1958-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f1958-106">Header file:</span></span>  <br/> |<span data-ttu-id="f1958-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f1958-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f1958-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f1958-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f1958-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f1958-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f1958-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f1958-110">Called by:</span></span>  <br/> |<span data-ttu-id="f1958-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f1958-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="f1958-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1958-112">Parameters</span></span>

 <span data-ttu-id="f1958-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="f1958-113">_padrlist_</span></span>
  
> <span data-ttu-id="f1958-114">[in] Zeiger auf die **ADRLIST** -Struktur, die gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f1958-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f1958-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1958-115">Return value</span></span>

<span data-ttu-id="f1958-116">None.</span><span class="sxs-lookup"><span data-stu-id="f1958-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1958-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f1958-117">Notes to callers</span></span>

<span data-ttu-id="f1958-118">Als Teil der Implementierung der **FreePadrlist**ruft MAPI die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um alle Einträge in der Struktur **ADRLIST** frei, bevor die vollständige Struktur freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f1958-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="f1958-119">Daher müssen alle diese Einträge die Zuweisung Regeln für die [ADRLIST](adrlist.md) -Struktur befolgt haben, mit einer einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) rufen Sie für jedes Array mit Mitgliedern und Struktur.</span><span class="sxs-lookup"><span data-stu-id="f1958-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="f1958-120">Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** und **SRowSet** Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="f1958-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1958-121">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="f1958-121">MFCMAPI reference</span></span>

<span data-ttu-id="f1958-122">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f1958-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1958-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f1958-123">**File**</span></span>|<span data-ttu-id="f1958-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f1958-124">**Function**</span></span>|<span data-ttu-id="f1958-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f1958-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1958-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f1958-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f1958-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="f1958-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="f1958-128">MFCMAPI (engl.) verwendet die **FreePadrlist** -Methode, um eine ADRLIST-Struktur frei, die zum Hinzufügen einer einmaligen Adresse auf eine Nachricht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1958-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1958-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1958-129">See also</span></span>



[<span data-ttu-id="f1958-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f1958-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

