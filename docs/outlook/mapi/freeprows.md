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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 93659a28969efd0d04e9fc44f8926e89586f7773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791748"
---
# <a name="freeprows"></a><span data-ttu-id="b141a-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="b141a-103">FreeProws</span></span>

  
  
<span data-ttu-id="b141a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b141a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b141a-105">Löscht eine [SRowSet](srowset.md) -Struktur und zugehörige Speicher, einschließlich des Speichers für alle Member Arrays und Strukturen frei.</span><span class="sxs-lookup"><span data-stu-id="b141a-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b141a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b141a-106">Header file:</span></span>  <br/> |<span data-ttu-id="b141a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b141a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b141a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b141a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b141a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b141a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b141a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b141a-110">Called by:</span></span>  <br/> |<span data-ttu-id="b141a-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b141a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="b141a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b141a-112">Parameters</span></span>

 <span data-ttu-id="b141a-113">_PROWS_</span><span class="sxs-lookup"><span data-stu-id="b141a-113">_prows_</span></span>
  
> <span data-ttu-id="b141a-114">[in] Zeiger auf die **SRowSet** -Struktur, die gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b141a-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b141a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b141a-115">Return value</span></span>

<span data-ttu-id="b141a-116">None.</span><span class="sxs-lookup"><span data-stu-id="b141a-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b141a-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b141a-117">Notes to callers</span></span>

<span data-ttu-id="b141a-118">Als Teil der Implementierung der **FreeProws**ruft MAPI [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um alle Einträge in der Struktur **SRowSet** freizugeben, bevor die vollständige Struktur freigegeben.</span><span class="sxs-lookup"><span data-stu-id="b141a-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="b141a-119">Aus diesem Grund alle diese Einträge müssen die Zuweisung Regeln für die [SRowSet](srowset.md) -Struktur folgen, mit einer einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) rufen Sie für jedes Array mit Mitgliedern und Struktur.</span><span class="sxs-lookup"><span data-stu-id="b141a-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="b141a-120">Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** und **SRowSet** Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b141a-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b141a-121">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="b141a-121">MFCMAPI reference</span></span>

<span data-ttu-id="b141a-122">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b141a-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b141a-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b141a-123">**File**</span></span>|<span data-ttu-id="b141a-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b141a-124">**Function**</span></span>|<span data-ttu-id="b141a-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b141a-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b141a-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b141a-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b141a-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="b141a-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="b141a-128">MFCMAPI (engl.) verwendet die **FreeProws** -Methode, um eine SRowSet-Struktur, die Zeilen der Tabelle verarbeitet enthält frei.</span><span class="sxs-lookup"><span data-stu-id="b141a-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b141a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b141a-129">See also</span></span>



[<span data-ttu-id="b141a-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b141a-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

