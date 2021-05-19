---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421172"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="d6c39-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="d6c39-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="d6c39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6c39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6c39-105">Gibt die Anlagentabelle der Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="d6c39-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d6c39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6c39-106">Parameters</span></span>

 <span data-ttu-id="d6c39-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6c39-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d6c39-108">[in] Bitmaske von Flags, die sich auf die Erstellung der Tabelle beziehen.</span><span class="sxs-lookup"><span data-stu-id="d6c39-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="d6c39-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d6c39-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="d6c39-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6c39-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d6c39-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d6c39-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="d6c39-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d6c39-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="d6c39-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d6c39-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d6c39-114">Ermöglicht **getAttachmentTable,** erfolgreich zurückzukehren, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6c39-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="d6c39-115">Wenn die Tabelle nicht verfügbar ist, kann ein nachfolgender Aufruf der Tabelle zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="d6c39-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="d6c39-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d6c39-116">_lppTable_</span></span>
  
> <span data-ttu-id="d6c39-117">[out] Zeiger auf einen Zeiger auf die Anlagentabelle.</span><span class="sxs-lookup"><span data-stu-id="d6c39-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6c39-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6c39-118">Return value</span></span>

<span data-ttu-id="d6c39-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6c39-119">S_OK</span></span> 
  
> <span data-ttu-id="d6c39-120">Die Anlagentabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d6c39-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6c39-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6c39-121">Remarks</span></span>

<span data-ttu-id="d6c39-122">Die **IMessage::GetAttachmentTable-Methode** gibt einen Zeiger auf die Anlagentabelle der Nachricht zurück, die Informationen zu allen Anlagen in der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="d6c39-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="d6c39-123">Clients können nur über die Anlagentabelle zugriff auf eine Anlage erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6c39-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="d6c39-124">Durch Abrufen der Nummer einer Anlage PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft kann ein Client mehrere der **IMessage-Methoden** verwenden, um mit der Anlage zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6c39-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="d6c39-125">Es gibt eine Zeile für jede Anlage.</span><span class="sxs-lookup"><span data-stu-id="d6c39-125">There is one row for each attachment.</span></span> <span data-ttu-id="d6c39-126">Eine vollständige Liste der Spalten in einer Anlagentabelle finden Sie unter [Attachment Tables](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d6c39-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="d6c39-127">Eine Anlage wird in der Regel erst in der Anlagentabelle angezeigt, wenn sowohl die Anlage als auch die Nachricht mit einem Aufruf von [IMAPIProp::SaveChanges gespeichert wurden.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="d6c39-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="d6c39-128">Anlagentabellen sind dynamisch.</span><span class="sxs-lookup"><span data-stu-id="d6c39-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="d6c39-129">Wenn ein Client eine neue Anlage erstellt, eine vorhandene Anlage löscht oder eine oder mehrere Eigenschaften ändert, nachdem die **SaveChanges-Aufrufe** für die Anlage in der Nachricht ausgeführt wurden, wird die Anlagentabelle entsprechend den neuen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d6c39-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="d6c39-130">Einige Anlagentabellen unterstützen eine Vielzahl von Einschränkungen. Andere tun dies nicht.</span><span class="sxs-lookup"><span data-stu-id="d6c39-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="d6c39-131">Die Unterstützung für Einschränkungen hängt von der Implementierung des Nachrichtenspeicheranbieters ab.</span><span class="sxs-lookup"><span data-stu-id="d6c39-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="d6c39-132">Beim ersten Öffnen werden Anlagentabellen nicht unbedingt in einer bestimmten Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="d6c39-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="d6c39-133">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf die folgenden Aufrufe der Anlagentabelle aus:</span><span class="sxs-lookup"><span data-stu-id="d6c39-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="d6c39-134">[IMAPITable::QueryColumns,](imapitable-querycolumns.md) um den Spaltensatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6c39-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="d6c39-135">[IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d6c39-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="d6c39-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) zum Abrufen der Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d6c39-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="d6c39-137">Das Festlegen des Unicode-Kennzeichens fordert, dass die Informationen für alle von diesen Aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="d6c39-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="d6c39-138">Da jedoch nicht alle Nachrichtenspeicheranbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6c39-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6c39-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6c39-139">See also</span></span>



[<span data-ttu-id="d6c39-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="d6c39-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="d6c39-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="d6c39-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="d6c39-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="d6c39-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="d6c39-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d6c39-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

