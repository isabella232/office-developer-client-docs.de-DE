---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a524a7eb40c33d6de2f64cd5373c9a39a8a1e3df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565298"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="c0a4e-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="c0a4e-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="c0a4e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0a4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0a4e-105">Erstellt eine Eintrags-ID aus der ASCII-Codierung neu.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0a4e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c0a4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0a4e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c0a4e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c0a4e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c0a4e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0a4e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0a4e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0a4e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c0a4e-110">Called by:</span></span>  <br/> |<span data-ttu-id="c0a4e-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="c0a4e-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="c0a4e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0a4e-112">Parameters</span></span>

 <span data-ttu-id="c0a4e-113">_su_</span><span class="sxs-lookup"><span data-stu-id="c0a4e-113">_sz_</span></span>
  
> <span data-ttu-id="c0a4e-114">[in] Zeiger auf die ASCII-Zeichenfolge aus dem Eintrags-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="c0a4e-115">_PCB_</span><span class="sxs-lookup"><span data-stu-id="c0a4e-115">_pcb_</span></span>
  
> <span data-ttu-id="c0a4e-116">[out] Zeiger auf die Größe des Eintrags-ID, die auf das durch den Parameter _Ppentry_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="c0a4e-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="c0a4e-117">_ppentry_</span></span>
  
> <span data-ttu-id="c0a4e-118">[out] Zeiger auf einen Zeiger auf das zurückgegebene [ENTRYID](entryid.md) -Struktur, die neuen Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0a4e-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c0a4e-119">Return value</span></span>

<span data-ttu-id="c0a4e-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0a4e-120">S_OK</span></span>
  
> <span data-ttu-id="c0a4e-121">Erneutes Erstellen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-121">The recreation was successful.</span></span>
    
<span data-ttu-id="c0a4e-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c0a4e-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="c0a4e-123">Die Eintrags-ID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0a4e-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c0a4e-124">Remarks</span></span>

<span data-ttu-id="c0a4e-125">Die Funktionen **HrEntryIDFromSz** und [HrSzFromEntryID](hrszfromentryid.md) bieten eine Konvertierung zwischen der Zeichenfolge und der binären Formate der Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0a4e-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c0a4e-126">Notes to callers</span></span>

<span data-ttu-id="c0a4e-127">Die **HrEntryIDFromSz** -Funktion weist Speicher für die Verwendung der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c0a4e-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

