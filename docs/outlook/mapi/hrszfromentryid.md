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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346417"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="8ca15-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="8ca15-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="8ca15-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ca15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ca15-105">Codiert eine Eintrags-ID in eine ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8ca15-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ca15-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8ca15-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ca15-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8ca15-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8ca15-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8ca15-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ca15-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca15-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8ca15-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8ca15-110">Called by:</span></span>  <br/> |<span data-ttu-id="8ca15-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8ca15-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="8ca15-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ca15-112">Parameters</span></span>

 <span data-ttu-id="8ca15-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="8ca15-113">_cb_</span></span>
  
> <span data-ttu-id="8ca15-114">in Größe (in Bytes) der Eintrags-ID, auf die durch __ den Penty-Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8ca15-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="8ca15-115">_Pentry_</span><span class="sxs-lookup"><span data-stu-id="8ca15-115">_pentry_</span></span>
  
> <span data-ttu-id="8ca15-116">in Zeiger auf eine [Eintrags](entryid.md) -ID-Struktur, die den zu codierenden Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="8ca15-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="8ca15-117">_PSZ_</span><span class="sxs-lookup"><span data-stu-id="8ca15-117">_psz_</span></span>
  
> <span data-ttu-id="8ca15-118">Out Zeiger auf die zurückgegebene ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8ca15-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ca15-119">Return value</span><span class="sxs-lookup"><span data-stu-id="8ca15-119">Return value</span></span>

<span data-ttu-id="8ca15-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ca15-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ca15-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ca15-121">Remarks</span></span>

<span data-ttu-id="8ca15-122">Die [HrEntryIDFromSz](hrentryidfromsz.md) -und **HrSzFromEntryID** -Funktionen ermöglichen die Konvertierung zwischen den Zeichenfolgen-und Binärformaten der Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="8ca15-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="8ca15-123">Mit MAPI sollten Sie Strukturen mit Binärdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ca15-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8ca15-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8ca15-124">Notes to callers</span></span>

<span data-ttu-id="8ca15-125">Die **HrSzFromEntryID** -Funktion reserviert Speicher für die ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8ca15-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

