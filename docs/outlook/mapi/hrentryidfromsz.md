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
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437728"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="65a2f-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="65a2f-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="65a2f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65a2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65a2f-105">Erstellt eine Eintrags-ID aus der ASCII-Codierung.</span><span class="sxs-lookup"><span data-stu-id="65a2f-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65a2f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="65a2f-106">Header file:</span></span>  <br/> |<span data-ttu-id="65a2f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="65a2f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="65a2f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="65a2f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="65a2f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="65a2f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="65a2f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="65a2f-110">Called by:</span></span>  <br/> |<span data-ttu-id="65a2f-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="65a2f-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="65a2f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="65a2f-112">Parameters</span></span>

 <span data-ttu-id="65a2f-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="65a2f-113">_sz_</span></span>
  
> <span data-ttu-id="65a2f-114">in Zeiger auf die ASCII-Zeichenfolge, aus der ein Eintragsbezeichner erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="65a2f-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="65a2f-115">_PCB_</span><span class="sxs-lookup"><span data-stu-id="65a2f-115">_pcb_</span></span>
  
> <span data-ttu-id="65a2f-116">Out Zeiger auf die Größe der Eintrags-ID, auf die durch den _ppentry_ -Parameter verwiesen wird, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="65a2f-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="65a2f-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="65a2f-117">_ppentry_</span></span>
  
> <span data-ttu-id="65a2f-118">Out Zeiger auf einen Zeiger auf die zurück [](entryid.md) geGebene Eintrags-ID-Struktur, die den neuen Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="65a2f-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="65a2f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65a2f-119">Return value</span></span>

<span data-ttu-id="65a2f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="65a2f-120">S_OK</span></span>
  
> <span data-ttu-id="65a2f-121">Die Erholung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="65a2f-121">The recreation was successful.</span></span>
    
<span data-ttu-id="65a2f-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="65a2f-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="65a2f-123">Die Eintrags-ID war ungültig.</span><span class="sxs-lookup"><span data-stu-id="65a2f-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65a2f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65a2f-124">Remarks</span></span>

<span data-ttu-id="65a2f-125">Die **HrEntryIDFromSz** -und [HrSzFromEntryID](hrszfromentryid.md) -Funktionen ermöglichen die Konvertierung zwischen den Zeichenfolgen-und Binärformaten der Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="65a2f-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="65a2f-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="65a2f-126">Notes to callers</span></span>

<span data-ttu-id="65a2f-127">Die **HrEntryIDFromSz** -Funktion reserviert Speicher für die ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="65a2f-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

