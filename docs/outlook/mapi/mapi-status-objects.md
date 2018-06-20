---
title: MAPI-Status-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793094"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="8f86e-103">MAPI-Status-Objekte</span><span class="sxs-lookup"><span data-stu-id="8f86e-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="8f86e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f86e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f86e-105">Status-Objekten ein Bericht mit Informationen zu MAPI-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8f86e-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="8f86e-106">Beispielsweise einem Dienstanbieter, die MAPI-senden-empfangen-Prozess oder im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="8f86e-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="8f86e-107">Es ist ein Statusobjekt, das Informationen zu jeder einzelnen Dienstanbieter im aktuellen Profil angeben.</span><span class="sxs-lookup"><span data-stu-id="8f86e-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="8f86e-108">MAPI ist verantwortlich für die Implementierung der Status-Objekte für das Subsystem, der MAPI-Prozess senden/empfangen und im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="8f86e-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="8f86e-109">Das Subsystem Status-Objekt stellt globalen Informationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8f86e-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="8f86e-110">Das Statusobjekt für das integrierte-Adressbuch liefert den Status aller Address Book Anbieter aktuell ausgeführten.</span><span class="sxs-lookup"><span data-stu-id="8f86e-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="8f86e-111">Jedes Statusobjekt ist in der Statustabelle, einer Tabelle, MAPI, das mit allen die Statusinformationen für die Sitzung Clients bietet verwaltet enthalten.</span><span class="sxs-lookup"><span data-stu-id="8f86e-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="8f86e-112">Weitere Informationen finden Sie unter [Statustabellen](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8f86e-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="8f86e-113">Clients können einen bestimmten Status-Objekt entweder durch die Tabelle oder bei einem Dienstanbieter, über die Anmeldung-Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8f86e-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="8f86e-114">Um eine Adressbuchanbieter Statusobjekt zuzugreifen, kann ein Client beispielsweise **IABLogon::OpenStatusEntry**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8f86e-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="8f86e-115">Weitere Informationen finden Sie unter [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="8f86e-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="8f86e-116">Clients können Status-Objekte zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="8f86e-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="8f86e-117">Informationen Sie zu den Status einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8f86e-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="8f86e-118">Überwachen von einem Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8f86e-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="8f86e-119">Steuern Sie Nachrichtenübermittlung.</span><span class="sxs-lookup"><span data-stu-id="8f86e-119">Control message transmission.</span></span>
    
- <span data-ttu-id="8f86e-120">Zeigen Sie an oder ändern Sie einer Ressource Konfigurations- und Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="8f86e-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="8f86e-121">Jedes Statusobjekt implementiert die **IMAPIStatus** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8f86e-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="8f86e-122">Weitere Informationen finden Sie unter [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="8f86e-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="8f86e-123">Allerdings werden nicht jedes Statusobjekt jede Methode **IMAPIStatus** vollständig unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8f86e-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="8f86e-124">Da es Variation in den Methoden, die durch ein Statusobjekt unterstützt werden ist, müssen Clients über einen bestimmten Status-Objekt zu informieren, bevor es verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f86e-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="8f86e-125">Status-Objekte sind zum Veröffentlichen von Informationen über ihre Features in den folgenden drei Eigenschaften erforderlich:</span><span class="sxs-lookup"><span data-stu-id="8f86e-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="8f86e-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f86e-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="8f86e-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f86e-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="8f86e-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f86e-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="8f86e-129">Weitere Informationen zum Implementieren eines Objekts Status finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="8f86e-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="8f86e-130">Weitere Informationen zum Verwenden einer Status-Objekts finden Sie unter [Statustabelle und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8f86e-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
