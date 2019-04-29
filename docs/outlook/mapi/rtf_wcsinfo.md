---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430532"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="5ea82-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="5ea82-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="5ea82-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ea82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ea82-105">Mit dieser Struktur können Sie Informationen zum Dekomprimieren des Textkörpers einer Nachricht im komprimierten Rich-Text-Format (RTF) angeben und optional den Body-Stream im systemeigenen Format zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5ea82-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5ea82-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5ea82-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="5ea82-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="5ea82-107">Members</span></span>

 <span data-ttu-id="5ea82-108">_size_</span><span class="sxs-lookup"><span data-stu-id="5ea82-108">_size_</span></span>
  
> <span data-ttu-id="5ea82-109">Die Größe der **RTF_WCSINFO** -Struktur in der Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="5ea82-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="5ea82-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ea82-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5ea82-111">Dies ist die Bitmaske von Options Kennzeichen für die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5ea82-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="5ea82-112">Die unterstützten Options-Flags sind:</span><span class="sxs-lookup"><span data-stu-id="5ea82-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="5ea82-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5ea82-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="5ea82-114">Dies gibt an, ob der Client beabsichtigt, die eingebundene Datenstromschnittstelle zu schreiben, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ea82-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="5ea82-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="5ea82-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="5ea82-116">Dies gibt an, ob das dekomprimierte RTF-Format in den Stream geschrieben werden soll, auf den durch den _lpCompressedRTFStream_ -Zeiger der [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5ea82-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="5ea82-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="5ea82-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="5ea82-118">Dies gibt an, ob der dekomprimierte Stream auch in den systemeigenen Text konvertiert wird, bevor der Stream zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ea82-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="5ea82-119">Dieses Flag kann nicht mit dem **MAPI_MODIFY** -Flag kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="5ea82-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="5ea82-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="5ea82-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="5ea82-121">Dies ist der Codepage-Wert der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5ea82-121">This is the code page value of the message.</span></span> <span data-ttu-id="5ea82-122">Dieser Wert wird in der Regel von der [kanonischEn Pidtaginternetcodepage (-Eigenschaft](pidtaginternetcodepage-canonical-property.md) der Nachricht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ea82-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="5ea82-123">Dieser Wert wird nur verwendet, wenn das **MAPI_NATIVE_BODY** -Flag in _ulFlags_übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ea82-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="5ea82-124">Andernfalls wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5ea82-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="5ea82-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="5ea82-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="5ea82-126">Hierbei handelt es sich um den Codepage-Wert des zurückgegebenen dekomprimierten Streams, den Sie wünschen.</span><span class="sxs-lookup"><span data-stu-id="5ea82-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="5ea82-127">Wenn dies auf einen Wert ungleich NULL festgelegt ist, wird der Stream von der [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion in die angegebene Codepage konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5ea82-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="5ea82-128">Wenn dies auf einen Nullwert festgelegt ist, bestimmt MAPI, welche Codepage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ea82-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="5ea82-129">Dieser Wert wird nur verwendet, wenn das **MAPI_NATIVE_BODY** -Flag in _ulFlags_übergeben wird, und das Body-Format nicht RTF ist.</span><span class="sxs-lookup"><span data-stu-id="5ea82-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="5ea82-130">Andernfalls wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5ea82-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ea82-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea82-131">See also</span></span>



[<span data-ttu-id="5ea82-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="5ea82-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

