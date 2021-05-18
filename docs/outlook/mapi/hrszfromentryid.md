---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411554"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="6bf20-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="6bf20-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="6bf20-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bf20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bf20-105">Codiert einen Eintragsbezeichner in eine ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6bf20-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bf20-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6bf20-106">Header file:</span></span>  <br/> |<span data-ttu-id="6bf20-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6bf20-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6bf20-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6bf20-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6bf20-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6bf20-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6bf20-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6bf20-110">Called by:</span></span>  <br/> |<span data-ttu-id="6bf20-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="6bf20-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="6bf20-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bf20-112">Parameters</span></span>

 <span data-ttu-id="6bf20-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="6bf20-113">_cb_</span></span>
  
> <span data-ttu-id="6bf20-114">[in] Größe des Eintragsbezeichners in Bytes, auf den der  _Pentry-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="6bf20-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="6bf20-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="6bf20-115">_pentry_</span></span>
  
> <span data-ttu-id="6bf20-116">[in] Zeiger auf eine [ENTRYID-Struktur,](entryid.md) die die zu codierte Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="6bf20-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="6bf20-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="6bf20-117">_psz_</span></span>
  
> <span data-ttu-id="6bf20-118">[out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6bf20-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6bf20-119">Return value</span><span class="sxs-lookup"><span data-stu-id="6bf20-119">Return value</span></span>

<span data-ttu-id="6bf20-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="6bf20-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6bf20-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6bf20-121">Remarks</span></span>

<span data-ttu-id="6bf20-122">Die [Funktionen HrEntryIDFromSz](hrentryidfromsz.md) und **HrSzFromEntryID** stellen eine Konvertierung zwischen den Zeichenfolgen- und Binärformaten von Eintragsbezeichnern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6bf20-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="6bf20-123">Bei MAPI sollten Sie Strukturen mit Binärdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="6bf20-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6bf20-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6bf20-124">Notes to callers</span></span>

<span data-ttu-id="6bf20-125">Die **HrSzFromEntryID-Funktion** weist der ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer-Funktion Arbeitsspeicher](mapiallocatebuffer.md) zu.</span><span class="sxs-lookup"><span data-stu-id="6bf20-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

