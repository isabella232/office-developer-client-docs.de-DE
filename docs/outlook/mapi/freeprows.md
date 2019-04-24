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
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328014"
---
# <a name="freeprows"></a><span data-ttu-id="0e354-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="0e354-103">FreeProws</span></span>

  
  
<span data-ttu-id="0e354-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e354-105">Zerstört eine [SRowSet](srowset.md) -Struktur und gibt zugeordneten Arbeitsspeicher frei, einschließlich des Arbeitsspeichers, der für alle Elementarrays und-Strukturen reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="0e354-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e354-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0e354-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e354-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0e354-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0e354-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0e354-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e354-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e354-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e354-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0e354-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e354-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0e354-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="0e354-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e354-112">Parameters</span></span>

 <span data-ttu-id="0e354-113">_PROWS_</span><span class="sxs-lookup"><span data-stu-id="0e354-113">_prows_</span></span>
  
> <span data-ttu-id="0e354-114">in Zeiger auf die **SRowSet** -Struktur, die zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e354-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e354-115">Return value</span><span class="sxs-lookup"><span data-stu-id="0e354-115">Return value</span></span>

<span data-ttu-id="0e354-116">None.</span><span class="sxs-lookup"><span data-stu-id="0e354-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e354-117">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0e354-117">Notes to callers</span></span>

<span data-ttu-id="0e354-118">Im Rahmen der Implementierung von **FreeProws**ruft MAPI die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um jeden Eintrag in der **SRowSet** -Struktur freizugeben, bevor die gesamte Struktur freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e354-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="0e354-119">Daher müssen alle diese Einträge den Zuordnungsregeln für die [SRowSet](srowset.md) -Struktur unter Verwendung eines einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) -Aufrufs für die einzelnen Elementarrays und-Strukturen gefolgt sein.</span><span class="sxs-lookup"><span data-stu-id="0e354-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="0e354-120">Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** -und **SRowSet** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="0e354-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e354-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="0e354-121">MFCMAPI reference</span></span>

<span data-ttu-id="0e354-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e354-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e354-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0e354-123">**File**</span></span>|<span data-ttu-id="0e354-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0e354-124">**Function**</span></span>|<span data-ttu-id="0e354-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0e354-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e354-126">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="0e354-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="0e354-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="0e354-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="0e354-128">MFCMAPI verwendet die **FreeProws** -Methode, um eine SRowSet-Struktur mit Zeilen der verarbeiteten Tabelle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0e354-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e354-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e354-129">See also</span></span>



[<span data-ttu-id="0e354-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0e354-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

