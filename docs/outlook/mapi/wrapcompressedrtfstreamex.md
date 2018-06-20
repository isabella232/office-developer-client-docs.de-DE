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
ms.openlocfilehash: bdb879a2412c817b7b314cd7bf6de1fa4c9f40d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795851"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="044e3-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="044e3-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="044e3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="044e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="044e3-105">Dekomprimiert die der Textkörper einer e-Mail-Nachricht, die im komprimierten Rich Text Format (RTF), gibt das Format an den dekomprimierten Stream-Objekts, optional konvertiert den dekomprimierten Datenstrom in seinem nativen Format und gibt entweder den dekomprimierten Stream oder die systemeigene Datenstrom konvertiert.</span><span class="sxs-lookup"><span data-stu-id="044e3-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="044e3-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="044e3-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="044e3-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="044e3-107">Exported by:</span></span>  <br/> |<span data-ttu-id="044e3-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="044e3-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="044e3-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="044e3-109">Called by:</span></span>  <br/> |<span data-ttu-id="044e3-110">Client</span><span class="sxs-lookup"><span data-stu-id="044e3-110">Client</span></span>  <br/> |
|<span data-ttu-id="044e3-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="044e3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="044e3-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="044e3-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="044e3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="044e3-113">Parameters</span></span>

<span data-ttu-id="044e3-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="044e3-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="044e3-115">[in] Dies ist ein Zeiger auf ein Datenstrom, der für die [Kanonische PidTagRtfCompressed-Eigenschaft](pidtagrtfcompressed-canonical-property.md) einer Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="044e3-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="044e3-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="044e3-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="044e3-117">[in] Hierbei handelt es sich um einen Zeiger auf eine</span><span class="sxs-lookup"><span data-stu-id="044e3-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="044e3-118">[RTF_WCSINFO](rtf_wcsinfo.md) -Struktur, die Optionen für die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="044e3-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="044e3-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="044e3-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="044e3-120">[out] Dies ist ein Zeiger auf den Speicherort, an ein Stream für die dekomprimierten RTF zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="044e3-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="044e3-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="044e3-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="044e3-122">[out] Dies ist ein Zeiger auf eine [RTF_WCSRETINFO](rtf_wcsretinfo.md) -Struktur, die Informationen zum Format der zurückgegebenen dekomprimierten Stream-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="044e3-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="044e3-123">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="044e3-123">Return values</span></span>

<span data-ttu-id="044e3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="044e3-124">S_OK</span></span> 
  
- <span data-ttu-id="044e3-125">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="044e3-125">The function call is successful.</span></span>
    
<span data-ttu-id="044e3-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="044e3-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="044e3-127">Dies wird zurückgegeben, wenn das Flag **MAPI_NATIVE_BODY** mit dem **MAPI_MODIFY** -Flag im Feld **UlFlags** der Struktur **RTF_WCSINFO** an, auf das *pWCSInfo* zeigt kombiniert ist.</span><span class="sxs-lookup"><span data-stu-id="044e3-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="044e3-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="044e3-128">Remarks</span></span>

<span data-ttu-id="044e3-129">**WrapCompressedRTFStreamEx** ermöglicht den Zugriff auf den Textkörper einer e-Mail-Nachricht in komprimierten RTF Dekomprimieren des Streams gekapselten der dekomprimierten Stream und das Format und optional die systemeigene Textstream zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="044e3-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="044e3-130">Die systemeigene Textstream kann in RTF, nur-Text oder HTML sein.</span><span class="sxs-lookup"><span data-stu-id="044e3-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="044e3-131">Microsoft Office Outlook-Objektmodell enthält eine **Body** -Eigenschaft für **MailItem** -Objekten und einer [Der MailItem.BodyFormat-Eigenschaft (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) , der das Format des Textkörpers angibt.</span><span class="sxs-lookup"><span data-stu-id="044e3-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="044e3-132">Entwurfsbedingt Ruft eine Lösung, die von Outlook nicht vertrauenswürdig ist Sicherheit Dialogfelder von Outlook-Sicherheitspersonals generiert.</span><span class="sxs-lookup"><span data-stu-id="044e3-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="044e3-133">Verwenden der exportierten MAPI-Funktion **WrapCompressedRTFStreamEx** ermöglicht eine Lösung für MAPI anstelle von Outlook-Objektmodell verwenden und diese Sicherheitsdialogfelder zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="044e3-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="044e3-134">Da die **MAPI\_NATIVE_BODY** Flag kombiniert werden die **MAPI\_ändern** -Kennzeichen in das Feld **UlFlags** von der **RTF\_WCSINFO** Struktur an, auf zeigt *pWCSInfo*, Sie können nur zugreifen, die systemeigene Textkörper-Datenstrom im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="044e3-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="044e3-135">Um die systemeigene Textstream im Lese-/Schreibmodus zuzugreifen, sollten Sie die **WrapCompressedRTFStream** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="044e3-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="044e3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="044e3-136">See also</span></span>

- [<span data-ttu-id="044e3-137">Abrufen von den Textkörper einer Nachricht im RTF komprimierte und konvertieren Sie es in seinem nativen Format</span><span class="sxs-lookup"><span data-stu-id="044e3-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

