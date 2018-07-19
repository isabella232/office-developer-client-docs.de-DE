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
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795429"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="dd156-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="dd156-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="dd156-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd156-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd156-105">Diese Struktur können Sie Informationen, die den Textkörper einer Nachricht in der komprimierten Rich Text Format (RTF) dekomprimieren und optional in seinem nativen Format Zurückgeben des Body-Streams angeben.</span><span class="sxs-lookup"><span data-stu-id="dd156-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dd156-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="dd156-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="dd156-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="dd156-107">Members</span></span>

 <span data-ttu-id="dd156-108">_Größe_</span><span class="sxs-lookup"><span data-stu-id="dd156-108">_size_</span></span>
  
> <span data-ttu-id="dd156-109">Die Größe der Struktur **RTF_WCSINFO** als Byteanzahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd156-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="dd156-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd156-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dd156-111">Hierbei handelt es sich um die Bitmaske der Optionsflags für die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dd156-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="dd156-112">Flags für die unterstützten sind:</span><span class="sxs-lookup"><span data-stu-id="dd156-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="dd156-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dd156-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="dd156-114">Dies gibt an, ob der Client beabsichtigt zum Schreiben der gepackten Stream-Schnittstelle, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd156-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="dd156-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="dd156-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="dd156-116">Dies gibt an, ob die dekomprimierte RTF sollte in den Stream geschrieben werden, die mit den Zeiger _LpCompressedRTFStream_ der Funktion [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd156-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="dd156-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="dd156-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="dd156-118">Dies gibt an, ob der dekomprimierte Stream auch der systemeigenen Stelle konvertiert wird, vor der Rückgabe des Streams.</span><span class="sxs-lookup"><span data-stu-id="dd156-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="dd156-119">Dieses Kennzeichen können nicht mit dem **MAPI_MODIFY** -Flag kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="dd156-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="dd156-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="dd156-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="dd156-121">Dies ist der Codepagewert der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dd156-121">This is the code page value of the message.</span></span> <span data-ttu-id="dd156-122">Dieser Wert wird in der Regel aus der [PidTagInternetCodepage kanonische-Eigenschaft](pidtaginternetcodepage-canonical-property.md) für die Nachricht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd156-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="dd156-123">Dieser Wert wird nur verwendet, wenn das Flag **MAPI_NATIVE_BODY** _UlFlags_übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd156-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="dd156-124">Andernfalls wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd156-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="dd156-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="dd156-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="dd156-126">Dies ist der Codepagewert der zurückgegebenen dekomprimierten Stream-Objekts, die Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="dd156-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="dd156-127">Wenn diese auf einen Wert ungleich Null gesetzt ist, konvertiert die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion den Datenstrom in der angegebenen Codepage.</span><span class="sxs-lookup"><span data-stu-id="dd156-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="dd156-128">Wenn dies auf einen NULL-Wert festgelegt ist, beschließt MAPI Codepage verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd156-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="dd156-129">Dieser Wert wird nur, wenn das Flag **MAPI_NATIVE_BODY** _UlFlags_übergeben wird, und das Textformat nicht RTF ist.</span><span class="sxs-lookup"><span data-stu-id="dd156-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="dd156-130">Andernfalls wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd156-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd156-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd156-131">See also</span></span>



[<span data-ttu-id="dd156-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="dd156-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

