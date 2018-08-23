---
title: MAPI-Dienstanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1f931382e790da13e7d4a746e286d9dc176b7b6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571906"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="35454-103">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="35454-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="35454-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35454-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35454-105">Es gibt drei gängige Typen der Dienstanbieter:</span><span class="sxs-lookup"><span data-stu-id="35454-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="35454-106">Beheben von adressbuchanbietern implementierte.</span><span class="sxs-lookup"><span data-stu-id="35454-106">Address book providers.</span></span>
    
- <span data-ttu-id="35454-107">Nachricht-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="35454-107">Message store providers.</span></span>
    
- <span data-ttu-id="35454-108">Transport-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="35454-108">Transport providers.</span></span>
    
<span data-ttu-id="35454-109">Address Book und Message-Anbieter müssen viele ähnlichkeiten.</span><span class="sxs-lookup"><span data-stu-id="35454-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="35454-110">Registrieren sie einen eindeutigen Bezeichner MAPI, die sie zum Erstellen von Eintragsbezeichner für Objekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="35454-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="35454-111">Sie bieten eine Hierarchie von Objekten und Eigenschaften, die Clients zugreifen und diese bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="35454-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="35454-112">Für ihre Containerobjekte unterstützen sie eine Hierarchie und einer Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="35454-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="35454-113">Sie unterstützen ereignisbenachrichtigung zu diesen Tabellen und optional für einzelne Objekte, damit Clients über Änderungen informiert werden können, die während der Sitzung auftreten.</span><span class="sxs-lookup"><span data-stu-id="35454-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="35454-114">Wenn Vorgänge langen werden, können sie eine Statusanzeige um informieren den Benutzer über den Vorgang Status anzeigen.</span><span class="sxs-lookup"><span data-stu-id="35454-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="35454-115">Können Clients kommunizieren mit Address Book und Message-Anbieter entweder indirekt über MAPI mithilfe der [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) und [IMAPISession: IUnknown](imapisessioniunknown.md) Schnittstellen oder direkt mithilfe eines der Service Provider-Schnittstellen in der in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="35454-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="35454-116">**Address Book Provider-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="35454-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="35454-117">**Nachricht Store Provider-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="35454-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35454-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="35454-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="35454-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35454-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="35454-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="35454-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="35454-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="35454-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="35454-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35454-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="35454-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35454-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="35454-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35454-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="35454-125">Transportanbieter unterscheiden sich von Adresse Adressbuch und Nachricht Speicher-Anbieter in die Möglichkeit, den, die Sie mit MAPI- und -Clients kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="35454-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="35454-126">In der Regel warten Transportanbieter MAPI, um Informationen dazu auffordern, anstatt Kommunikation zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="35454-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="35454-127">Im Gegensatz zu anderen Anbietern unterstützt Transportanbieter keine Vielzahl von Objekten und Tabellen, die von Clients häufig zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="35454-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="35454-128">Allerdings unterstützen sie ein Statusobjekt wie alle-Dienstanbieter, und seine Eigenschaften in der Statustabelle veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="35454-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="35454-129">Während Address Book und Message-Anbieter die [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode zum Registrieren der eindeutige Bezeichner für die Erstellung ihrer Eintragsbezeichner aufrufen, rufen Sie Transportanbieter die [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode Registrieren Sie sich eindeutige Bezeichner als auch-Adresstypen für die Verantwortung für die Übermittlung von bestimmten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="35454-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="35454-130">Ihren Dienstanbieter müssen drei Headerdateien: eine öffentliche Headerdatei und zwei interne Dateien.</span><span class="sxs-lookup"><span data-stu-id="35454-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="35454-131">Verwenden Sie die öffentlichen Header-Datei aus, für die Konfiguration und zum Dokumentieren von Eigenschaften und deren Werten.</span><span class="sxs-lookup"><span data-stu-id="35454-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="35454-132">Enthalten Sie in einem der internen Headerdateien alle erforderlichen öffentlichen MAPI-Header. Diese Headerdatei sollte in allen der Service Provider Quelldateien enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="35454-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="35454-133">Verwenden Sie die anderen interne Datei Resource Identifier definieren.</span><span class="sxs-lookup"><span data-stu-id="35454-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="35454-134">Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="35454-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="35454-135">Geben Sie eine Eintrag-Funktion.</span><span class="sxs-lookup"><span data-stu-id="35454-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="35454-136">Geben Sie ein Anbieter und Anmeldeobjekt zur Verarbeitung von Anmelde- und Initialisierung an.</span><span class="sxs-lookup"><span data-stu-id="35454-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="35454-137">Wenn der Anbieter eine Message Service gehört, geben Sie eine Nachricht Service Entry Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="35454-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="35454-138">Konfiguration durch die Implementierung eines Eigenschaftenblatts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35454-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="35454-139">Implementieren Sie ein Statusobjekt und Unterstützung der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="35454-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="35454-140">Handle Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="35454-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35454-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35454-141">See also</span></span>



[<span data-ttu-id="35454-142">MAPI-Konzepte</span><span class="sxs-lookup"><span data-stu-id="35454-142">MAPI Concepts</span></span>](mapi-concepts.md)

