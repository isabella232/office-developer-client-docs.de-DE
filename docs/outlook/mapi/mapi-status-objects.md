---
title: MAPI-Status Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406745"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="6102e-103">MAPI-Status Objekte</span><span class="sxs-lookup"><span data-stu-id="6102e-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="6102e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6102e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6102e-105">Status Objekte melden Informationen zu MAPI-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6102e-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="6102e-106">Beispielsweise ein Dienstanbieter, der MAPI-Übermittlungsprozess oder das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="6102e-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="6102e-107">Es gibt ein Status-Objekt, das Informationen zu jedem einzelnen Dienstanbieter im aktuellen Profil bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6102e-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="6102e-108">MAPI ist für die Implementierung von Statusobjekten für das Subsystem, den MAPI-Sende-und Empfangsprozess und das Adressbuch verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="6102e-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="6102e-109">Das Subsystem Status-Objekt liefert globale Informationen.</span><span class="sxs-lookup"><span data-stu-id="6102e-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="6102e-110">Das Status-Objekt für das integrierte Adressbuch liefert den Status aller Adressbuchanbieter, die derzeit in Betrieb sind.</span><span class="sxs-lookup"><span data-stu-id="6102e-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="6102e-111">Jedes Status-Objekt ist in der Statustabelle enthalten, eine von MAPI verwaltete Tabelle, die Clients alle Statusinformationen für die Sitzung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6102e-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="6102e-112">Weitere Informationen finden Sie unter [Status Tabellen](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6102e-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="6102e-113">Clients können über die Tabelle oder, bei einem Dienstanbieter, über das Anmeldeobjekt auf ein bestimmtes Statusobjekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6102e-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="6102e-114">Um beispielsweise auf das Statusobjekt eines Adressbuch Anbieters zuzugreifen, kann ein Client **IABLogon:: OpenStatusEntry**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6102e-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="6102e-115">Weitere Informationen finden Sie unter [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="6102e-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="6102e-116">Clients können Status-Objekte für folgende Zwecke verwenden:</span><span class="sxs-lookup"><span data-stu-id="6102e-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="6102e-117">Erfahren Sie mehr über den Status einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6102e-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="6102e-118">Überwachen eines Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="6102e-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="6102e-119">Steuern der Nachrichtenübertragung.</span><span class="sxs-lookup"><span data-stu-id="6102e-119">Control message transmission.</span></span>
    
- <span data-ttu-id="6102e-120">Anzeigen oder Ändern der Konfiguration und des Status einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="6102e-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="6102e-121">Jedes Status-Objekt implementiert die **IMAPIStatus** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6102e-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="6102e-122">Weitere Informationen finden Sie unter [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6102e-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="6102e-123">Allerdings unterstützt nicht jedes Status-Objekt vollständig jede **IMAPIStatus** -Methode.</span><span class="sxs-lookup"><span data-stu-id="6102e-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="6102e-124">Da es in den von einem Status-Objekt unterstützten Methoden Variationen gibt, müssen sich die Clients über ein bestimmtes Statusobjekt informieren, bevor es verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6102e-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="6102e-125">Status Objekte sind erforderlich, um Informationen zu Ihren Features in den folgenden drei Eigenschaften zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="6102e-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="6102e-126">**PR_RESOURCE_METHODS** ([Pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6102e-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="6102e-127">**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6102e-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="6102e-128">**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6102e-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="6102e-129">Weitere Informationen zum Implementieren eines Status-Objekts finden Sie unter [Status Object Implementation](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="6102e-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="6102e-130">Weitere Informationen zur Verwendung eines Status-Objekts finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6102e-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

