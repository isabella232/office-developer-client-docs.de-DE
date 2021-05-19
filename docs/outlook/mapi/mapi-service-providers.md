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
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409538"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="7fa27-103">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7fa27-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="7fa27-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fa27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fa27-105">Es gibt drei allgemeine Typen von Dienstanbietern:</span><span class="sxs-lookup"><span data-stu-id="7fa27-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="7fa27-106">Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="7fa27-106">Address book providers.</span></span>
    
- <span data-ttu-id="7fa27-107">Nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="7fa27-107">Message store providers.</span></span>
    
- <span data-ttu-id="7fa27-108">Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="7fa27-108">Transport providers.</span></span>
    
<span data-ttu-id="7fa27-109">Adressbuch- und Nachrichtenspeicheranbieter haben viele Ähnlichkeiten.</span><span class="sxs-lookup"><span data-stu-id="7fa27-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="7fa27-110">Sie registrieren einen eindeutigen Bezeichner bei MAPI, den sie zum Erstellen von Eintragsbezeichnern für ihre Objekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="7fa27-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="7fa27-111">Sie stellen eine Hierarchie von Objekten und Eigenschaften zur Verfügung, auf die Clients zugreifen und diese bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="7fa27-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="7fa27-112">Für ihre Containerobjekte unterstützen sie eine Hierarchietabelle und eine Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="7fa27-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="7fa27-113">Sie unterstützen Ereignisbenachrichtigungen für diese Tabellen und optional für einzelne Objekte, damit Clients über Änderungen informiert werden können, die während der Sitzung auftreten.</span><span class="sxs-lookup"><span data-stu-id="7fa27-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="7fa27-114">Wenn Vorgänge länger werden, können sie eine Statusanzeige anzeigen, um den Benutzer über den Status des Vorgangs zu informieren.</span><span class="sxs-lookup"><span data-stu-id="7fa27-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="7fa27-115">Clients können mit Adressbuch- und Nachrichtenspeicheranbietern entweder indirekt über MAPI kommunizieren, indem sie das [IAddrBook verwenden: IMAPIProp](iaddrbookimapiprop.md) und [IMAPISession : IUnknown-Schnittstellen](imapisessioniunknown.md) oder direkt mithilfe einer der Dienstanbieterschnittstellen in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7fa27-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="7fa27-116">**Adressbuchanbieterschnittstellen**</span><span class="sxs-lookup"><span data-stu-id="7fa27-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="7fa27-117">**Schnittstellen des Nachrichtenspeicheranbieters**</span><span class="sxs-lookup"><span data-stu-id="7fa27-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fa27-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7fa27-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="7fa27-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7fa27-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="7fa27-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7fa27-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="7fa27-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7fa27-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="7fa27-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7fa27-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="7fa27-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7fa27-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="7fa27-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7fa27-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="7fa27-125">Transportanbieter unterscheiden sich von Adressbuch- und Nachrichtenspeicheranbietern in der Art und Weise, wie sie mit MAPI und mit Clients kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7fa27-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="7fa27-126">Transportanbieter warten in der Regel darauf, dass MAPI sie zur Information anfordert, anstatt die Kommunikation zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="7fa27-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="7fa27-127">Im Gegensatz zu anderen Anbietern unterstützen Transportanbieter keine Vielzahl von Objekten und Tabellen, auf die häufig von Clients zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7fa27-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="7fa27-128">Sie unterstützen jedoch wie alle Dienstanbieter ein Statusobjekt und veröffentlichen seine Eigenschaften in der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="7fa27-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="7fa27-129">Während Adressbuch- und Nachrichtenspeicheranbieter die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) aufrufen, um eindeutige Bezeichner für die Erstellung ihrer Eintragsbezeichner zu registrieren, rufen Transportanbieter die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) auf, um eindeutige Bezeichner sowie Adresstypen für die Übernahme der Verantwortung für die Zustellung bestimmter Nachrichten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7fa27-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="7fa27-130">Ihr Dienstanbieter sollte über drei Headerdateien verfügen: eine öffentliche Headerdatei und zwei interne Dateien.</span><span class="sxs-lookup"><span data-stu-id="7fa27-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="7fa27-131">Verwenden Sie die öffentliche Headerdatei zur Konfiguration und zum Dokumentieren von Eigenschaften und deren Werten.</span><span class="sxs-lookup"><span data-stu-id="7fa27-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="7fa27-132">Schließen Sie in eine der internen Headerdateien alle erforderlichen öffentlichen #A0 ein. Diese Headerdatei sollte in allen Quelldateien des Dienstanbieters enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="7fa27-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="7fa27-133">Verwenden Sie die andere interne Datei, um Ressourcenbezeichner zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7fa27-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="7fa27-134">Adressbuch-, Nachrichtenspeicher- und Transportanbieter führen die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="7fa27-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="7fa27-135">Gibt eine Einstiegspunktfunktion an.</span><span class="sxs-lookup"><span data-stu-id="7fa27-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="7fa27-136">Liefern Sie einen Anbieter und ein Anmeldeobjekt, um die Anmeldung und Initialisierung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7fa27-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="7fa27-137">Wenn der Anbieter zu einem Nachrichtendienst gehört, müssen Sie eine Einstiegspunktfunktion für den Nachrichtendienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="7fa27-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="7fa27-138">Unterstützen Sie die Konfiguration, indem Sie ein Eigenschaftenblatt implementieren.</span><span class="sxs-lookup"><span data-stu-id="7fa27-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="7fa27-139">Implementieren Sie ein Statusobjekt, und unterstützen Sie die Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="7fa27-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="7fa27-140">Behandeln Des Herunterfahrens.</span><span class="sxs-lookup"><span data-stu-id="7fa27-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fa27-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fa27-141">See also</span></span>



[<span data-ttu-id="7fa27-142">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="7fa27-142">MAPI Concepts</span></span>](mapi-concepts.md)

