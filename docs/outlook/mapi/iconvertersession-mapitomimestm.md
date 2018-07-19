---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Zuletzt geändert: 20 September 2017'
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792030"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="89e9e-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="89e9e-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="89e9e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89e9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89e9e-105">Konvertiert eine MAPI-Nachricht in einen MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="89e9e-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="89e9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89e9e-106">Parameters</span></span>

 <span data-ttu-id="89e9e-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="89e9e-107">_pmsg_</span></span>
  
> <span data-ttu-id="89e9e-108">[in] Zeiger auf die Nachricht zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="89e9e-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="89e9e-109">Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs.</span><span class="sxs-lookup"><span data-stu-id="89e9e-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="89e9e-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="89e9e-110">_pstm_</span></span>
  
> <span data-ttu-id="89e9e-111">[out] [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Schnittstelle an den Stream ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="89e9e-111">[out] [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="89e9e-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89e9e-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="89e9e-113">[in] Flags, die für den Konverter bestimmte Aktionen angeben:</span><span class="sxs-lookup"><span data-stu-id="89e9e-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="89e9e-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="89e9e-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="89e9e-115">Der Konverter sollte 8-Bit-Kopfzeilen zulassen.</span><span class="sxs-lookup"><span data-stu-id="89e9e-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="89e9e-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="89e9e-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="89e9e-117">Informationen gesendet/nicht gesendet wird dauerhaft in X nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="89e9e-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="89e9e-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="89e9e-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="89e9e-119">Der Konverter sollte eine internationale Nachricht (EAI/RFC6530) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="89e9e-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="89e9e-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="89e9e-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="89e9e-121">BCC-Empfänger der Nachricht MAPI sollte im MIME-Datenstrom enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89e9e-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="89e9e-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="89e9e-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="89e9e-123">Nehmen Sie Nachrichten-Id-Feld nicht in ausgehenden Nachrichten aus.</span><span class="sxs-lookup"><span data-stu-id="89e9e-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="89e9e-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="89e9e-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="89e9e-125">Der Konverter sollten die Kopfzeilen der äußeren Nachricht ignorieren.</span><span class="sxs-lookup"><span data-stu-id="89e9e-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="89e9e-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="89e9e-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="89e9e-127">Der Konverter sollte nur nur-Text senden.</span><span class="sxs-lookup"><span data-stu-id="89e9e-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="89e9e-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="89e9e-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="89e9e-129">Der Konverter ist eine SMTP-Nachricht übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="89e9e-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="89e9e-130">Dieses Kennzeichen müssen immer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="89e9e-130">This flag must always be set.</span></span>
    
<span data-ttu-id="89e9e-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="89e9e-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="89e9e-132">Der Konverter sollten aus HTML-Code der MIME-Nachricht im RTF-Format konvertieren.</span><span class="sxs-lookup"><span data-stu-id="89e9e-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="89e9e-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="89e9e-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="89e9e-134">Der Konverter sollten Transport Neutral Encapsulation Format (TNEF) Format der MIME-Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="89e9e-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="89e9e-135">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="89e9e-135">Return values</span></span>

<span data-ttu-id="89e9e-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="89e9e-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="89e9e-137">Ungültige Flags übergeben wurden, oder *Pmsg* oder *Pstm* ist NULL.</span><span class="sxs-lookup"><span data-stu-id="89e9e-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="89e9e-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89e9e-138">Remarks</span></span>

<span data-ttu-id="89e9e-139">Nur für Outlook-Nachricht Standardtypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89e9e-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="89e9e-140">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="89e9e-140">MFCMAPI reference</span></span>

<span data-ttu-id="89e9e-141">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="89e9e-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89e9e-142">**Datei**</span><span class="sxs-lookup"><span data-stu-id="89e9e-142">**File**</span></span>|<span data-ttu-id="89e9e-143">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="89e9e-143">**Function**</span></span>|<span data-ttu-id="89e9e-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="89e9e-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89e9e-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="89e9e-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="89e9e-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="89e9e-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="89e9e-147">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="89e9e-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="89e9e-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="89e9e-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="89e9e-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="89e9e-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="89e9e-150">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="89e9e-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89e9e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89e9e-151">See also</span></span>



[<span data-ttu-id="89e9e-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89e9e-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="89e9e-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="89e9e-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="89e9e-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="89e9e-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="89e9e-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="89e9e-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="89e9e-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="89e9e-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="89e9e-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="89e9e-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="89e9e-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="89e9e-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="89e9e-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="89e9e-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="89e9e-160">PidTagMessageEditorFormat (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89e9e-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="89e9e-161">Kanonische PidLidUseTnef-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="89e9e-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="89e9e-162">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="89e9e-162">MAPI Constants</span></span>](mapi-constants.md)

