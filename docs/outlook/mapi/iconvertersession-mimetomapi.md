---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723033"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="72d80-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="72d80-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="72d80-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72d80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72d80-105">Konvertiert einen MIME-Datenstrom an einem MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="72d80-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="72d80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72d80-106">Parameters</span></span>

 <span data-ttu-id="72d80-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="72d80-107">_pstm_</span></span>
  
> <span data-ttu-id="72d80-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle in eine MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="72d80-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="72d80-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="72d80-109">_pmsg_</span></span>
  
> <span data-ttu-id="72d80-110">[out] Zeiger auf die Meldung geladen werden.</span><span class="sxs-lookup"><span data-stu-id="72d80-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="72d80-111">Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs.</span><span class="sxs-lookup"><span data-stu-id="72d80-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="72d80-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="72d80-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="72d80-113">[in] Dieser Wert muss **null**sein.</span><span class="sxs-lookup"><span data-stu-id="72d80-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="72d80-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72d80-114">_ulFlags_</span></span>
  
> <span data-ttu-id="72d80-115">[in] Dieser Parameter identifiziert eine spezielle Aktion während der Konvertierung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="72d80-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="72d80-116">Es muss null (0), wenn keine bestimmte Aktion ausgeführt werden soll, oder eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="72d80-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="72d80-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="72d80-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="72d80-118">Informationen gesendet/nicht gesendet wird dauerhaft in X nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="72d80-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="72d80-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="72d80-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="72d80-120">Der MIME-Stream ist für eine Nachricht Simple MAPI-Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="72d80-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="72d80-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="72d80-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="72d80-122">BCC-Empfänger des MIME-Streams sollte in der MAPI-Nachricht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="72d80-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="72d80-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="72d80-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="72d80-124">Der HTML-Textkörper des MIME-Streams sollte auf Rich Text Format (RTF) in der MAPI-Nachricht konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="72d80-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="72d80-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="72d80-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="72d80-126">Der Konverter sollte den MIME-Stream als internationale Nachricht (EAI/RFC6530) behandeln.</span><span class="sxs-lookup"><span data-stu-id="72d80-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="72d80-127">In Outlook 2013 unterstützt nicht.</span><span class="sxs-lookup"><span data-stu-id="72d80-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72d80-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72d80-128">Return value</span></span>

<span data-ttu-id="72d80-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="72d80-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="72d80-130">Gibt an, dass _Pstm_ **null ist**, _Pmsg_ **null ist**oder _UlFlags_ ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="72d80-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="72d80-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72d80-131">Remarks</span></span>

<span data-ttu-id="72d80-132">Wenn Sie **CCSF_USE_RTF** als Teil des _UlFlags_ angegeben haben, und der Nachricht Zielspeicher HTML- und RTF unterstützt, wird die MAPI-Nachricht in HTML oder RTF konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="72d80-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="72d80-133">Wenn die Nachricht in RTF konvertiert wird, wird das Format der konvertierte komprimiert RTF, HTML-Code wird in der komprimierten RTF-Zeichenfolge eingebettet werden, und die Zeichenfolge wird in der [PidTagRtfCompressed kanonische-Eigenschaft](pidtagrtfcompressed-canonical-property.md)enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="72d80-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72d80-134">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="72d80-134">MFCMAPI reference</span></span>

<span data-ttu-id="72d80-135">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="72d80-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72d80-136">**Datei**</span><span class="sxs-lookup"><span data-stu-id="72d80-136">**File**</span></span>|<span data-ttu-id="72d80-137">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="72d80-137">**Function**</span></span>|<span data-ttu-id="72d80-138">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="72d80-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72d80-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="72d80-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="72d80-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="72d80-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="72d80-141">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="72d80-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="72d80-142">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="72d80-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="72d80-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="72d80-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="72d80-144">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="72d80-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72d80-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72d80-145">See also</span></span>



[<span data-ttu-id="72d80-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72d80-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="72d80-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="72d80-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="72d80-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="72d80-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="72d80-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="72d80-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="72d80-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="72d80-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="72d80-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="72d80-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="72d80-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="72d80-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="72d80-153">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="72d80-153">MAPI Constants</span></span>](mapi-constants.md)

