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
description: 'Letzte Änderung: 20. September 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326944"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="20e87-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="20e87-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="20e87-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20e87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20e87-105">Konvertiert eine MAPI-Nachricht in einen MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="20e87-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="20e87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20e87-106">Parameters</span></span>

 <span data-ttu-id="20e87-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="20e87-107">_pmsg_</span></span>
  
> <span data-ttu-id="20e87-108">in Zeiger auf die zu konvertierende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="20e87-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="20e87-109">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="20e87-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="20e87-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="20e87-110">_pstm_</span></span>
  
> <span data-ttu-id="20e87-111">Out [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle zum Ausgeben des Streams.</span><span class="sxs-lookup"><span data-stu-id="20e87-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="20e87-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20e87-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="20e87-113">in Flags, die bestimmte Aktionen für den Konverter kennzeichnen:</span><span class="sxs-lookup"><span data-stu-id="20e87-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="20e87-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="20e87-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="20e87-115">Der Konverter sollte 8-Bit-Kopfzeilen zulassen.</span><span class="sxs-lookup"><span data-stu-id="20e87-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="20e87-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="20e87-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="20e87-117">Gesendete/nicht gesendete Informationen werden in X-unsent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="20e87-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="20e87-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="20e87-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="20e87-119">Der Konverter sollte eine internationale Nachricht (EAI/RFC6530) erstellen.</span><span class="sxs-lookup"><span data-stu-id="20e87-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="20e87-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="20e87-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="20e87-121">BCC-Empfänger der MAPI-Nachricht sollten im MIME-Stream enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="20e87-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="20e87-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="20e87-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="20e87-123">In ausgehenden Nachrichten keine Nachricht-ID-Felder einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="20e87-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="20e87-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="20e87-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="20e87-125">Der Konverter sollte die Kopfzeilen der externen Nachricht ignorieren.</span><span class="sxs-lookup"><span data-stu-id="20e87-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="20e87-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="20e87-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="20e87-127">Der Konverter sollte nur nur-Text senden.</span><span class="sxs-lookup"><span data-stu-id="20e87-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="20e87-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="20e87-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="20e87-129">Der Konverter wird an eine SMTP-Nachricht übergeben.</span><span class="sxs-lookup"><span data-stu-id="20e87-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="20e87-130">Dieses Flag muss immer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="20e87-130">This flag must always be set.</span></span>
    
<span data-ttu-id="20e87-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="20e87-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="20e87-132">Der Konverter sollte in der MIME-Nachricht vom HTML-in das RTF-Format konvertieren.</span><span class="sxs-lookup"><span data-stu-id="20e87-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="20e87-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="20e87-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="20e87-134">Der Konverter sollte das TNEF-Format (Transport Neutral Encapsulation Format) in der MIME-Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="20e87-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="20e87-135">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="20e87-135">Return values</span></span>

<span data-ttu-id="20e87-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="20e87-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="20e87-137">Ungültige Flags wurden übergeben, oder *pmsg* oder *pstm* ist NULL.</span><span class="sxs-lookup"><span data-stu-id="20e87-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="20e87-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20e87-138">Remarks</span></span>

<span data-ttu-id="20e87-139">Wird nur für standardmäßige Outlook-Nachrichtentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20e87-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="20e87-140">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="20e87-140">MFCMAPI reference</span></span>

<span data-ttu-id="20e87-141">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="20e87-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="20e87-142">**Datei**</span><span class="sxs-lookup"><span data-stu-id="20e87-142">**File**</span></span>|<span data-ttu-id="20e87-143">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="20e87-143">**Function**</span></span>|<span data-ttu-id="20e87-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="20e87-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20e87-145">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="20e87-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="20e87-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="20e87-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="20e87-147">MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="20e87-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="20e87-148">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="20e87-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="20e87-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="20e87-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="20e87-150">MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="20e87-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20e87-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20e87-151">See also</span></span>



[<span data-ttu-id="20e87-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20e87-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="20e87-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="20e87-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="20e87-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="20e87-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="20e87-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="20e87-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="20e87-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="20e87-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="20e87-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="20e87-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="20e87-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="20e87-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="20e87-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="20e87-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="20e87-160">Kanonische Pidtagmessageeditorformat (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="20e87-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="20e87-161">Kanonische PidLidUseTnef-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="20e87-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="20e87-162">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="20e87-162">MAPI Constants</span></span>](mapi-constants.md)

