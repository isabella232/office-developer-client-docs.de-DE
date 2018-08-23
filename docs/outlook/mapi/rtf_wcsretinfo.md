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
ms.openlocfilehash: bf8cf115c6188b5058717437c470e11797ff5b9a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564962"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="f5fc7-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="f5fc7-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="f5fc7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5fc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5fc7-105">Diese Struktur enthält Informationen zu einem Datenstrom im systemeigenen Format von Dekomprimieren den Textkörper einer Nachricht, die in der komprimierten Rich Text Format (RTF) zusammengefasst wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5fc7-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5fc7-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f5fc7-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="f5fc7-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="f5fc7-107">Members</span></span>

<span data-ttu-id="f5fc7-108">_size_</span><span class="sxs-lookup"><span data-stu-id="f5fc7-108">_size_</span></span>
  
> <span data-ttu-id="f5fc7-109">Die Größe der Struktur **RTF_WCSRETINFO** als Byteanzahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5fc7-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="f5fc7-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="f5fc7-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="f5fc7-111">Dies ist ein Wert, der das Format des Textkörpers systemeigene angibt.</span><span class="sxs-lookup"><span data-stu-id="f5fc7-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="f5fc7-112">Dieser Wert ist nur gültig, wenn das Flag **MAPI_NATIVE_BODY** in der Struktur [RTF_WCSINFO](rtf_wcsinfo.md) der _UlFlags_ -Parameter übergeben wird, die an die Funktion [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f5fc7-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="f5fc7-113">Dies kann eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="f5fc7-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="f5fc7-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="f5fc7-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="f5fc7-115">Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper RTF weist.</span><span class="sxs-lookup"><span data-stu-id="f5fc7-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="f5fc7-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="f5fc7-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="f5fc7-117">Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper nur-Text-Format weist.</span><span class="sxs-lookup"><span data-stu-id="f5fc7-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="f5fc7-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="f5fc7-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="f5fc7-119">Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper-Format (Hypertext Markup Language weist).</span><span class="sxs-lookup"><span data-stu-id="f5fc7-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5fc7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5fc7-120">See also</span></span>

- [<span data-ttu-id="f5fc7-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="f5fc7-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

