---
title: Bereitstellen von Benachrichtigungen für Nachrichtenspeicher Anbieter
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
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="6a018-103">Bereitstellen von Benachrichtigungen für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="6a018-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="6a018-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a018-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a018-105">Während Benachrichtigungen optional sind, sind Sie ein sehr wichtiger Teil eines guten Nachrichtenspeicher Anbieters.</span><span class="sxs-lookup"><span data-stu-id="6a018-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="6a018-106">Client Anwendungen und der MAPI-Spooler verwenden Benachrichtigungen des Nachrichtenspeicher Anbieters, um beim Übermitteln ausgehender Nachrichten oder empfangen von eingehenden Nachrichten eine gute Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="6a018-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="6a018-107">Clients und der MAPI-Spooler können ohne Benachrichtigung des Nachrichtenspeicher Anbieters funktionieren, Sie können jedoch keine Benutzer über Änderungen im Nachrichtenspeicher informieren.</span><span class="sxs-lookup"><span data-stu-id="6a018-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="6a018-108">In der Regel ist dies der Fall, dass Benutzer nicht erkennen können, dass eine neue Nachricht eingegangen ist, bis Ihr Client als nächstes den Empfangsordner des Nachrichtenspeichers öffnet.</span><span class="sxs-lookup"><span data-stu-id="6a018-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="6a018-109">Clients registrieren sich für Benachrichtigungen, indem Sie die [IMsgStore:: Advise](imsgstore-advise.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6a018-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="6a018-110">Der Client übergibt eine [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle, eine Bitmaske, die angibt, welche Art von Benachrichtigungen der Client erhalten soll, \*\*\*\* und ein Eintrags-Nr., der angibt, welches Objekt im Nachrichtenspeicher die **Advise** Request gilt für.</span><span class="sxs-lookup"><span data-stu-id="6a018-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="6a018-111">Wenn im Objekt relevante Ereignisse auftreten (beispielsweise, wenn eine neue Nachricht im empfangenden Ordner im Nachrichtenspeicher eingeht), sollte der Nachrichtenspeicher Anbieter oder das Objekt selbst die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für alle \*\* IMAPIAdviseSink\*\* -Objekte, die für diesen Ereignistyp registriert sind.</span><span class="sxs-lookup"><span data-stu-id="6a018-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="6a018-112">Auch wenn der Nachrichtenspeicher Anbieter keine anderen MAPI-Komponenten von Änderungen im Nachrichtenspeicher benachrichtigt, sollte er weiterhin **IMsgStore:: Advise** implementieren, um MAPI_E_NO_SUPPORT zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6a018-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="6a018-113">Dadurch werden andere Komponenten informiert, dass keine Benachrichtigungen vom Nachrichtenspeicher Anbieter erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="6a018-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a018-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a018-114">See also</span></span>



[<span data-ttu-id="6a018-115">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="6a018-115">Message Store Features</span></span>](message-store-features.md)

