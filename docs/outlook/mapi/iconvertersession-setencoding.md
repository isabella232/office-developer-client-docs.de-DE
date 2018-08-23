---
title: IConverterSessionSetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3edcb422eb0e3dd415d49c5e014c8b69095e7ec1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577205"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="63a63-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="63a63-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="63a63-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63a63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63a63-105">Initialisiert die Codierung, um bei der Umwandlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63a63-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="63a63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63a63-106">Parameters</span></span>

<span data-ttu-id="63a63-107">_et_</span><span class="sxs-lookup"><span data-stu-id="63a63-107">_et_</span></span>
  
> <span data-ttu-id="63a63-108">Ein [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) -Wert.</span><span class="sxs-lookup"><span data-stu-id="63a63-108">An [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="63a63-109">Nur die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="63a63-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="63a63-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="63a63-110">IET_BASE64</span></span>
   - <span data-ttu-id="63a63-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="63a63-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="63a63-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="63a63-112">IET_QP</span></span>
   - <span data-ttu-id="63a63-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="63a63-113">IET_7BIT</span></span>
   - <span data-ttu-id="63a63-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="63a63-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63a63-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="63a63-115">Return value</span></span>

<span data-ttu-id="63a63-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="63a63-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="63a63-117">Der Typ der Codierung übergeben war ungültig.</span><span class="sxs-lookup"><span data-stu-id="63a63-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63a63-118">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="63a63-118">Remarks</span></span>

<span data-ttu-id="63a63-119">Rufen Sie **SetEncoding** vor der Nutzung [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) Konvertierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="63a63-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="63a63-120">Verwenden Sie zum Festlegen der Codierung für eine e-Mail-Elements nur die äußerste Nachrichtentext **SetEncoding** .</span><span class="sxs-lookup"><span data-stu-id="63a63-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="63a63-121">Microsoft Outlook 2010 und Microsoft Outlook 2013 wählen Sie die Codierung für jede einzelnen Anlagen.</span><span class="sxs-lookup"><span data-stu-id="63a63-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="63a63-122">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="63a63-122">MFCMAPI reference</span></span>

<span data-ttu-id="63a63-123">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="63a63-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63a63-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="63a63-124">**File**</span></span>|<span data-ttu-id="63a63-125">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="63a63-125">**Function**</span></span>|<span data-ttu-id="63a63-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="63a63-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63a63-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="63a63-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="63a63-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="63a63-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="63a63-129">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="63a63-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="63a63-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="63a63-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="63a63-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="63a63-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="63a63-132">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="63a63-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63a63-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63a63-133">See also</span></span>

- [<span data-ttu-id="63a63-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63a63-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="63a63-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="63a63-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="63a63-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="63a63-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="63a63-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="63a63-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="63a63-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="63a63-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="63a63-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="63a63-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="63a63-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="63a63-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="63a63-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="63a63-141">MAPI Constants</span></span>](mapi-constants.md)

