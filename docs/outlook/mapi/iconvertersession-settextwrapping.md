---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 81771a263a7496042d4950b465c0d5b03290399b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792041"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="79ce8-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="79ce8-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="79ce8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79ce8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79ce8-105">Legt den Text umschließen Breite für ein MIME-Datenstrom, den der Konverter in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79ce8-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="79ce8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79ce8-106">Parameters</span></span>

 <span data-ttu-id="79ce8-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="79ce8-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="79ce8-108">[in] Ob Text umgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="79ce8-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="79ce8-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="79ce8-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="79ce8-110">[in] Der Textumbruch Breite zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="79ce8-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79ce8-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="79ce8-111">Return value</span></span>

<span data-ttu-id="79ce8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="79ce8-112">S_OK</span></span>
  
> <span data-ttu-id="79ce8-113">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="79ce8-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="79ce8-114">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="79ce8-114">MFCMAPI reference</span></span>

<span data-ttu-id="79ce8-115">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="79ce8-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79ce8-116">**Datei**</span><span class="sxs-lookup"><span data-stu-id="79ce8-116">**File**</span></span>|<span data-ttu-id="79ce8-117">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="79ce8-117">**Function**</span></span>|<span data-ttu-id="79ce8-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="79ce8-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79ce8-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="79ce8-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="79ce8-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="79ce8-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="79ce8-121">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="79ce8-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="79ce8-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="79ce8-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="79ce8-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="79ce8-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="79ce8-124">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="79ce8-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79ce8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79ce8-125">See also</span></span>



[<span data-ttu-id="79ce8-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79ce8-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="79ce8-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="79ce8-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="79ce8-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="79ce8-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="79ce8-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="79ce8-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="79ce8-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="79ce8-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="79ce8-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="79ce8-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="79ce8-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="79ce8-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="79ce8-133">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="79ce8-133">MAPI Constants</span></span>](mapi-constants.md)

