---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325774"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="2b4bd-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="2b4bd-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="2b4bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b4bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b4bd-105">Dekomprimiert den Textkörper einer E-Mail-Nachricht im komprimierten Rich Text Format (RTF), gibt das Format des dekomprimierten Datenstroms an, konvertiert optional den dekomprimierten Datenstrom in sein systemeigenes Format und gibt entweder den dekomprimierten Datenstrom oder den konvertierten systemeigenen Datenstrom zurück.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2b4bd-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2b4bd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b4bd-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="2b4bd-107">Exported by:</span></span>  <br/> |<span data-ttu-id="2b4bd-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="2b4bd-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2b4bd-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2b4bd-109">Called by:</span></span>  <br/> |<span data-ttu-id="2b4bd-110">Client</span><span class="sxs-lookup"><span data-stu-id="2b4bd-110">Client</span></span>  <br/> |
|<span data-ttu-id="2b4bd-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2b4bd-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2b4bd-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="2b4bd-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="2b4bd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b4bd-113">Parameters</span></span>

<span data-ttu-id="2b4bd-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="2b4bd-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="2b4bd-115">[in] Dies ist ein Zeiger auf einen Datenstrom, der in der [kanonischen Eigenschaft PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) einer Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="2b4bd-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="2b4bd-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="2b4bd-117">[in] Dies ist ein Zeiger auf eine</span><span class="sxs-lookup"><span data-stu-id="2b4bd-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="2b4bd-118">[RTF_WCSINFO,](rtf_wcsinfo.md) die Optionen für die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="2b4bd-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="2b4bd-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="2b4bd-120">[out] Dies ist ein Zeiger auf den Speicherort, an dem ein Datenstrom für die dekomprimierte RTF zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="2b4bd-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="2b4bd-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="2b4bd-122">[out] Dies ist ein Zeiger auf [eine RTF_WCSRETINFO,](rtf_wcsretinfo.md) die Informationen zum Format des zurückgegebenen dekomprimierten Datenstroms enthält.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2b4bd-123">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2b4bd-123">Return values</span></span>

<span data-ttu-id="2b4bd-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b4bd-124">S_OK</span></span> 
  
- <span data-ttu-id="2b4bd-125">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-125">The function call is successful.</span></span>
    
<span data-ttu-id="2b4bd-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b4bd-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="2b4bd-127">Dies wird zurückgegeben, wenn **das MAPI_NATIVE_BODY-Flag** mit dem **flag MAPI_MODIFY** im **ulFlags-Feld** der **RTF_WCSINFO-Struktur** kombiniert wird, auf die von *pWCSInfo verwiesen wird.*</span><span class="sxs-lookup"><span data-stu-id="2b4bd-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2b4bd-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b4bd-128">Remarks</span></span>

<span data-ttu-id="2b4bd-129">**Mit WrapCompressedRTFStreamEx** können Sie auf den Textkörper einer E-Mail-Nachricht zugreifen, die in komprimiertem RTF gekapselt ist, indem Sie den Datenstrom dekomprimieren, den dekomprimierten Datenstrom und dessen Format sowie optional den systemeigenen Textdatenstrom zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="2b4bd-130">Der systemeigene Textdatenstrom kann in RTF, Nur-Text oder HTML enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="2b4bd-131">Das Microsoft Office Outlook-Objektmodell stellt eine **Body-Eigenschaft** für **MailItem-Objekte** und eine [MailItem.BodyFormat-Eigenschaft (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) zur Verfügung, die das Format des Textkörpers angibt.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="2b4bd-132">Eine Lösung, die von Outlook nicht als vertrauenswürdig eingestuft wird, ruft standardmäßig sicherheitsdialogfelder auf, die von Outlook Security Guard generiert werden.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="2b4bd-133">Mithilfe der exportierten MAPI-Funktion **WrapCompressedRTFStreamEx** kann eine Lösung MAPI anstelle des Outlook-Objektmodells verwenden und diese Sicherheitsdialogfelder vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="2b4bd-134">Da das **\_ MAPI-NATIVE_BODY-Flag** nicht mit dem **MAPI \_ MODIFY-Flag** im **ulFlags-Feld** der **RTF \_ WCSINFO-Struktur** kombiniert werden kann, auf die *pWCSInfo* verweist, können Sie nur im schreibgeschützten Modus auf den systemeigenen Textdatenstrom zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="2b4bd-135">Zum Zugreifen auf den systemeigenen Textdatenstrom im Lese-/Schreibmodus sollten Sie die **WrapCompressedRTFStream-Funktion** verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b4bd-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b4bd-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b4bd-136">See also</span></span>

- [<span data-ttu-id="2b4bd-137">Abrufen des Textkörpers einer Nachricht in komprimiertem RTF und Konvertieren in das systemeigene Format</span><span class="sxs-lookup"><span data-stu-id="2b4bd-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

