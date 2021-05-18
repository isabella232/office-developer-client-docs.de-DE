---
title: Behandeln von Adressbuchbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413535"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="3abe3-103">Behandeln von Adressbuchbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3abe3-103">Handing address book notification</span></span>
  
<span data-ttu-id="3abe3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3abe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3abe3-105">Adressbuchbenachrichtigungen ermöglichen es einem Client, von Ereignissen zu erfahren, die für jeden Adressbucheintrag oder für einen bestimmten Eintrag auftreten.</span><span class="sxs-lookup"><span data-stu-id="3abe3-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="3abe3-106">Sie können sich für diese Benachrichtigungen entweder über das MAPI-Adressbuch registrieren, indem Sie [IAddrBook::Advise](iaddrbook-advise.md) aufrufen oder die Hierarchie- oder Inhaltstabelle eines Adressbuchcontainers über [IMAPITable::Advise aufrufen.](imapitable-advise.md)</span><span class="sxs-lookup"><span data-stu-id="3abe3-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="3abe3-107">Geben Sie die Eintrags-ID eines Adressbuchcontainers, einer Verteilerliste oder eines Messagingbenutzers an, wenn Sie sich für Benachrichtigungen für einen bestimmten Eintrag registrieren, und NULL, wenn Sie sich für Benachrichtigungen im gesamten Adressbuch registrieren.</span><span class="sxs-lookup"><span data-stu-id="3abe3-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="3abe3-108">Der Eintragsbezeichner muss einen Messagingbenutzer oder eine Verteilerliste in einem Adressbuchcontainer darstellen.</span><span class="sxs-lookup"><span data-stu-id="3abe3-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="3abe3-109">**IAddrBook::Advise** untersucht diesen Eintragsbezeichner, um zu bestimmen, welcher Adressbuchanbieter für das entsprechende Objekt verantwortlich ist, und gibt den Aufruf an die [IABLogon::Advise-Methode](iablogon-advise.md) des entsprechenden Adressbuchanbieters weiter.</span><span class="sxs-lookup"><span data-stu-id="3abe3-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="3abe3-110">Clients können sich für die folgenden Ereignistypen für Adressbucheinträge registrieren:</span><span class="sxs-lookup"><span data-stu-id="3abe3-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="3abe3-111">Kritischer Fehler</span><span class="sxs-lookup"><span data-stu-id="3abe3-111">Critical error</span></span>
    
- <span data-ttu-id="3abe3-112">Alle Objektereignisse (erstellt, geändert, gelöscht, verschoben oder kopiert)</span><span class="sxs-lookup"><span data-stu-id="3abe3-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="3abe3-113">Tabelle geändert</span><span class="sxs-lookup"><span data-stu-id="3abe3-113">Table modified</span></span>
    
<span data-ttu-id="3abe3-114">In der Regel erfolgt die Registrierung nur für Adressbuchcontainerinhalte und Hierarchietabellen.</span><span class="sxs-lookup"><span data-stu-id="3abe3-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="3abe3-115">Es ist selten, dass Clients sich bei den Messagingbenutzer- und Verteilerlistenobjekten der unteren Ebene registrieren.</span><span class="sxs-lookup"><span data-stu-id="3abe3-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="3abe3-116">Dies liegt daran, dass:</span><span class="sxs-lookup"><span data-stu-id="3abe3-116">This is because:</span></span>
  
- <span data-ttu-id="3abe3-117">Viele Adressbuchanbieter unterstützen keine Benachrichtigungen für ihre Messagingbenutzer und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="3abe3-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="3abe3-118">Tabellenbenachrichtigungen sind ausreichend, um Änderungen zu verfolgen und sie benutzern zu melden.</span><span class="sxs-lookup"><span data-stu-id="3abe3-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

