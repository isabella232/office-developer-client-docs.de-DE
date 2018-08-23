---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f24ad938fdb8c3ac234e1d78f2668139840c8b8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568217"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="bd7b6-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="bd7b6-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="bd7b6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd7b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd7b6-105">Legt das Format, in dem der Konverter MIME-Stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="bd7b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd7b6-106">Parameters</span></span>

<span data-ttu-id="bd7b6-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="bd7b6-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="bd7b6-108">[in] Das Speichern-format für einen MIME-Stream verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="bd7b6-109">Weitere Informationen finden Sie unter den Enumerationstyp [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd7b6-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="bd7b6-110">**SAVE_RFC1521**: Verwendung MIME, was die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="bd7b6-111">**SAVE_RFC822**: Uuencode verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="bd7b6-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bd7b6-112">Return values</span></span>

<span data-ttu-id="bd7b6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd7b6-113">S_OK</span></span>
  
> <span data-ttu-id="bd7b6-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bd7b6-115">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="bd7b6-115">MFCMAPI reference</span></span>

<span data-ttu-id="bd7b6-116">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bd7b6-117">**Datei**</span><span class="sxs-lookup"><span data-stu-id="bd7b6-117">**File**</span></span>|<span data-ttu-id="bd7b6-118">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="bd7b6-118">**Function**</span></span>|<span data-ttu-id="bd7b6-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="bd7b6-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd7b6-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="bd7b6-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="bd7b6-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="bd7b6-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="bd7b6-122">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="bd7b6-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="bd7b6-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="bd7b6-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="bd7b6-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="bd7b6-125">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="bd7b6-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd7b6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd7b6-126">See also</span></span>

- [<span data-ttu-id="bd7b6-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd7b6-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="bd7b6-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="bd7b6-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="bd7b6-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="bd7b6-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="bd7b6-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="bd7b6-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="bd7b6-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="bd7b6-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="bd7b6-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="bd7b6-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="bd7b6-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="bd7b6-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="bd7b6-134">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="bd7b6-134">MAPI Constants</span></span>](mapi-constants.md)

