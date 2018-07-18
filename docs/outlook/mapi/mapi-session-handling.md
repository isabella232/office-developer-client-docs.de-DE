---
title: MAPI-Sitzung-Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793079"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="458a5-103">MAPI-Sitzung-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="458a5-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="458a5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="458a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="458a5-105">Bevor Sie mit der Dienstanbieter und einer zugrunde liegenden messaging-System kommunizieren können, müssen Sie eine Sitzung einrichten.</span><span class="sxs-lookup"><span data-stu-id="458a5-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="458a5-106">MAPI-Sitzung ist eine Verknüpfung von einem Client an andere MAPI-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="458a5-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="458a5-107">Als Ergebnis der erfolgreich starten einer Sitzung, MAPI gibt an die Clients einen Zeiger auf ein Sitzungsobjekt – ein Objekt, das die **IMAPISession** -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="458a5-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="458a5-108">Weitere Informationen finden Sie unter [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="458a5-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="458a5-109">Die Methoden des **IMAPISession** -Schnittstelle können Sie den Zugriff auf die Objekte der Address Book und Message-Anbieter, Zugriff auf mehrere Tabellen, Anzeigen von Formularen, Transport Anbietereigenschaften festlegen und Verwalten des Diensts Benutzerprofil und Nachricht ausführen.</span><span class="sxs-lookup"><span data-stu-id="458a5-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="458a5-110">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="458a5-110">In this section</span></span>

[<span data-ttu-id="458a5-111">Staren einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="458a5-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="458a5-112">Beschreibt, wie Sie eine MAPI-Sitzung zu starten, und enthält Links zu Themen mit Ausführlichere Informationen.</span><span class="sxs-lookup"><span data-stu-id="458a5-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="458a5-113">Beenden einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="458a5-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="458a5-114">Beschreibt, wie eine MAPI-Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="458a5-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="458a5-115">Zugreifen auf Objekte durch eine Sitzung</span><span class="sxs-lookup"><span data-stu-id="458a5-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="458a5-116">Beschreibt, wie einen Sitzung Zeiger verwenden, um die Sitzungsobjekte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="458a5-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="458a5-117">Abrufen der primären und Anbieteridentität</span><span class="sxs-lookup"><span data-stu-id="458a5-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="458a5-118">Beschreibt die Eigenschaften, die zum Abrufen von primären und Identity Provider.</span><span class="sxs-lookup"><span data-stu-id="458a5-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="458a5-119">Statustabelle und Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="458a5-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="458a5-120">Beschreibt das Zugreifen auf Informationen aus der Tabelle "Status".</span><span class="sxs-lookup"><span data-stu-id="458a5-120">Describes how to access information from the status table.</span></span>
    

