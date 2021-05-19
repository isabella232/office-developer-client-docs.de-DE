---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348734"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="aaf7c-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="aaf7c-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="aaf7c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf7c-105">Öffnet eine Streamschnittstelle für den Text einer gekapselten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="aaf7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaf7c-106">Parameters</span></span>

 <span data-ttu-id="aaf7c-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="aaf7c-107">_lpMessage_</span></span>
  
> <span data-ttu-id="aaf7c-108">[in] Ein Zeiger auf die Nachricht, der der Datenstrom zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="aaf7c-109">Diese Nachricht muss nicht dieselbe Nachricht sein, die beim Aufruf der [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion übergeben](opentnefstreamex.md) wird.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="aaf7c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aaf7c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="aaf7c-111">[in] Eine Bitmaske mit Flags, die steuert, wie die Streamschnittstelle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="aaf7c-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="aaf7c-112">The following flags can be set:</span></span>
    
<span data-ttu-id="aaf7c-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="aaf7c-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="aaf7c-114">Wenn in der aktuellen Nachricht keine Eigenschaft vorhanden ist, sollte sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="aaf7c-115">Wenn die Eigenschaft vorhanden ist, sollten die aktuellen Daten in der Eigenschaft durch die Daten aus dem Transport-Neutral Encapsulation Format (TNEF)-Stream ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="aaf7c-116">Wenn eine Implementierung das MAPI_CREATE legt, sollte sie auch das MAPI_MODIFY festlegen.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="aaf7c-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="aaf7c-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="aaf7c-118">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-118">Requests read/write permission.</span></span> <span data-ttu-id="aaf7c-119">Die Standardschnittstelle ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-119">The default interface is read-only.</span></span> <span data-ttu-id="aaf7c-120">MAPI_MODIFY muss festgelegt werden, wenn MAPI_CREATE festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="aaf7c-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="aaf7c-121">_lppStream_</span></span>
  
> <span data-ttu-id="aaf7c-122">[out] Ein Zeiger auf einen Zeiger auf ein Streamobjekt, das den Text aus der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft der übergebenen gekapselten Nachricht enthält und die [IStream-Schnittstelle](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aaf7c-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aaf7c-123">Return value</span></span>

<span data-ttu-id="aaf7c-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="aaf7c-124">S_OK</span></span> 
  
> <span data-ttu-id="aaf7c-125">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aaf7c-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aaf7c-126">Remarks</span></span>

<span data-ttu-id="aaf7c-127">Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::OpenTaggedBody-Methode** auf, um eine Streamschnittstelle für den Text einer gekapselten Nachricht (d. h. für ein TNEF-Objekt) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="aaf7c-128">Im Rahmen der Verarbeitung fügt **OpenTaggedBody** Anlagentags ein oder analysiert sie, die die Position von Anlagen oder OLE-Objekten im Nachrichtentext angeben.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="aaf7c-129">Die Anlagentags haben das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="aaf7c-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="aaf7c-130">**[[** _Anlagenname_ **:** _n_ **im** Namen des _Anlagencontainers_ **]]**</span><span class="sxs-lookup"><span data-stu-id="aaf7c-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="aaf7c-131">_Anlagenname_ beschreibt das Attachment-Objekt.  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist, inkrementiert von dem Wert, der im  _lpKey-Parameter_ der [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben wird. und  _der Name des Anlagencontainers_ beschreibt die physische Komponente, in der sich das Anlageobjekt befindet.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="aaf7c-132">**OpenTaggedBody** liest Nachrichtentext aus und fügt ein Anlagentag an jedem Ort ein, an dem ein Anlageobjekt ursprünglich im Text angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="aaf7c-133">Der ursprüngliche Nachrichtentext wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="aaf7c-134">Wenn eine Nachricht mit Tags an einen Datenstrom übergeben wird, werden die Tags entfernt, und die Anlagenobjekte werden an der Position der Tags im Datenstrom verschoben.</span><span class="sxs-lookup"><span data-stu-id="aaf7c-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aaf7c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaf7c-135">See also</span></span>



[<span data-ttu-id="aaf7c-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="aaf7c-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="aaf7c-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="aaf7c-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="aaf7c-138">PidTagBody (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aaf7c-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="aaf7c-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aaf7c-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

