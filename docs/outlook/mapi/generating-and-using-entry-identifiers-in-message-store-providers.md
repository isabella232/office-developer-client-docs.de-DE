---
title: Generieren und Verwenden von Eintragsbezeichner in Nachricht speichern-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3bfda4a1dbe464c744917c2e9b3ca66eaf88fd20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791792"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="99a4c-103">Generieren und Verwenden von Eintragsbezeichner in Nachricht speichern-Anbieter</span><span class="sxs-lookup"><span data-stu-id="99a4c-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="99a4c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99a4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99a4c-105">Wenn Sie einen neuen Ordner oder Nachricht in einem Nachrichtenspeicher erstellt wird, hat der Nachricht Speicheranbieter dieses Objekt eines Eintrags-ID zugewiesen, sodass Clientanwendungen darauf verweisen können.</span><span class="sxs-lookup"><span data-stu-id="99a4c-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="99a4c-106">Nachricht-Anbieter können die außer Kraft gesetzten langfristige-Eintragsbezeichner von gelöschten Objekten wiederverwenden oder erstellen neue IDs.</span><span class="sxs-lookup"><span data-stu-id="99a4c-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="99a4c-107">Es gibt keine Anforderung unidirektional oder das andere für die Nachricht-Anbieter. jedoch, wenn es möglich ist, sollte eine Nachricht Speicheranbieter immer neue langfristige Eintragsbezeichner für neue Objekte, sondern Wiederverwenden von alten generieren.</span><span class="sxs-lookup"><span data-stu-id="99a4c-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="99a4c-108">Es ist kein Problem kurzfristige-Eintragsbezeichner wiederverwendet, wenn die Objekte, denen sie referenzieren gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="99a4c-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="99a4c-109">Der Grund für diese Löschung ist, dass Clients Eintragsbezeichner, manchmal für längere Zeit zwischengespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="99a4c-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="99a4c-110">Wenn in diesem Fall der Nachricht Speicheranbieter Eintragsbezeichner wiederverwenden, ist es möglich, für die Eintrags-ID für ein anderes Objekt zu verweisen, wenn der Client die Eintrags-ID öffnet, als wenn es zuerst die Eintrags-ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="99a4c-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="99a4c-111">Wenn die Nachricht Informationsdienst nicht Eintragsbezeichner wieder verwenden – oder mindestens ein Eintrag Bezeichner Generation Schema verwendet, die nicht sehr lange wiederholt wird – dieses Problem kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="99a4c-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="99a4c-112">In ähnlicher Weise sollten Nachricht Anbieter Eintragsbezeichner für Ordner und Nachrichten beibehalten, wenn sie im Nachrichtenspeicher verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="99a4c-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="99a4c-113">Wenn der Nachricht Speicheranbieter dies möglich ist, werden Verweise auf Objekte im Speicher nicht ungültig, wenn das Objekt an eine andere Position im Speicher verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="99a4c-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99a4c-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99a4c-114">See also</span></span>

- [<span data-ttu-id="99a4c-115">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="99a4c-115">Message Store Features</span></span>](message-store-features.md)

