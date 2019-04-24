---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325774"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="5abe4-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="5abe4-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="5abe4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5abe4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5abe4-105">Dekomprimiert den Textkörper einer e-Mail-Nachricht im komprimierten Rich-Text-Format (RTF), gibt das Format des dekomprimierten Streams an, konvertiert optional den dekomprimierten Stream in das systemeigene Format und gibt entweder den dekomprimierten Stream oder den konvertierter systemeigener Stream.</span><span class="sxs-lookup"><span data-stu-id="5abe4-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5abe4-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5abe4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5abe4-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="5abe4-107">Exported by:</span></span>  <br/> |<span data-ttu-id="5abe4-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="5abe4-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="5abe4-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5abe4-109">Called by:</span></span>  <br/> |<span data-ttu-id="5abe4-110">Client</span><span class="sxs-lookup"><span data-stu-id="5abe4-110">Client</span></span>  <br/> |
|<span data-ttu-id="5abe4-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5abe4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5abe4-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="5abe4-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="5abe4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5abe4-113">Parameters</span></span>

<span data-ttu-id="5abe4-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="5abe4-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="5abe4-115">in Dies ist ein Zeiger auf einen Stream, der für die [kanonische PidTagRtfCompressed-Eigenschaft](pidtagrtfcompressed-canonical-property.md) einer Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5abe4-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="5abe4-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="5abe4-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="5abe4-117">in Dies ist ein Zeiger auf eine</span><span class="sxs-lookup"><span data-stu-id="5abe4-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="5abe4-118">[RTF_WCSINFO](rtf_wcsinfo.md) -Struktur, die Optionen für die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="5abe4-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="5abe4-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="5abe4-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="5abe4-120">Out Dies ist ein Zeiger auf den Speicherort, an dem ein Stream für das dekomprimierte RTF-Objekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5abe4-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="5abe4-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="5abe4-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="5abe4-122">Out Dies ist ein Zeiger auf eine [RTF_WCSRETINFO](rtf_wcsretinfo.md) -Struktur, die Informationen zum Format des zurückgegebenen dekomprimierten Streams enthält.</span><span class="sxs-lookup"><span data-stu-id="5abe4-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5abe4-123">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5abe4-123">Return values</span></span>

<span data-ttu-id="5abe4-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5abe4-124">S_OK</span></span> 
  
- <span data-ttu-id="5abe4-125">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5abe4-125">The function call is successful.</span></span>
    
<span data-ttu-id="5abe4-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5abe4-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="5abe4-127">Dieser Wert wird zurückgegeben, wenn das **MAPI_NATIVE_BODY** -Flag mit dem **MAPI_MODIFY** -Flag im **ulFlags** -Feld der **RTF_WCSINFO** -Struktur kombiniert wird, auf die von *pWCSInfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5abe4-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5abe4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5abe4-128">Remarks</span></span>

<span data-ttu-id="5abe4-129">**WrapCompressedRTFStreamEx** ermöglicht den Zugriff auf den Textkörper einer e-Mail-Nachricht, die in komprimiertem RTF gekapselt ist, indem der Datenstrom dekomprimiert wird, der dekomprimierte Stream und sein Format sowie optional der systemeigene Textstream zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5abe4-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="5abe4-130">Der systemeigene Textstream kann in RTF, nur-Text oder HTML sein.</span><span class="sxs-lookup"><span data-stu-id="5abe4-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="5abe4-131">Das Microsoft Office Outlook-Objektmodell stellt eine **Body** -Eigenschaft für MailItem-Objekte und eine MailItem [. BodyFormat-Eigenschaft (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) bereit, die das Format des Textkörpers angibt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5abe4-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="5abe4-132">Eine Lösung, die von Outlook nicht als vertrauenswürdig eingestuft wird, ruft Sicherheitsdialogfelder auf, die vom Outlook-Sicherheitsdienst generiert werden.</span><span class="sxs-lookup"><span data-stu-id="5abe4-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="5abe4-133">Die Verwendung der exportierten MAPI-Funktion **WrapCompressedRTFStreamEx** ermöglicht es einer Lösung, MAPI anstelle des Outlook-Objektmodells zu verwenden und diese Sicherheitsdialogfelder zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="5abe4-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="5abe4-134">Da das **MAPI\_-NATIVE_BODY** -Flag nicht mit dem **MAPI\_-Änderungs** Kennzeichen im **ulFlags** -Feld der **RTF\_-WCSINFO** -Struktur kombiniert werden kann, auf die von *pWCSInfo*verwiesen wird, können Sie nur auf die systemeigene Textstream im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="5abe4-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="5abe4-135">Verwenden Sie die **WrapCompressedRTFStream** -Funktion, um auf den systemeigenen Textstream im Lese-/Schreibzugriff zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5abe4-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5abe4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5abe4-136">See also</span></span>

- [<span data-ttu-id="5abe4-137">Abrufen des Textkörpers einer Nachricht im komprimierten RTF und konvertieren in das systemeigene Format</span><span class="sxs-lookup"><span data-stu-id="5abe4-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

