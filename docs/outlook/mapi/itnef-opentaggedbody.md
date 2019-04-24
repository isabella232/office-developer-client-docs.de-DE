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
# <a name="itnefopentaggedbody"></a><span data-ttu-id="79a84-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="79a84-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="79a84-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79a84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79a84-105">Öffnet eine Stream-Schnittstelle für den Text einer gekapselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="79a84-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="79a84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79a84-106">Parameters</span></span>

 <span data-ttu-id="79a84-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="79a84-107">_lpMessage_</span></span>
  
> <span data-ttu-id="79a84-108">in Ein Zeiger auf die Nachricht, der der Stream zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="79a84-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="79a84-109">Diese Nachricht muss nicht dieselbe Nachricht sein, die beim Aufruf der [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="79a84-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="79a84-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79a84-110">_ulFlags_</span></span>
  
> <span data-ttu-id="79a84-111">in Eine Bitmaske von Flags, die steuert, wie die Stream-Schnittstelle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="79a84-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="79a84-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="79a84-112">The following flags can be set:</span></span>
    
<span data-ttu-id="79a84-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="79a84-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="79a84-114">Wenn eine Eigenschaft nicht in der aktuellen Nachricht vorhanden ist, sollte Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="79a84-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="79a84-115">Wenn die Eigenschaft vorhanden ist, sollten die aktuellen Daten in der-Eigenschaft durch die Daten aus dem TNEF-Stream (Transport-Neutral Encapsulation Format) ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="79a84-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="79a84-116">Wenn eine Implementierung das MAPI_CREATE-Flag festlegt, sollte auch das MAPI_MODIFY-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="79a84-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="79a84-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="79a84-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="79a84-118">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="79a84-118">Requests read/write permission.</span></span> <span data-ttu-id="79a84-119">Die Standardschnittstelle ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="79a84-119">The default interface is read-only.</span></span> <span data-ttu-id="79a84-120">MAPI_MODIFY muss festgelegt werden, wenn MAPI_CREATE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79a84-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="79a84-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="79a84-121">_lppStream_</span></span>
  
> <span data-ttu-id="79a84-122">Out Ein Zeiger auf einen Zeiger auf ein Stream-Objekt, das den Text aus der **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft der übergebenen verkapselten Nachricht enthält und die [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79a84-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="79a84-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79a84-123">Return value</span></span>

<span data-ttu-id="79a84-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="79a84-124">S_OK</span></span> 
  
> <span data-ttu-id="79a84-125">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79a84-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79a84-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79a84-126">Remarks</span></span>

<span data-ttu-id="79a84-127">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: OpenTaggedBody** -Methode auf, um eine Stream-Schnittstelle für den Text einer gekapselte Nachricht zu öffnen (also für ein TNEF-Objekt).</span><span class="sxs-lookup"><span data-stu-id="79a84-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="79a84-128">Im Rahmen seiner Verarbeitung fügt **OpenTaggedBody** entweder Anhänge-Tags ein, die die Position von Anlagen oder OLE-Objekten im Nachrichtentext Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="79a84-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="79a84-129">Die Attachment-Tags haben das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="79a84-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="79a84-130">**[[** _Attachment Name_ **:** _n_ **in** _Attachment Containername_ **]]**</span><span class="sxs-lookup"><span data-stu-id="79a84-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="79a84-131">_Attachment Name_ Beschreibung des Attachment-Objekts;  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist, die von dem Wert inkrementiert wird, der im _lpKey_ -Parameter der [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben wird; und der _Name des Anlagen Containers_ beschreibt die physische Komponente, in der sich das Attachment-Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="79a84-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="79a84-132">**OpenTaggedBody** liest Nachrichtentext aus und fügt ein Attachment-Tag ein, wenn ein Attachment-Objekt ursprünglich im Text erschien.</span><span class="sxs-lookup"><span data-stu-id="79a84-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="79a84-133">Der ursprüngliche Nachrichtentext wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="79a84-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="79a84-134">Wenn eine Nachricht mit Tags an einen Stream übergeben wird, werden die Tags entfernt, und die Attachment-Objekte werden an die Position der Tags im Stream verschoben.</span><span class="sxs-lookup"><span data-stu-id="79a84-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79a84-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79a84-135">See also</span></span>



[<span data-ttu-id="79a84-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="79a84-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="79a84-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="79a84-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="79a84-138">Kanonische Pidtagbody (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="79a84-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="79a84-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79a84-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

