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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f1a4834fc600cc93eeb7fc96563723326c7f2169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792045"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="d2cab-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="d2cab-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="d2cab-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2cab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2cab-105">Legt das Format, in dem der Konverter MIME-Stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="d2cab-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="d2cab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2cab-106">Parameters</span></span>

<span data-ttu-id="d2cab-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="d2cab-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="d2cab-108">[in] Das Speichern-format für einen MIME-Stream verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2cab-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="d2cab-109">Weitere Informationen finden Sie unter den Enumerationstyp [MIMESAVETYPE](http://msdn.microsoft.com/de-de/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2cab-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/de-de/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="d2cab-110">**SAVE_RFC1521**: Verwendung MIME, was die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="d2cab-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="d2cab-111">**SAVE_RFC822**: Uuencode verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2cab-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d2cab-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d2cab-112">Return values</span></span>

<span data-ttu-id="d2cab-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2cab-113">S_OK</span></span>
  
> <span data-ttu-id="d2cab-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d2cab-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d2cab-115">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="d2cab-115">MFCMAPI reference</span></span>

<span data-ttu-id="d2cab-116">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d2cab-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d2cab-117">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d2cab-117">**File**</span></span>|<span data-ttu-id="d2cab-118">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d2cab-118">**Function**</span></span>|<span data-ttu-id="d2cab-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d2cab-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2cab-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d2cab-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d2cab-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="d2cab-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="d2cab-122">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d2cab-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="d2cab-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d2cab-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d2cab-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="d2cab-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="d2cab-125">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d2cab-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2cab-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2cab-126">See also</span></span>

- [<span data-ttu-id="d2cab-127">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2cab-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="d2cab-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="d2cab-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="d2cab-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="d2cab-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="d2cab-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="d2cab-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="d2cab-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="d2cab-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="d2cab-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="d2cab-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="d2cab-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="d2cab-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="d2cab-134">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d2cab-134">MAPI Constants</span></span>](mapi-constants.md)

