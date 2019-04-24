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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349280"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="38c39-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="38c39-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="38c39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38c39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38c39-105">Gibt die Empfängertabelle der Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="38c39-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="38c39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38c39-106">Parameters</span></span>

 <span data-ttu-id="38c39-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38c39-107">_ulFlags_</span></span>
  
> <span data-ttu-id="38c39-108">in Bitmaske von Flags, die die Rückgabe der Tabelle steuert.</span><span class="sxs-lookup"><span data-stu-id="38c39-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="38c39-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="38c39-109">The following flags can be set:</span></span>
    
<span data-ttu-id="38c39-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="38c39-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="38c39-111">Ermöglicht \*\*\*\* getrecipientable, um erfolgreich zurückzugeben, möglicherweise bevor die Tabelle vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="38c39-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="38c39-112">Wenn die Tabelle nicht verfügbar ist, kann der nachfolgende Aufruf einen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="38c39-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="38c39-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="38c39-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="38c39-114">Zeichenfolgenspalten sollten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="38c39-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="38c39-115">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgenspalten im ANSI-Format sein.</span><span class="sxs-lookup"><span data-stu-id="38c39-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="38c39-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="38c39-116">_lppTable_</span></span>
  
> <span data-ttu-id="38c39-117">Out Zeiger auf einen Zeiger auf die Empfängertabelle.</span><span class="sxs-lookup"><span data-stu-id="38c39-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38c39-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38c39-118">Return value</span></span>

<span data-ttu-id="38c39-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="38c39-119">S_OK</span></span> 
  
> <span data-ttu-id="38c39-120">Die Empfängertabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38c39-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38c39-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38c39-121">Remarks</span></span>

<span data-ttu-id="38c39-122">Die **IMessage::** getrecipientable-Methode gibt einen Zeiger auf die Empfängertabelle der Nachricht zurück, die Informationen zu allen Empfängern der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="38c39-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="38c39-123">Es gibt eine Zeile für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="38c39-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="38c39-124">Empfänger Tabellen haben unterschiedliche Spaltensätze, je nachdem, ob die Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="38c39-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="38c39-125">Eine vollständige Liste der Spalten in einer Empfängertabelle finden Sie unter [Recipient Tables](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="38c39-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="38c39-126">Einige Empfänger Tabellen unterstützen eine Vielzahl von Einschränkungen; andere nicht.</span><span class="sxs-lookup"><span data-stu-id="38c39-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="38c39-127">Die Unterstützung von Einschränkungen hängt von der Implementierung des Nachrichtenspeicher Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="38c39-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="38c39-128">Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf die folgenden Aufrufe der Recipient-Tabelle aus:</span><span class="sxs-lookup"><span data-stu-id="38c39-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="38c39-129">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) zum Abrufen des Spaltensatzes.</span><span class="sxs-lookup"><span data-stu-id="38c39-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="38c39-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) zum Abrufen von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="38c39-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="38c39-131">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="38c39-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="38c39-132">Durch Festlegen des Unicode-Kennzeichens wird angefordert, dass die Informationen für Zeichenfolgenspalten, die von diesen Aufrufen zurückgegeben werden, im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="38c39-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="38c39-133">Da jedoch nicht alle Nachrichtenspeicher Anbieter Unicode unterstützen, ist das Festlegen dieses Kennzeichens nur eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="38c39-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="38c39-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="38c39-134">Notes to callers</span></span>

<span data-ttu-id="38c39-135">Sie können eine Empfängertabelle ändern, während Sie geöffnet ist, indem Sie die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="38c39-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="38c39-136">**ModifyRecipients** fügt Empfänger hinzu, löscht Empfänger oder ändert Empfänger Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="38c39-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38c39-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38c39-137">See also</span></span>



[<span data-ttu-id="38c39-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="38c39-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="38c39-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="38c39-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="38c39-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="38c39-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="38c39-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="38c39-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

