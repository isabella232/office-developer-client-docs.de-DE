---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795411"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="6ff54-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="6ff54-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="6ff54-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ff54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ff54-105">Diese Struktur enthält Informationen zu einem Datenstrom im systemeigenen Format von Dekomprimieren den Textkörper einer Nachricht, die in der komprimierten Rich Text Format (RTF) zusammengefasst wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ff54-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6ff54-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6ff54-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="6ff54-107">Members</span><span class="sxs-lookup"><span data-stu-id="6ff54-107">Members</span></span>

<span data-ttu-id="6ff54-108">_Größe_</span><span class="sxs-lookup"><span data-stu-id="6ff54-108">_size_</span></span>
  
> <span data-ttu-id="6ff54-109">Die Größe der Struktur **RTF_WCSRETINFO** als Byteanzahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="6ff54-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="6ff54-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="6ff54-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="6ff54-111">Dies ist ein Wert, der das Format des Textkörpers systemeigene angibt.</span><span class="sxs-lookup"><span data-stu-id="6ff54-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="6ff54-112">Dieser Wert ist nur gültig, wenn das Flag **MAPI_NATIVE_BODY** in der Struktur [RTF_WCSINFO](rtf_wcsinfo.md) der _UlFlags_ -Parameter übergeben wird, die an die Funktion [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ff54-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="6ff54-113">Dies kann eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="6ff54-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="6ff54-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="6ff54-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="6ff54-115">Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper RTF weist.</span><span class="sxs-lookup"><span data-stu-id="6ff54-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="6ff54-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="6ff54-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="6ff54-117">Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper nur-Text-Format weist.</span><span class="sxs-lookup"><span data-stu-id="6ff54-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="6ff54-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="6ff54-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="6ff54-119">Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper-Format (Hypertext Markup Language weist).</span><span class="sxs-lookup"><span data-stu-id="6ff54-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ff54-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ff54-120">See also</span></span>

- [<span data-ttu-id="6ff54-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="6ff54-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

