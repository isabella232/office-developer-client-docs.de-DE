---
title: Langfristige-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792912"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="53e7c-103">Langfristige-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="53e7c-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="53e7c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53e7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53e7c-105">Langfristige Eintrags-ID wird von einem Dienstanbieter zu einem Objekt zugewiesen, wenn ein Objekt einen Bezeichner mit längerer Lebensdauer erfordert.</span><span class="sxs-lookup"><span data-stu-id="53e7c-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="53e7c-106">Langfristige-Eintragsbezeichner sind immer für Wochen oder Monate gültig und können auf anderen Arbeitsstationen, je nach den Anbieter gültig sein.</span><span class="sxs-lookup"><span data-stu-id="53e7c-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="53e7c-107">Die langfristige Bezeichner von adressbuchanbietern implementierte für benutzerdefinierte Empfänger erstellt sind universell gültig.</span><span class="sxs-lookup"><span data-stu-id="53e7c-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="53e7c-108">Langfristige-Eintragsbezeichner werden Nachrichtenspeicher, Ordner, Nachrichten, Address Book Containern, messaging-Benutzer und Verteilung Listen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="53e7c-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="53e7c-109">Wenn Clientanwendungen die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode dieser Objekte aufrufen, ist es immer eine langfristige Eintrags-ID, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="53e7c-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="53e7c-110">Langfristige-Eintragsbezeichner müssen für alle Nachrichtenspeicher in das aktive Profil eindeutig sein; aus diesem Grund, wenn eine Nachricht oder einen Ordner aus einem Informationsspeicher in eine andere kopiert werden, muss es eine neuen Eintrags-ID zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="53e7c-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="53e7c-111">Wenn eine Nachricht Store-Objekt verschoben wird, bestimmt der Nachricht Speicher-Anbieter, der die Verschiebung implementiert, ob die ursprüngliche Eintrags-ID gültig ist.</span><span class="sxs-lookup"><span data-stu-id="53e7c-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="53e7c-112">Einige Dienstanbieter weisen Sie neue-Eintragsbezeichner verschobene Objekte; andere nicht.</span><span class="sxs-lookup"><span data-stu-id="53e7c-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="53e7c-113">Wenn eine Änderung vorhanden ist, wird die neuen Eintrags-ID in die Informationen an die Clients übergeben wird, wenn sie, der die Verschiebung benachrichtigt werden enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="53e7c-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="53e7c-114">Nachricht Anbieter implementieren in der Regel das folgende Verhalten beim Verschieben von Ordnern:</span><span class="sxs-lookup"><span data-stu-id="53e7c-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="53e7c-115">Wenn ein Ordner an einen anderen Informationsspeicher eines anderen Typs aus einem Informationsspeicher verschoben wird, wird die Eintrags-ID unbedingt ändern.</span><span class="sxs-lookup"><span data-stu-id="53e7c-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="53e7c-116">Wenn Sie ein Ordner aus einem Informationsspeicher in einen anderen Speicher des gleichen Typs verschoben wird, ändert die Eintrags-ID fast immer.</span><span class="sxs-lookup"><span data-stu-id="53e7c-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="53e7c-117">Wenn Sie ein Ordner an einen anderen Speicherort innerhalb der gleichen Nachrichtenspeicher verschoben wurde, die Eintrags-ID möglicherweise oder möglicherweise nicht geändert, je nach Anbieter die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="53e7c-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="53e7c-118">Umbenennen eines Ordners in der Regel ohne seines übergeordneten Ordners bewirkt keine Eintrags-ID zu ändern.</span><span class="sxs-lookup"><span data-stu-id="53e7c-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53e7c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e7c-119">See also</span></span>



[<span data-ttu-id="53e7c-120">MAPI-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="53e7c-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

