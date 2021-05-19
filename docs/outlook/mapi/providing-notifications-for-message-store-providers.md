---
title: Bereitstellen von Benachrichtigungen für Store Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419933"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="c745b-103">Bereitstellen von Benachrichtigungen für Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="c745b-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="c745b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c745b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c745b-105">Obwohl Benachrichtigungen optional sind, sind sie ein sehr wichtiger Bestandteil eines guten Nachrichtenspeicheranbieters.</span><span class="sxs-lookup"><span data-stu-id="c745b-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="c745b-106">Clientanwendungen und der MAPI-Spooler sind auf Benachrichtigungen des Nachrichtenspeicheranbieters angewiesen, um eine gute Leistung beim Senden ausgehender Nachrichten oder beim Empfangen eingehender Nachrichten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c745b-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="c745b-107">Clients und der MAPI-Spooler können ohne Benachrichtigungen vom Nachrichtenspeicheranbieter funktionieren, aber sie können Benutzer nicht über Änderungen im Nachrichtenspeicher informieren, ohne sie.</span><span class="sxs-lookup"><span data-stu-id="c745b-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="c745b-108">In der Regel bedeutet dies, dass Benutzer erst dann sehen können, wenn eine neue Nachricht eingetroffen ist, bis ihr Client als Nächstes den Empfangsordner des Nachrichtenspeichers öffnet.</span><span class="sxs-lookup"><span data-stu-id="c745b-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="c745b-109">Clients registrieren sich für Benachrichtigungen, indem sie die [IMsgStore::Advise-Methode](imsgstore-advise.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c745b-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="c745b-110">Der Client übergibt eine [IMAPIAdviseSink : IUnknown-Schnittstelle,](imapiadvisesinkiunknown.md) eine Bitmaske, die angibt, welche Art von Benachrichtigungen der Client empfangen möchte, und eine **EntryID,** die angibt, für welches Objekt im Nachrichtenspeicher die **Advise-Anforderung** gilt.</span><span class="sxs-lookup"><span data-stu-id="c745b-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="c745b-111">Wenn relevante Ereignisse im Objekt auftreten (z. B. wenn eine neue Nachricht im Empfangsordner im Nachrichtenspeicher eintrifft), sollte der Nachrichtenspeicheranbieter oder das Objekt selbst die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für alle **IMAPIAdviseSink-Objekte** aufrufen, die für diesen Ereignistyp registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c745b-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="c745b-112">Auch wenn ihr Nachrichtenspeicheranbieter andere MAPI-Komponenten niemals über Änderungen im Nachrichtenspeicher benachrichtigt, sollte er dennoch **IMsgStore::Advise** implementieren, um MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c745b-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="c745b-113">Dadurch werden andere Komponenten informiert, dass sie keine Benachrichtigungen vom Nachrichtenspeicheranbieter erwarten.</span><span class="sxs-lookup"><span data-stu-id="c745b-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c745b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c745b-114">See also</span></span>



[<span data-ttu-id="c745b-115">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="c745b-115">Message Store Features</span></span>](message-store-features.md)

