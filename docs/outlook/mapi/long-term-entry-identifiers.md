---
title: Langfristige EintragsBezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307784"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="1cb5e-103">Langfristige EintragsBezeichner</span><span class="sxs-lookup"><span data-stu-id="1cb5e-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="1cb5e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cb5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cb5e-105">Ein langfristiger Eintragsbezeichner wird einem Objekt von einem Dienstanbieter zugewiesen, wenn für ein Objekt ein Bezeichner mit einer längeren Lebensdauer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="1cb5e-106">Langfristige Eintrags-IDs sind immer für Wochen oder Monate gültig und können auf anderen Arbeitsstationen abhängig vom Anbieter gültig sein.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="1cb5e-107">Die langfristigen Bezeichner, die von Adressbuch Anbietern für benutzerdefinierte Empfänger erstellt wurden, sind universell gültig.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="1cb5e-108">Langfristige Eintrags-IDs werden Nachrichten speichern, Ordnern, Nachrichten, Adressbuch Containern, Messaging Benutzern und Verteilerlisten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="1cb5e-109">Wenn Clientanwendungen die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode dieser Objekte aufrufen, wird immer eine langfristige Eintrags-ID zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="1cb5e-110">Langfristige Eintrags-IDs müssen für alle Nachrichtenspeicher im aktiven Profil eindeutig sein. Wenn eine Nachricht oder ein Ordner aus einem Nachrichtenspeicher in einen anderen kopiert wird, muss daher eine neue Eintrags-ID zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="1cb5e-111">Wenn ein Nachrichtenspeicherobjekt verschoben wird, bestimmt der Nachrichtenspeicher Anbieter, der die Verschiebung implementiert, ob der ursprüngliche Eintragsbezeichner gültig bleibt.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="1cb5e-112">Einige Dienstanbieter weisen verschobene Objekte neue Eintrags-IDs zu; andere nicht.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="1cb5e-113">Wenn eine Änderung vorliegt, wird die neue Eintrags-ID in die Informationen eingeschlossen, die an Clients übergeben werden, wenn Sie über die Verschiebung benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="1cb5e-114">In der Regel implementieren Nachrichtenspeicher Anbieter beim Verschieben von Ordnern das folgende Verhalten:</span><span class="sxs-lookup"><span data-stu-id="1cb5e-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="1cb5e-115">Wenn ein Ordner aus einem Nachrichtenspeicher in einen anderen Speicher eines anderen Typs verschoben wird, wird die Eintrags-ID garantiert geändert.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="1cb5e-116">Wenn ein Ordner aus einem Nachrichtenspeicher in einen anderen Speicher desselben Typs verschoben wird, ändert sich die Eintrags-ID fast immer.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="1cb5e-117">Wenn ein Ordner an einen anderen Speicherort innerhalb desselben Nachrichtenspeichers verschoben wird, ändert sich möglicherweise die Eintrags-ID je nach Nachrichtenspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="1cb5e-118">Wenn Sie einen Ordner umbenennen, ohne den übergeordneten Ordner zu ändern, wird der Eintragsbezeichner in der Regel nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="1cb5e-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1cb5e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cb5e-119">See also</span></span>



[<span data-ttu-id="1cb5e-120">MAPI-Eintrags-IDs</span><span class="sxs-lookup"><span data-stu-id="1cb5e-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

