---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424609"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="db4ce-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="db4ce-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="db4ce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db4ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db4ce-105">Gibt die Empfängertabelle der Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="db4ce-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="db4ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db4ce-106">Parameters</span></span>

 <span data-ttu-id="db4ce-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="db4ce-107">_ulFlags_</span></span>
  
> <span data-ttu-id="db4ce-108">[in] Bitmaske von Flags, die die Rückgabe der Tabelle steuert.</span><span class="sxs-lookup"><span data-stu-id="db4ce-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="db4ce-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="db4ce-109">The following flags can be set:</span></span>
    
<span data-ttu-id="db4ce-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="db4ce-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="db4ce-111">Ermöglicht **getRecipientTable,** erfolgreich zurückzukehren, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="db4ce-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="db4ce-112">Wenn die Tabelle nicht verfügbar ist, kann ein nachfolgender Aufruf der Tabelle zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="db4ce-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="db4ce-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="db4ce-114">Zeichenfolgenspalten sollten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="db4ce-115">Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgenspalten im ANSI-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="db4ce-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="db4ce-116">_lppTable_</span></span>
  
> <span data-ttu-id="db4ce-117">[out] Zeiger auf einen Zeiger auf die Empfängertabelle.</span><span class="sxs-lookup"><span data-stu-id="db4ce-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db4ce-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db4ce-118">Return value</span></span>

<span data-ttu-id="db4ce-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="db4ce-119">S_OK</span></span> 
  
> <span data-ttu-id="db4ce-120">Die Empfängertabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db4ce-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db4ce-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db4ce-121">Remarks</span></span>

<span data-ttu-id="db4ce-122">Die **IMessage::GetRecipientTable-Methode** gibt einen Zeiger auf die Empfängertabelle der Nachricht zurück, die Informationen zu allen Empfängern für die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="db4ce-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="db4ce-123">Es gibt eine Zeile für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="db4ce-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="db4ce-124">Empfängertabellen haben einen anderen Spaltensatz, je nachdem, ob die Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="db4ce-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="db4ce-125">Eine vollständige Liste der Spalten in einer Empfängertabelle finden Sie unter [Recipient Tables](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="db4ce-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="db4ce-126">Einige Empfängertabellen unterstützen eine Vielzahl von Einschränkungen. Andere tun dies nicht.</span><span class="sxs-lookup"><span data-stu-id="db4ce-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="db4ce-127">Die Unterstützung für Einschränkungen hängt von der Implementierung des Nachrichtenspeicheranbieters ab.</span><span class="sxs-lookup"><span data-stu-id="db4ce-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="db4ce-128">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf die folgenden Aufrufe an die Empfängertabelle aus:</span><span class="sxs-lookup"><span data-stu-id="db4ce-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="db4ce-129">[IMAPITable::QueryColumns,](imapitable-querycolumns.md) um den Spaltensatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="db4ce-130">[IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="db4ce-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) zum Abrufen der Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="db4ce-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="db4ce-132">Das Festlegen des Unicode-Kennzeichens fordert, dass die Informationen für alle von diesen Aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="db4ce-133">Da jedoch nicht alle Nachrichtenspeicheranbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="db4ce-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="db4ce-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="db4ce-134">Notes to callers</span></span>

<span data-ttu-id="db4ce-135">Sie können eine Empfängertabelle ändern, während sie geöffnet ist, indem Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db4ce-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="db4ce-136">**ModifyRecipients** fügt Empfänger hinzu, löscht Empfänger oder ändert Empfängereigenschaften.</span><span class="sxs-lookup"><span data-stu-id="db4ce-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db4ce-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db4ce-137">See also</span></span>



[<span data-ttu-id="db4ce-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="db4ce-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="db4ce-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="db4ce-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="db4ce-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="db4ce-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="db4ce-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="db4ce-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

