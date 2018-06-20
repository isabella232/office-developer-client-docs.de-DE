---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 032f071e18af3a89a2850cf2bd1e141f34bc86d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792038"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="9e90b-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="9e90b-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="9e90b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e90b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e90b-105">Gibt an, dass eine optional, die die MAPI zur Verwendung von MIME-Konverter Zeichensatz beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="9e90b-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="9e90b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e90b-106">Parameters</span></span>

 <span data-ttu-id="9e90b-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="9e90b-107">_fApply_</span></span>
  
> <span data-ttu-id="9e90b-108">[in] Gibt an, ob Sie einen bestimmten Zeichensatz für die Konvertierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e90b-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="9e90b-109">Legen Sie diesen Parameter auf **true fest,** den Zeichensatz in nachfolgenden Konvertierungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="9e90b-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="9e90b-110">Legen Sie diesen Parameter auf **false festgelegt** , wenn Sie nicht mehr gelten bestimmten Zeichensatz und auf die Standardwerte für nachfolgende Nachrichten zurückgeben möchten.</span><span class="sxs-lookup"><span data-stu-id="9e90b-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="9e90b-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="9e90b-111">_hcharset_</span></span>
  
> <span data-ttu-id="9e90b-112">[in] Ein Handle für einen Zeichensatz gemäß Definition im mimeole.h von Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="9e90b-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="9e90b-113">Geben Sie **null,** um anzugeben, dass keine bestimmten Zeichensatz anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9e90b-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="9e90b-114">Für nicht - **null** -Werte können mit einer Funktion wie [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) einen Handle für den Zeichensatz abrufen.</span><span class="sxs-lookup"><span data-stu-id="9e90b-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="9e90b-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="9e90b-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="9e90b-116">[in] Gibt an, wie anwenden ein Zeichensatzes auf eine Nachricht zu konvertieren, gemäß Definition im mimeole.h von Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="9e90b-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e90b-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9e90b-117">Return value</span></span>

<span data-ttu-id="9e90b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e90b-118">S_OK</span></span>
  
> <span data-ttu-id="9e90b-119">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9e90b-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e90b-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="9e90b-120">MFCMAPI reference</span></span>

<span data-ttu-id="9e90b-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9e90b-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e90b-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9e90b-122">**File**</span></span>|<span data-ttu-id="9e90b-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9e90b-123">**Function**</span></span>|<span data-ttu-id="9e90b-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9e90b-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e90b-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="9e90b-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9e90b-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="9e90b-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="9e90b-127">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9e90b-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9e90b-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="9e90b-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9e90b-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="9e90b-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="9e90b-130">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="9e90b-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e90b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e90b-131">See also</span></span>



[<span data-ttu-id="9e90b-132">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e90b-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="9e90b-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="9e90b-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="9e90b-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="9e90b-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="9e90b-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="9e90b-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="9e90b-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="9e90b-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="9e90b-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="9e90b-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="9e90b-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="9e90b-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

