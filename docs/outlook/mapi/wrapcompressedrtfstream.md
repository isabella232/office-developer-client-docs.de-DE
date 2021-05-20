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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439800"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="b297d-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="b297d-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="b297d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b297d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b297d-105">Erstellt einen Textdatenstrom im unkomprimierten Rich Text Format (RTF) aus dem komprimierten Format, das in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b297d-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b297d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b297d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b297d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b297d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b297d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b297d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b297d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b297d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b297d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b297d-110">Called by:</span></span>  <br/> |<span data-ttu-id="b297d-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="b297d-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="b297d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b297d-112">Parameters</span></span>

 <span data-ttu-id="b297d-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="b297d-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="b297d-114">[in] Zeiger auf einen Datenstrom, der auf der PR_RTF_COMPRESSED einer Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b297d-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="b297d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b297d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b297d-116">[in] Bitmaske von Optionskennzeichen für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="b297d-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="b297d-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b297d-117">The following flags can be set:</span></span>
    
<span data-ttu-id="b297d-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b297d-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b297d-119">Gibt an, ob der Client die zurückgegebene umschlossene Streamschnittstelle lesen oder schreiben möchte.</span><span class="sxs-lookup"><span data-stu-id="b297d-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="b297d-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="b297d-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="b297d-121">Nicht komprimiertes RTF sollte in den Datenstrom geschrieben werden, auf den  _lpCompressedRTFStream verweist_</span><span class="sxs-lookup"><span data-stu-id="b297d-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="b297d-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="b297d-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="b297d-123">[out] Zeiger auf den Speicherort, an dem **WrapCompressedRTFStream** einen Datenstrom für die nicht komprimierte RTF zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b297d-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b297d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b297d-124">Return value</span></span>

<span data-ttu-id="b297d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="b297d-125">S_OK</span></span> 
  
> <span data-ttu-id="b297d-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b297d-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b297d-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b297d-127">Remarks</span></span>

<span data-ttu-id="b297d-128">Wenn das MAPI_MODIFY im  _ulFlags-Parameter_ übergeben wird, muss der  _lpCompressedRTFStream-Parameter_ bereits zum Lesen und Schreiben geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="b297d-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="b297d-129">Neuer, nicht komprimierter RTF-Text sollte in die stream-Schnittstelle geschrieben werden, die in _lpUncompressedRTFStream zurückgegeben wird._</span><span class="sxs-lookup"><span data-stu-id="b297d-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="b297d-130">Da das Anfügen des vorhandenen Datenstroms nicht möglich ist, muss der gesamte Nachrichtentext geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b297d-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="b297d-131">Wenn null im  _ulFlags-Parameter_ übergeben wird, wird  _lpCompressedRTFStream_ möglicherweise schreibgeschützt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b297d-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="b297d-132">Nur der gesamte Nachrichtentext kann aus der stream-Schnittstelle gelesen werden, die in _lpUncompressedRTFStream zurückgegeben wird._</span><span class="sxs-lookup"><span data-stu-id="b297d-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="b297d-133">Es ist nicht möglich, ab der Mitte des Datenstroms zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b297d-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="b297d-134">**WrapCompressedRTFStream** geht davon aus, dass der Zeiger des komprimierten Datenstroms auf den Anfang des Datenstroms festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b297d-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="b297d-135">Bestimmte OLE **IStream-Methoden** werden vom zurückgegebenen nicht komprimierten Datenstrom nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b297d-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="b297d-136">Dazu gehören **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** und **IStream::UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="b297d-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="b297d-137">Zum Kopieren in den gesamten Datenstrom ist eine Lese-/Schreibschleife erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b297d-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="b297d-138">Da der Client neue RTF im unkomprimierten Format schreibt, sollte er **WrapCompressedRTFStream** verwenden, anstatt direkt in den Datenstrom zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b297d-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="b297d-139">RTF-bewusste Clients sollten nach dem STORE_UNCOMPRESSED_RTF-Flag in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft suchen und es an **WrapCompressed RTFStream** übergeben, wenn es festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b297d-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b297d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b297d-140">See also</span></span>



[<span data-ttu-id="b297d-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="b297d-141">RTFSync</span></span>](rtfsync.md)

