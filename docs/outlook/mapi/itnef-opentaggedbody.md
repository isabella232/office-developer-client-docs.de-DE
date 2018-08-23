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
ms.openlocfilehash: 14964f367e3dbca484c4e1612b374a6a72ddf17b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593781"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="5848a-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="5848a-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="5848a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5848a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5848a-105">Öffnet eine Stream-Schnittstelle für den Text der Fehlermeldung der gekapselte.</span><span class="sxs-lookup"><span data-stu-id="5848a-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="5848a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5848a-106">Parameters</span></span>

 <span data-ttu-id="5848a-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5848a-107">_lpMessage_</span></span>
  
> <span data-ttu-id="5848a-108">[in] Ein Zeiger auf die Nachricht, die die Stream-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5848a-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="5848a-109">Diese Nachricht ist nicht erforderlich, um die gleiche Nachricht werden, die im Aufruf der Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5848a-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="5848a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5848a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5848a-111">[in] Eine Bitmaske aus Flags, die steuert, wie die Schnittstelle Stream geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5848a-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="5848a-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5848a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="5848a-113">MAPI_CREATE IST</span><span class="sxs-lookup"><span data-stu-id="5848a-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="5848a-114">Wenn eine Eigenschaft in der aktuellen Nachricht nicht vorhanden ist, sollte er erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5848a-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="5848a-115">Wenn die Eigenschaft vorhanden ist, sollte die aktuellen Daten in der Eigenschaft mit den Daten aus dem Stream Transport-Neutral Encapsulation Format (TNEF) ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5848a-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="5848a-116">Wenn eine Implementierung der MAPI_CREATE ist Flag festlegt, sollte auch die Kennzeichen MAPI_MODIFY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5848a-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="5848a-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5848a-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5848a-118">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="5848a-118">Requests read/write permission.</span></span> <span data-ttu-id="5848a-119">Die Standard-Schnittstelle ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5848a-119">The default interface is read-only.</span></span> <span data-ttu-id="5848a-120">MAPI_MODIFY muss festgelegt werden, sobald MAPI_CREATE ist festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5848a-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="5848a-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="5848a-121">_lppStream_</span></span>
  
> <span data-ttu-id="5848a-122">[out] Ein Zeiger auf einen Zeiger auf ein Stream-Objekt, das den Text aus der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft des übergebenen enthält gekapselte Nachricht und, das die [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5848a-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5848a-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5848a-123">Return value</span></span>

<span data-ttu-id="5848a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5848a-124">S_OK</span></span> 
  
> <span data-ttu-id="5848a-125">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5848a-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5848a-126">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="5848a-126">Remarks</span></span>

<span data-ttu-id="5848a-127">Transport-Provider, Anbieter Nachricht und Gateways rufen Sie die **ITnef::OpenTaggedBody** -Methode zum Öffnen eine Stream-Schnittstelle für den Text der Fehlermeldung der gekapselte (d. h., eine TNEF-Objekts).</span><span class="sxs-lookup"><span data-stu-id="5848a-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="5848a-128">Als Teil der Verarbeitung **OpenTaggedBody** eingefügt oder analysiert Anlage-Tags, die die Position des alle Anlagen oder OLE-Objekte in den Nachrichtentext angeben.</span><span class="sxs-lookup"><span data-stu-id="5848a-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="5848a-129">Die Anlage-Tags sind im folgenden Format:</span><span class="sxs-lookup"><span data-stu-id="5848a-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="5848a-130">**[[** _Name der Anlage_ **:** _n_ **in** _Anlage Containernamen_ **]]**</span><span class="sxs-lookup"><span data-stu-id="5848a-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="5848a-131">_Name der Anlage_ beschreibt das Attachment-Objekt.  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist von der im Parameter _LpKey_ der [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder der [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergebene Wert erhöht. und _Anlage Containername_ beschreibt die physikalische Komponente, in dem das Attachment-Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="5848a-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="5848a-132">**OpenTaggedBody** des Nachrichtentexts liest und einen Attachment-Tag eingefügt, unabhängig von dessen Speicherort ein Attachment-Objekt ursprünglich im Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5848a-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="5848a-133">Der Text der ursprünglichen Nachricht wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="5848a-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="5848a-134">Wenn eine Meldung mit Tags in einem Stream-Objekt übergeben wird, die Tags entfernt werden, und Attachment-Objekte werden in die Position der Tags im Stream-Objekt verschoben.</span><span class="sxs-lookup"><span data-stu-id="5848a-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5848a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5848a-135">See also</span></span>



[<span data-ttu-id="5848a-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="5848a-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="5848a-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="5848a-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="5848a-138">PidTagBody (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5848a-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="5848a-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5848a-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

