---
title: MAPI-Dienstanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346676"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="3645e-103">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3645e-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="3645e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3645e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3645e-105">Es gibt drei gängige Typen von Dienstanbietern:</span><span class="sxs-lookup"><span data-stu-id="3645e-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="3645e-106">Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="3645e-106">Address book providers.</span></span>
    
- <span data-ttu-id="3645e-107">Nachrichtenspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3645e-107">Message store providers.</span></span>
    
- <span data-ttu-id="3645e-108">Transport Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3645e-108">Transport providers.</span></span>
    
<span data-ttu-id="3645e-109">Adressbuch-und Nachrichtenspeicher Anbieter haben viele Ähnlichkeiten.</span><span class="sxs-lookup"><span data-stu-id="3645e-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="3645e-110">Sie registrieren einen eindeutigen Bezeichner mit MAPI, den Sie zum Erstellen von Eintrags Bezeichnern für Ihre Objekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="3645e-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="3645e-111">Sie bieten eine Hierarchie von Objekten und Eigenschaften, auf die Clients zugreifen und diese bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="3645e-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="3645e-112">Für Ihre Container-Objekte unterstützen Sie eine Hierarchietabelle und eine Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="3645e-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="3645e-113">Sie unterstützen Ereignisbenachrichtigungen für diese Tabellen und optional für einzelne Objekte, sodass Clients über Änderungen informiert werden können, die während der Sitzung stattfinden.</span><span class="sxs-lookup"><span data-stu-id="3645e-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="3645e-114">Wenn Vorgänge langwierig werden, können Sie eine Statusanzeige anzeigen, um den Benutzer über den Status des Vorgangs zu informieren.</span><span class="sxs-lookup"><span data-stu-id="3645e-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="3645e-115">Clients können mit Adressbuch-und Nachrichtenspeicher Anbietern entweder indirekt über MAPI kommunizieren, indem Sie die [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) und [IMAPISession: IUnknown](imapisessioniunknown.md) -Schnittstellen verwenden oder direkt über eine der Dienstanbieter Schnittstellen in der folgende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3645e-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="3645e-116">**Schnittstellen des Adressbuch Anbieters**</span><span class="sxs-lookup"><span data-stu-id="3645e-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="3645e-117">**Schnittstellen des Nachrichtenspeicher Anbieters**</span><span class="sxs-lookup"><span data-stu-id="3645e-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3645e-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3645e-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="3645e-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3645e-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="3645e-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3645e-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="3645e-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3645e-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="3645e-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3645e-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="3645e-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3645e-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="3645e-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3645e-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="3645e-125">Transport Anbieter unterscheiden sich von Adressbuch-und Nachrichtenspeicher Anbietern bei der Kommunikation mit MAPI und mit Clients.</span><span class="sxs-lookup"><span data-stu-id="3645e-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="3645e-126">Transport Anbieter warten in der Regel, bis MAPI Sie zur Information auffordert, statt die Kommunikation zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="3645e-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="3645e-127">Im Gegensatz zu anderen Anbietern unterstützen Transportanbieter keine Vielzahl von Objekten und Tabellen, auf die häufig Clients zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3645e-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="3645e-128">Sie unterstützen jedoch ein Status-Objekt, wie alle Dienstanbieter, und veröffentlichen die Eigenschaften in der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="3645e-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="3645e-129">Während Adressbuch-und Nachrichtenspeicher Anbieter die [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode aufrufen, um eindeutige Bezeichner für die Erstellung Ihrer Eintragsbezeichner zu registrieren, rufen Transportanbieter die [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode auf, um Registrieren Sie eindeutige Bezeichner sowie Adresstypen für die Übernahme der Verantwortung für die Bereitstellung bestimmter Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3645e-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="3645e-130">Der Dienstanbieter sollte drei Headerdateien haben: eine öffentliche Headerdatei und zwei interne Dateien.</span><span class="sxs-lookup"><span data-stu-id="3645e-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="3645e-131">Verwenden Sie die öffentliche Headerdatei zur Konfiguration und zum Dokumentieren von Eigenschaften und deren Werten.</span><span class="sxs-lookup"><span data-stu-id="3645e-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="3645e-132">Fügen Sie in eine der internen Headerdateien alle erforderlichen öffentlichen MAPI-Header ein. Diese Headerdatei sollte in allen Dienstanbieter-Quelldateien enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3645e-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="3645e-133">Verwenden Sie die andere interne Datei, um Ressourcen-IDs zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3645e-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="3645e-134">Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="3645e-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="3645e-135">Geben Sie eine Einstiegspunktfunktion an.</span><span class="sxs-lookup"><span data-stu-id="3645e-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="3645e-136">Geben Sie einen Anbieter und ein Anmeldeobjekt an, um die Anmeldung und Initialisierung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="3645e-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="3645e-137">Wenn der Anbieter zu einem Nachrichtendienst gehört, geben Sie eine Einstiegspunktfunktion für den Nachrichtendienst ein.</span><span class="sxs-lookup"><span data-stu-id="3645e-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="3645e-138">Unterstützen der Konfiguration durch Implementieren eines Eigenschaftenblatts.</span><span class="sxs-lookup"><span data-stu-id="3645e-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="3645e-139">Implementieren Sie ein Status-Objekt, und unterstützen Sie die Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="3645e-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="3645e-140">Handle heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="3645e-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3645e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3645e-141">See also</span></span>



[<span data-ttu-id="3645e-142">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="3645e-142">MAPI Concepts</span></span>](mapi-concepts.md)

