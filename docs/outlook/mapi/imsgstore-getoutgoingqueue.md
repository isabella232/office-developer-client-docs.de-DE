---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792632"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="5e217-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="5e217-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="5e217-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e217-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e217-105">Bietet Zugriff auf ausgehende Warteschlangentabelle eine Tabelle mit Informationen über alle Nachrichten in der Nachrichtenspeicher ausgehenden Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5e217-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="5e217-106">Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e217-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5e217-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e217-107">Parameters</span></span>

 <span data-ttu-id="5e217-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e217-108">_ulFlags_</span></span>
  
> <span data-ttu-id="5e217-109">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="5e217-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5e217-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5e217-110">_lppTable_</span></span>
  
> <span data-ttu-id="5e217-111">[out] Ein Zeiger auf einen Zeiger auf die ausgehende Warteschlangentabelle.</span><span class="sxs-lookup"><span data-stu-id="5e217-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e217-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5e217-112">Return value</span></span>

<span data-ttu-id="5e217-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e217-113">S_OK</span></span> 
  
> <span data-ttu-id="5e217-114">Die ausgehende Warteschlangentabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e217-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e217-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e217-115">Remarks</span></span>

<span data-ttu-id="5e217-116">Die **IMsgStore::GetOutgoingQueue** -Methode enthält die MAPI-Warteschlange mit Zugriff auf die Tabelle, die die Nachrichtenspeicher-Warteschlange von ausgehenden Nachrichten anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5e217-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="5e217-117">Nachrichten werden in der Regel in der ausgehenden Warteschlangentabelle platziert, nach deren [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5e217-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="5e217-118">Allerdings, da die Reihenfolge der Übermittlung die Reihenfolge der vorverarbeitung und Übermittlung an der Adressbuchhierarchie betroffen sind, möglicherweise einige Nachrichten, die für das Senden von gekennzeichnet wurden nicht in der ausgehenden Warteschlangentabelle sofort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e217-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5e217-119">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="5e217-119">Notes to implementers</span></span>

<span data-ttu-id="5e217-120">Eine Liste der Eigenschaften, die als Spalten in der ausgehenden Warteschlangentabelle enthalten sein müssen, finden Sie unter [Ausgehende Warteschlange Tabellen](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5e217-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="5e217-121">Da die MAPI-Warteschlange zum Akzeptieren von Nachrichten von einem Nachrichtenspeicher in aufsteigender Reihenfolge der Zeitpunkt der Übermittlung ausgelegt ist, entweder zulassen Sie die MAPI-Warteschlange zum Sortieren der ausgehenden Warteschlangentabelle, um diesen Auftrag übereinstimmen oder diese als die standardmäßige Sortierreihenfolge einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5e217-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="5e217-122">Sie müssen Unterstützung Benachrichtigungen für ausgehende Nachrichten Warteschlange-Tabelle, um sicherzustellen, dass die MAPI-Warteschlange benachrichtigt wird, wenn der Inhalt der Warteschlange ändern.</span><span class="sxs-lookup"><span data-stu-id="5e217-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e217-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e217-123">See also</span></span>



[<span data-ttu-id="5e217-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5e217-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="5e217-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5e217-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

