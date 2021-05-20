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
# <a name="rtf_wcsinfo"></a><span data-ttu-id="865ed-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="865ed-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="865ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="865ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="865ed-105">Mit dieser Struktur können Sie Informationen zum Dekomprimieren des Nachrichtentexts im komprimierten Rich Text Format (RTF) angeben und optional den Textdatenstrom im systemeigenen Format zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="865ed-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="865ed-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="865ed-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="865ed-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="865ed-107">Members</span></span>

 <span data-ttu-id="865ed-108">_size_</span><span class="sxs-lookup"><span data-stu-id="865ed-108">_size_</span></span>
  
> <span data-ttu-id="865ed-109">Die Größe der **RTF_WCSINFO** in der Anzahl der Bytes.</span><span class="sxs-lookup"><span data-stu-id="865ed-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="865ed-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="865ed-110">_ulFlags_</span></span>
  
> <span data-ttu-id="865ed-111">Dies ist die Bitmaske der Optionskennzeichen für die [WrapCompressedRTFStreamEx-Funktion.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="865ed-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="865ed-112">Die unterstützten Optionskennzeichen sind:</span><span class="sxs-lookup"><span data-stu-id="865ed-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="865ed-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="865ed-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="865ed-114">Dies gibt an, ob der Client die zurückgegebene umschlossene Streamschnittstelle schreiben möchte.</span><span class="sxs-lookup"><span data-stu-id="865ed-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="865ed-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="865ed-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="865ed-116">Dies gibt an, ob der dekomprimierte RTF in den Datenstrom geschrieben werden soll, auf den der  _lpCompressedRTFStream-Zeiger_ der [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) verweist.</span><span class="sxs-lookup"><span data-stu-id="865ed-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="865ed-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="865ed-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="865ed-118">Dies gibt an, ob der dekomprimierte Datenstrom auch in den systemeigenen Textkörper konvertiert wird, bevor der Datenstrom zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="865ed-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="865ed-119">Dieses Flag kann nicht mit dem MAPI_MODIFY **kombiniert** werden.</span><span class="sxs-lookup"><span data-stu-id="865ed-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="865ed-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="865ed-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="865ed-121">Dies ist der Codeseitenwert der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="865ed-121">This is the code page value of the message.</span></span> <span data-ttu-id="865ed-122">In der Regel wird dieser Wert aus der [kanonischen Eigenschaft PidTagInternetCodepage für](pidtaginternetcodepage-canonical-property.md) die Nachricht bezogen.</span><span class="sxs-lookup"><span data-stu-id="865ed-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="865ed-123">Dieser Wert wird nur verwendet, wenn **das MAPI_NATIVE_BODY** in _ulFlags übergeben wird._</span><span class="sxs-lookup"><span data-stu-id="865ed-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="865ed-124">Andernfalls wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="865ed-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="865ed-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="865ed-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="865ed-126">Dies ist der Codeseitenwert des zurückgegebenen dekomprimierten Datenstroms, den Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="865ed-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="865ed-127">Wenn dies auf einen Nicht-Null-Wert festgelegt ist, konvertiert die [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) den Datenstrom in die angegebene Codeseite.</span><span class="sxs-lookup"><span data-stu-id="865ed-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="865ed-128">Wenn dieser Wert auf null festgelegt ist, entscheidet MAPI, welche Codeseite verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="865ed-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="865ed-129">Dieser Wert wird nur verwendet, wenn **das MAPI_NATIVE_BODY** in  _ulFlags_ übergeben wird und das Textformat nicht RTF ist.</span><span class="sxs-lookup"><span data-stu-id="865ed-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="865ed-130">Andernfalls wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="865ed-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="865ed-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="865ed-131">See also</span></span>



[<span data-ttu-id="865ed-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="865ed-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

