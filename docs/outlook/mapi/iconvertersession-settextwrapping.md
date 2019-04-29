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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423587"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="729e9-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="729e9-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="729e9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729e9-105">Legt die Breite des Textumbruchs für einen MIME-Stream fest, den der Konverter in [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="729e9-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="729e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="729e9-106">Parameters</span></span>

 <span data-ttu-id="729e9-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="729e9-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="729e9-108">in Ob Text umbrochen werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="729e9-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="729e9-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="729e9-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="729e9-110">in Die zu verwendende Textumbruch Breite.</span><span class="sxs-lookup"><span data-stu-id="729e9-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="729e9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="729e9-111">Return value</span></span>

<span data-ttu-id="729e9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="729e9-112">S_OK</span></span>
  
> <span data-ttu-id="729e9-113">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="729e9-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="729e9-114">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="729e9-114">MFCMAPI reference</span></span>

<span data-ttu-id="729e9-115">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="729e9-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="729e9-116">**Datei**</span><span class="sxs-lookup"><span data-stu-id="729e9-116">**File**</span></span>|<span data-ttu-id="729e9-117">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="729e9-117">**Function**</span></span>|<span data-ttu-id="729e9-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="729e9-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="729e9-119">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="729e9-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="729e9-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="729e9-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="729e9-121">MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="729e9-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="729e9-122">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="729e9-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="729e9-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="729e9-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="729e9-124">MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="729e9-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="729e9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="729e9-125">See also</span></span>



[<span data-ttu-id="729e9-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="729e9-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="729e9-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="729e9-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="729e9-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="729e9-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="729e9-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="729e9-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="729e9-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="729e9-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="729e9-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="729e9-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="729e9-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="729e9-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="729e9-133">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="729e9-133">MAPI Constants</span></span>](mapi-constants.md)

