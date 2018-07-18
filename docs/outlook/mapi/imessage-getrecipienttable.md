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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792513"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="59a51-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="59a51-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="59a51-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59a51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59a51-105">Gibt die Empfänger der Nachricht-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="59a51-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="59a51-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59a51-106">Parameters</span></span>

 <span data-ttu-id="59a51-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59a51-107">_ulFlags_</span></span>
  
> <span data-ttu-id="59a51-108">[in] Bitmaske aus Flags, die die Rückgabe von der Tabelle steuert.</span><span class="sxs-lookup"><span data-stu-id="59a51-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="59a51-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="59a51-109">The following flags can be set:</span></span>
    
<span data-ttu-id="59a51-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="59a51-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="59a51-111">Ermöglicht **GetRecipientTable** erfolgreich, möglicherweise beendet, bevor die Tabelle vollständig an den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="59a51-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="59a51-112">Wenn die Tabelle nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="59a51-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="59a51-113">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59a51-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="59a51-114">Zeichenfolgenspalten sollte im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="59a51-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="59a51-115">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgenspalten im ANSI-Format sein.</span><span class="sxs-lookup"><span data-stu-id="59a51-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="59a51-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="59a51-116">_lppTable_</span></span>
  
> <span data-ttu-id="59a51-117">[out] Zeiger auf einen Zeiger auf die Empfänger Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59a51-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59a51-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="59a51-118">Return value</span></span>

<span data-ttu-id="59a51-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="59a51-119">S_OK</span></span> 
  
> <span data-ttu-id="59a51-120">Die Empfänger Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59a51-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59a51-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59a51-121">Remarks</span></span>

<span data-ttu-id="59a51-122">Die **IMessage::GetRecipientTable** -Methode gibt einen Zeiger auf Empfänger die Nachricht-Tabelle, die Informationen zu allen der Empfänger der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="59a51-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="59a51-123">Es wird eine Zeile für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="59a51-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="59a51-124">Empfänger Tabellen ist eine andere Spalte festlegen, je nachdem, ob die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="59a51-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="59a51-125">Eine vollständige Liste der Spalten in einer Tabelle Empfänger finden Sie unter [Empfänger Tabellen](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="59a51-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="59a51-126">Einige Empfänger Tabellen unterstützt eine Vielzahl von Einschränkungen. andere nicht.</span><span class="sxs-lookup"><span data-stu-id="59a51-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="59a51-127">Unterstützung für Einschränkungen hängt von der Nachricht Informationsdienst Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="59a51-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="59a51-128">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf die folgenden Aufrufe an die Empfänger Tabelle aus:</span><span class="sxs-lookup"><span data-stu-id="59a51-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="59a51-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) zum Abrufen der Spalte festlegen.</span><span class="sxs-lookup"><span data-stu-id="59a51-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="59a51-130">[IMAPITable::QueryRows](imapitable-queryrows.md) abzurufenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="59a51-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="59a51-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) , um die Sortierreihenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="59a51-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="59a51-132">Durch Festlegen der Unicode-Flag-Anforderungen, die die Informationen für alle diese aufrufen zurückgegebenen Zeichenfolgenspalten im Unicode-Format sein.</span><span class="sxs-lookup"><span data-stu-id="59a51-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="59a51-133">Da nicht alle Nachricht Anbieter Unicode unterstützen, ist jedoch festlegen dieses Flag nur eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="59a51-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="59a51-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="59a51-134">Notes to callers</span></span>

<span data-ttu-id="59a51-135">Sie können eine Empfänger Tabelle ändern, während es geöffnet ist, indem Sie die [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="59a51-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="59a51-136">**ModifyRecipients** Fügt Empfänger, löscht Empfänger oder Empfängereigenschaften ändert.</span><span class="sxs-lookup"><span data-stu-id="59a51-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59a51-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59a51-137">See also</span></span>



[<span data-ttu-id="59a51-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="59a51-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="59a51-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="59a51-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="59a51-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="59a51-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="59a51-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="59a51-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

