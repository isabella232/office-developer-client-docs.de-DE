---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325627"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="dc3d3-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="dc3d3-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="dc3d3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc3d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc3d3-105">Erstellt einen Textstream im unkomprimierten Rich-Text-Format (RTF) aus dem komprimierten Format, das in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc3d3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dc3d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc3d3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dc3d3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dc3d3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dc3d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc3d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc3d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc3d3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dc3d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc3d3-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="dc3d3-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="dc3d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc3d3-112">Parameters</span></span>

 <span data-ttu-id="dc3d3-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="dc3d3-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="dc3d3-114">in Zeiger auf einen Stream, der für die PR_RTF_COMPRESSED-Eigenschaft einer Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="dc3d3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc3d3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="dc3d3-116">in Bitmaske von Options-Flags für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="dc3d3-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dc3d3-117">The following flags can be set:</span></span>
    
<span data-ttu-id="dc3d3-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dc3d3-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="dc3d3-119">Gibt an, ob der Client die eingebundene Datenstromschnittstelle lesen oder schreiben möchte, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="dc3d3-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="dc3d3-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="dc3d3-121">Unkomprimiertes RTF sollte in den Stream geschrieben werden, auf den durch _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="dc3d3-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="dc3d3-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="dc3d3-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="dc3d3-123">Out Zeiger auf die Position, an der **WrapCompressedRTFStream** einen Stream für das unkomprimiert RTF zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc3d3-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc3d3-124">Return value</span></span>

<span data-ttu-id="dc3d3-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc3d3-125">S_OK</span></span> 
  
> <span data-ttu-id="dc3d3-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc3d3-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc3d3-127">Remarks</span></span>

<span data-ttu-id="dc3d3-128">Wenn das MAPI_MODIFY-Flag im _ulFlags_ -Parameter übergeben wird, muss der _lpCompressedRTFStream_ -Parameter bereits zum Lesen und Schreiben geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="dc3d3-129">Neuer, nicht komprimierter RTF-Text sollte in die in _lpUncompressedRTFStream_zurückgegebene Stream-Schnittstelle geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="dc3d3-130">Da der vorhandene Stream nicht angefügt werden kann, muss der gesamte Nachrichtentext geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="dc3d3-131">Wenn NULL im _ulFlags_ -Parameter übergeben wird, kann _lpCompressedRTFStream_ schreibgeschützt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="dc3d3-132">Nur der gesamte Nachrichtentext kann aus der in _lpUncompressedRTFStream_zurückgegebenen Stream-Schnittstelle ausgelesen werden.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="dc3d3-133">Es ist nicht möglich, in der Mitte des Streams zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="dc3d3-134">**WrapCompressedRTFStream** geht davon aus, dass der Zeiger des komprimierten Streams auf den Anfang des Streams festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="dc3d3-135">Bestimmte OLE **IStream** -Methoden werden vom zurückgegebenen unkomprimierten Stream nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="dc3d3-136">Hierzu gehört **IStream:: Clone**, **IStream**:: LockRegion, **IStream:: Revert**, **IStream:: Seek**, **IStream:: SetSize**, **IStream:: stat**und **IStream:: UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="dc3d3-137">Zum Kopieren in den gesamten Stream ist eine Read/Write-Schleife erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="dc3d3-138">Da der Client neues RTF im unkomprimierten Format schreibt, sollte es **WrapCompressedRTFStream**verwenden, statt direkt in den Stream zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="dc3d3-139">RTF-fähige Clients sollten in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft nach dem STORE_UNCOMPRESSED_RTF-Flag suchen und es an **WrapCompressed RTFStream** weitergeben, wenn es festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc3d3-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc3d3-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc3d3-140">See also</span></span>



[<span data-ttu-id="dc3d3-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="dc3d3-141">RTFSync</span></span>](rtfsync.md)

