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
ms.openlocfilehash: 9025bcebdd5e656070b31cd82e6519166a3e3791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795873"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="dbc23-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="dbc23-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="dbc23-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbc23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbc23-105">Erstellt einen Textstream in nicht komprimierten Rich Text Format (RTF) aus der komprimierten Format in der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbc23-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbc23-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dbc23-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbc23-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dbc23-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dbc23-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dbc23-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbc23-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dbc23-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dbc23-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dbc23-110">Called by:</span></span>  <br/> |<span data-ttu-id="dbc23-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="dbc23-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="dbc23-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbc23-112">Parameters</span></span>

 <span data-ttu-id="dbc23-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="dbc23-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="dbc23-114">[in] Zeiger in ein Stream-Objekt auf die PR_RTF_COMPRESSED-Eigenschaft einer Nachricht geöffnet.</span><span class="sxs-lookup"><span data-stu-id="dbc23-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="dbc23-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dbc23-115">_ulFlags_</span></span>
  
> <span data-ttu-id="dbc23-116">[in] Bitmaske der Optionsflags für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="dbc23-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="dbc23-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dbc23-117">The following flags can be set:</span></span>
    
<span data-ttu-id="dbc23-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dbc23-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="dbc23-119">Gibt an, ob der Client beabsichtigt zum Lesen oder Schreiben der gepackten Stream-Schnittstelle, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dbc23-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="dbc23-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="dbc23-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="dbc23-121">Nicht komprimierten RTF sollte in das Stream-Objekt auf den _LpCompressedRTFStream_ geschrieben werden</span><span class="sxs-lookup"><span data-stu-id="dbc23-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="dbc23-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="dbc23-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="dbc23-123">[out] Zeiger auf den Speicherort, in dem **WrapCompressedRTFStream** einen Stream für die nicht komprimierten RTF zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dbc23-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dbc23-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbc23-124">Return value</span></span>

<span data-ttu-id="dbc23-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbc23-125">S_OK</span></span> 
  
> <span data-ttu-id="dbc23-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="dbc23-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbc23-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dbc23-127">Remarks</span></span>

<span data-ttu-id="dbc23-128">Wenn das Flag MAPI_MODIFY im _UlFlags_ -Parameter übergeben wird, muss der Parameter _LpCompressedRTFStream_ bereits zum Lesen und Schreiben geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="dbc23-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="dbc23-129">Neue, nicht komprimierten RTF-Text sollte in die Benutzeroberfläche der Stream-Objekt zurückgegeben, die in _LpUncompressedRTFStream_geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dbc23-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="dbc23-130">Da es nicht möglich, den vorhandenen Stream anzufügen ist, muss der gesamte Nachrichtentext geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dbc23-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="dbc23-131">Wenn 0 (null) im _UlFlags_ -Parameter übergeben wird, kann dann _LpCompressedRTFStream_ schreibgeschützt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="dbc23-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="dbc23-132">Nur der gesamte Nachrichtentext kann über die Stream-Schnittstelle, die in _LpUncompressedRTFStream_zurückgegeben gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="dbc23-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="dbc23-133">Es ist nicht möglich, den Suchvorgang starten der Mitte des Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbc23-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="dbc23-134">**WrapCompressedRTFStream** wird davon ausgegangen, dass die komprimierte Stream Zeiger an den Anfang des Datenstroms festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dbc23-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="dbc23-135">Bestimmte OLE **IStream** -Methoden werden von der nicht komprimierten zurückgegebene Stream nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbc23-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="dbc23-136">**IStream:: Clone**, **:: LockRegion**, **:: Revert**, **IStream:: Seek**, **:: setSize**, **:: Stat**und **:: UnlockRegion**beinhalten.</span><span class="sxs-lookup"><span data-stu-id="dbc23-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="dbc23-137">Um den gesamten Datenstrom zu kopieren, wird eine Schleife Lese-/Schreibzugriff benötigt.</span><span class="sxs-lookup"><span data-stu-id="dbc23-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="dbc23-138">Da der Client nicht komprimierten Format neue RTF schreibt, sollte **WrapCompressedRTFStream**, anstatt direkt an den Stream schreiben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbc23-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="dbc23-139">RTF-fähigen Clients sollte das Flag STORE_UNCOMPRESSED_RTF in der Eigenschaft **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) suchen und übergeben es an **WrapCompressed RTFStream** , wenn sie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dbc23-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbc23-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbc23-140">See also</span></span>



[<span data-ttu-id="dbc23-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="dbc23-141">RTFSync</span></span>](rtfsync.md)

