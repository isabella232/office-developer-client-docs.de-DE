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
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791937"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="d1dc0-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="d1dc0-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="d1dc0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1dc0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1dc0-105">Eine Eintrags-ID codiert in eine ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1dc0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d1dc0-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1dc0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d1dc0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d1dc0-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d1dc0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d1dc0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d1dc0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d1dc0-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d1dc0-110">Called by:</span></span>  <br/> |<span data-ttu-id="d1dc0-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="d1dc0-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="d1dc0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1dc0-112">Parameters</span></span>

 <span data-ttu-id="d1dc0-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="d1dc0-113">_cb_</span></span>
  
> <span data-ttu-id="d1dc0-114">[in] Größe des Eintrags-ID, die auf das durch den Parameter _Pentry_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="d1dc0-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="d1dc0-115">_pentry_</span></span>
  
> <span data-ttu-id="d1dc0-116">[in] Zeiger auf eine [ENTRYID](entryid.md) -Struktur, die Eintrags-ID zu codierenden enthält.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="d1dc0-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="d1dc0-117">_psz_</span></span>
  
> <span data-ttu-id="d1dc0-118">[out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1dc0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1dc0-119">Return value</span></span>

<span data-ttu-id="d1dc0-120">None.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1dc0-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1dc0-121">Remarks</span></span>

<span data-ttu-id="d1dc0-122">Die Funktionen [HrEntryIDFromSz](hrentryidfromsz.md) und **HrSzFromEntryID** bieten eine Konvertierung zwischen der Zeichenfolge und der binären Formate der Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="d1dc0-123">Mit MAPI sollten Sie die Strukturen mit Binärdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1dc0-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d1dc0-124">Notes to callers</span></span>

<span data-ttu-id="d1dc0-125">Die **HrSzFromEntryID** -Funktion weist Speicher für die Verwendung der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1dc0-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

