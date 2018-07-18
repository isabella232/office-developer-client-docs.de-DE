---
title: Zuzuteilen Address Book-Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791791"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="e975c-103">Zuzuteilen Address Book-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="e975c-103">Handing address book notification</span></span>
  
<span data-ttu-id="e975c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e975c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e975c-105">Address Book Benachrichtigungen ermöglichen einen Client Hier erfahren, die Adressbuch Adresseintrag oder zu einem bestimmten Eintrag Auftreten von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="e975c-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="e975c-106">Sie können für diese Benachrichtigungen über das MAPI-Adressbuch durch Aufrufen von [IAddrBook::Advise](iaddrbook-advise.md) oder über ein Adressbuchcontainer Hierarchie oder Inhaltstabelle durch Aufrufen von [IMAPITable::Advise](imapitable-advise.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="e975c-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="e975c-107">Geben Sie den Eintrag Bezeichner eines Adressbuchcontainer, Verteilerliste oder messaging-Benutzer, wenn Sie für Benachrichtigungen auf einen bestimmten Eintrag und NULL registrieren, wenn für Benachrichtigungen auf das gesamte Adressbuch registrieren.</span><span class="sxs-lookup"><span data-stu-id="e975c-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="e975c-108">Die Eintrags-ID muss es sich um ein messaging-Benutzer oder eine Verteilerliste in einem Adressbuchcontainer darstellen.</span><span class="sxs-lookup"><span data-stu-id="e975c-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="e975c-109">**IAddrBook::Advise** untersucht dieses Eintrags-ID, um zu bestimmen, welche Adresse Adressbuchanbieter für das entsprechende Objekt zuständig ist, und leitet den Anruf an die entsprechenden-Adressbuchanbieter [IABLogon::Advise](iablogon-advise.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e975c-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="e975c-110">Clients können für die folgenden Typen von Ereignissen auf Adressbucheinträge registrieren:</span><span class="sxs-lookup"><span data-stu-id="e975c-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="e975c-111">Schwerwiegender Fehler</span><span class="sxs-lookup"><span data-stu-id="e975c-111">Critical error</span></span>
    
- <span data-ttu-id="e975c-112">Eines der Objektereignisse (erstellt, geändert, gelöscht, verschoben oder kopiert)</span><span class="sxs-lookup"><span data-stu-id="e975c-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="e975c-113">Tabelle geändert</span><span class="sxs-lookup"><span data-stu-id="e975c-113">Table modified</span></span>
    
<span data-ttu-id="e975c-114">In der Regel erfolgt Registrierung nur unter Address Book Containerinhalt und Hierarchietabellen.</span><span class="sxs-lookup"><span data-stu-id="e975c-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="e975c-115">Es ist nur in seltenen Fällen Clients mit der unteren Ebene messaging Benutzer- und Verteilung List-Objekten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e975c-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="e975c-116">Dies ist, da:</span><span class="sxs-lookup"><span data-stu-id="e975c-116">This is because:</span></span>
  
- <span data-ttu-id="e975c-117">Viele adressbuchanbietern implementierte unterstützen keine Benachrichtigungen ihrer messaging-Benutzern und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="e975c-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="e975c-118">Tabelle Benachrichtigungen reichen zum Nachverfolgen von Änderungen und Berichten sie Benutzern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e975c-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

