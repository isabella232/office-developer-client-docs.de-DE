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
# <a name="rtf_wcsretinfo"></a><span data-ttu-id="5f355-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="5f355-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="5f355-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f355-105">Diese Struktur enthält Informationen zu einem Datenstrom im systemeigenen Format, der beim Dekomprimieren des Textkörpers einer Nachricht zurückgegeben wird, der im komprimierten Rich Text Format (RTF) gekapselt ist.</span><span class="sxs-lookup"><span data-stu-id="5f355-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5f355-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5f355-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="5f355-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="5f355-107">Members</span></span>

<span data-ttu-id="5f355-108">_size_</span><span class="sxs-lookup"><span data-stu-id="5f355-108">_size_</span></span>
  
> <span data-ttu-id="5f355-109">Die Größe der **RTF_WCSRETINFO** in der Anzahl der Bytes.</span><span class="sxs-lookup"><span data-stu-id="5f355-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="5f355-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="5f355-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="5f355-111">Dies ist ein Wert, der das Format des systemeigenen Textkörpers angibt.</span><span class="sxs-lookup"><span data-stu-id="5f355-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="5f355-112">Dieser Wert ist nur gültig, wenn **das MAPI_NATIVE_BODY**  _im ulFlags-Parameter_ der [RTF_WCSINFO-Struktur](rtf_wcsinfo.md) übergeben wird, die an die [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f355-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="5f355-113">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="5f355-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="5f355-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="5f355-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="5f355-115">Dieser Wert wird nur verwendet, wenn  _ulFlags_ das MAPI_NATIVE_BODY **und** der Textkörper RTF ist.</span><span class="sxs-lookup"><span data-stu-id="5f355-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="5f355-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="5f355-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="5f355-117">Dieser Wert wird nur verwendet, wenn  _ulFlags_ das MAPI_NATIVE_BODY **enthält** und der Textkörper nur im Nur-Text-Format ist.</span><span class="sxs-lookup"><span data-stu-id="5f355-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="5f355-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="5f355-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="5f355-119">Dieser Wert wird nur verwendet,  wenn _ulFlags_ das MAPI_NATIVE_BODY und der Textkörper das HTML-Format (Hypertext Markup Language) hat.</span><span class="sxs-lookup"><span data-stu-id="5f355-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f355-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f355-120">See also</span></span>

- [<span data-ttu-id="5f355-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="5f355-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

