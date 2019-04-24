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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341300"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="013d8-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="013d8-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="013d8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="013d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="013d8-105">Initialisiert die Codierung, die während der Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="013d8-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="013d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="013d8-106">Parameters</span></span>

<span data-ttu-id="013d8-107">_et_</span><span class="sxs-lookup"><span data-stu-id="013d8-107">_et_</span></span>
  
> <span data-ttu-id="013d8-108">Ein [EncodingType](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) -Wert.</span><span class="sxs-lookup"><span data-stu-id="013d8-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="013d8-109">Nur die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="013d8-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="013d8-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="013d8-110">IET_BASE64</span></span>
   - <span data-ttu-id="013d8-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="013d8-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="013d8-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="013d8-112">IET_QP</span></span>
   - <span data-ttu-id="013d8-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="013d8-113">IET_7BIT</span></span>
   - <span data-ttu-id="013d8-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="013d8-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="013d8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="013d8-115">Return value</span></span>

<span data-ttu-id="013d8-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="013d8-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="013d8-117">Der übergebene Codierungs war ungültig.</span><span class="sxs-lookup"><span data-stu-id="013d8-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="013d8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="013d8-118">Remarks</span></span>

<span data-ttu-id="013d8-119">Rufen \*\*\*\* Sie die setEncoding vor der Verwendung von [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) für die Konvertierung auf.</span><span class="sxs-lookup"><span data-stu-id="013d8-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="013d8-120">Verwenden \*\*\*\* Sie setEncoding, um die Codierung nur für den äußersten Nachrichtentext eines e-Mail-Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="013d8-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="013d8-121">Microsoft Outlook 2010 und Microsoft Outlook 2013 wählen die Codierung für einzelne Anlagen aus.</span><span class="sxs-lookup"><span data-stu-id="013d8-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="013d8-122">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="013d8-122">MFCMAPI reference</span></span>

<span data-ttu-id="013d8-123">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="013d8-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="013d8-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="013d8-124">**File**</span></span>|<span data-ttu-id="013d8-125">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="013d8-125">**Function**</span></span>|<span data-ttu-id="013d8-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="013d8-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="013d8-127">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="013d8-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="013d8-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="013d8-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="013d8-129">MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="013d8-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="013d8-130">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="013d8-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="013d8-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="013d8-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="013d8-132">MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="013d8-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="013d8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="013d8-133">See also</span></span>

- [<span data-ttu-id="013d8-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="013d8-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="013d8-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="013d8-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="013d8-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="013d8-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="013d8-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="013d8-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="013d8-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="013d8-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="013d8-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="013d8-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="013d8-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="013d8-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="013d8-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="013d8-141">MAPI Constants</span></span>](mapi-constants.md)

