---
title: Bereitstellen von Benachrichtigungen für Nachrichtenspeicher-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3abb4ba67ff5f0cf2284fa9286b6968698877b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795333"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="b4818-103">Bereitstellen von Benachrichtigungen für Nachrichtenspeicher-Anbieter</span><span class="sxs-lookup"><span data-stu-id="b4818-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="b4818-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4818-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4818-105">Während Benachrichtigungen optional sind, werden sie ein sehr wichtiger Bestandteil der Anbieter eine gute Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b4818-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="b4818-106">Clientanwendungen und die MAPI-Warteschlange basieren auf Benachrichtigungen vom Anbieter für die Nachricht an eine gute Leistung beim Senden von ausgehenden Nachrichten oder Empfangen von eingehenden Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4818-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="b4818-107">Clients und die MAPI-Warteschlange können ohne Empfang von Benachrichtigungen aus der Nachricht Informationsdienst funktionieren, aber sie sind nicht in der Lage, Benutzer über Änderungen an den Nachrichtenspeicher, ohne sie zu informieren.</span><span class="sxs-lookup"><span data-stu-id="b4818-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="b4818-108">Dies bedeutet, die Benutzer werden nicht angezeigt, dass eine neue Nachrichten eingegangen sind, bis deren Clients als Nächstes des Nachrichtenspeicher wird geöffnet wird meistens Ordner.</span><span class="sxs-lookup"><span data-stu-id="b4818-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="b4818-109">Clients, die durch Aufrufen der Methode [IMsgStore::Advise](imsgstore-advise.md) für Benachrichtigungen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="b4818-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="b4818-110">Der Client übergibt ein [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle, eine Bitmaske dar, der angibt, welche Art von Benachrichtigungen der Client empfangen, interessiert ist und eine **EntryID** , der angibt, welches Objekt in der Nachricht Speichern der **Advise** Anforderung betrifft.</span><span class="sxs-lookup"><span data-stu-id="b4818-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="b4818-111">Treten relevanten Ereignisse im-Objekt (beispielsweise, wenn eine neue Nachricht in den Empfangsordner im Nachrichtenspeicher eingeht), sollte die Nachricht Speicheranbieter oder das Objekt selbst die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für alle die **aufrufen IMAPIAdviseSink** -Objekten, die für diesen Ereignistyp registriert haben.</span><span class="sxs-lookup"><span data-stu-id="b4818-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="b4818-112">Auch wenn Ihre Nachricht speichern benachrichtigt Anbieter nie andere MAPI-Komponenten über Änderungen an der Nachrichtenspeicher weiterhin **IMsgStore::Advise** zum Zurückgeben von MAPI_E_NO_SUPPORT implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4818-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="b4818-113">Andere Komponenten nicht zu erwarten, dass Benachrichtigungen aus der Nachricht Anbieter speichern weiß.</span><span class="sxs-lookup"><span data-stu-id="b4818-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4818-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4818-114">See also</span></span>



[<span data-ttu-id="b4818-115">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="b4818-115">Message Store Features</span></span>](message-store-features.md)

