---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426170"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="48af7-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="48af7-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="48af7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48af7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48af7-105">Diese Struktur stellt Informationen zu einem Stream im systemeigenen Format bereit, der von der Dekomprimierung des Texts einer Nachricht zurückgegeben wird, die im komprimierten Rich-Text-Format (RTF) gekapselt ist.</span><span class="sxs-lookup"><span data-stu-id="48af7-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="48af7-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="48af7-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="48af7-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="48af7-107">Members</span></span>

<span data-ttu-id="48af7-108">_size_</span><span class="sxs-lookup"><span data-stu-id="48af7-108">_size_</span></span>
  
> <span data-ttu-id="48af7-109">Die Größe der **RTF_WCSRETINFO** -Struktur in der Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="48af7-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="48af7-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="48af7-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="48af7-111">Dies ist ein Wert, der das Format des systemeigenen Texts angibt.</span><span class="sxs-lookup"><span data-stu-id="48af7-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="48af7-112">Dieser Wert ist nur gültig, wenn das **MAPI_NATIVE_BODY** -Flag im _ulFlags_ -Parameter der [RTF_WCSINFO](rtf_wcsinfo.md) -Struktur übergeben wird, die an die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="48af7-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="48af7-113">Dabei kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="48af7-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="48af7-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="48af7-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="48af7-115">Dieser Wert wird nur verwendet, wenn _ulFlags_ das **MAPI_NATIVE_BODY** -Flag enthält und der Text RTF ist.</span><span class="sxs-lookup"><span data-stu-id="48af7-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="48af7-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="48af7-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="48af7-117">Dieser Wert wird nur verwendet, wenn _ulFlags_ das **MAPI_NATIVE_BODY** -Flag enthält und der Text nur-Text-Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="48af7-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="48af7-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="48af7-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="48af7-119">Dieser Wert wird nur verwendet, wenn _ulFlags_ das **MAPI_NATIVE_BODY** -Flag enthält, und der Text im HTML-Format (Hypertext Markup Language).</span><span class="sxs-lookup"><span data-stu-id="48af7-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48af7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48af7-120">See also</span></span>

- [<span data-ttu-id="48af7-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="48af7-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

