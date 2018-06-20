---
title: Über die API-Replikation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 50b36ee60d00e06a1f5baa8726b5f27c4a3e6ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791220"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="4da09-103">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="4da09-103">About the Replication API</span></span>

  
  
<span data-ttu-id="4da09-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4da09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4da09-105">Die Replikation-API bietet die Funktionalität für einen Anbieter für MAPI-Nachricht anmelden zum Synchronisieren von Microsoft Outlook 2013 oder Microsoft Outlook 2010 Elemente zwischen einem Server und einem privaten PST-basierten lokalen Speicher, der für diesen Anbieter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4da09-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4da09-106">Nachricht ein MAPI-Anbieter muss die Replikation API gemäß den Anweisungen in [Über die Replikation Zustandsautomat](about-the-replication-state-machine.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="4da09-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="4da09-107">Der Anbieter mithilfe der API nur in einem persönlichen Speicher für sich selbst erstellt haben, und nicht auf persönliche Speicher für andere Anbieter erstellt haben, da persönliche Informationsspeicher für erstellt andere Anbieter möglicherweise bereits eingerichtet haben eigene Replikationsmechanismen mit dem jeweiligen Server.</span><span class="sxs-lookup"><span data-stu-id="4da09-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="4da09-108">Beispielsweise verwaltet Offlineordnerdatei (OST) eine eigene Replikations-Beziehung mit einem Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4da09-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="4da09-109">Um die Replikation-API verwenden, muss ein Anbieter für MAPI-Nachricht Anmelden zuerst öffnen und Text fließt um eine PST-basierten lokalen Speicher durch Aufrufen von **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="4da09-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="4da09-110">Der Anbieter können Sie die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)**, um die Replikation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4da09-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="4da09-111">**IPSTX** erfolgt durch Abfragen auf [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), und **IOSTX** durch **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4da09-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="4da09-112">Die IOSTX-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4da09-112">The IOSTX Interface</span></span>

<span data-ttu-id="4da09-113">Die **IOSTX** -Schnittstelle ist die primäre Schnittstelle, die in der Replikation API Synchronisierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4da09-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="4da09-114">**IOSTX** verschiebt den lokalen Speicher durch eine Reihe von Staaten, Abrufen von Informationen zum Änderungen im lokalen Speicher in jedem Status als auch darüber informiert den lokalen Speicher von Änderungen auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="4da09-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="4da09-115">Die Replikation-API gibt auch viele Datenstrukturen, die die Synchronisierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4da09-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="4da09-116">Ein Anbieter verwendet als Client für diese API die Replikation-API zur Text fließt um die lokalen Speicher und die Zustände, Navigation, pushen von Änderungen an den Server auf dem lokalen Speicher (beispielsweise Änderungen an der Ordnerhierarchie oder das Hinzufügen neuer Elemente), und das auch abrufen Informationen zu Änderungen auf dem Server und diese Informationen an die **IOSTX** -Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4da09-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="4da09-117">Die Schnittstelle **IOSTX** nimmt inkrementelle Änderung Synchronisierung (ICS) von Microsoft Exchange Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4da09-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="4da09-118">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4da09-118">For more information about ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="4da09-119">Über **IOSTX**verwendet der Client ICS überwachen und synchronisieren inkrementelle Änderungen an der Hierarchie oder Inhalt in einem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="4da09-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="4da09-120">Die IPSTX-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4da09-120">The IPSTX Interface</span></span>

 <span data-ttu-id="4da09-121">**IPSTX** und fünf andere ** IPSTX *n* ** Schnittstellen, die von **IPSTX** erben bieten Hilfsfunktionen, die beim Ausführen einer Replikation über die Schnittstelle **IOSTX** verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4da09-121">**IPSTX** and five other **IPSTX *n* ** interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="4da09-122">Beispielsweise können **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** Sie mit den lokalen Speicher emulieren von Outlook-Protokoll-Manager, um ausgehende Nachrichten an einen Server Spoolen tätigen.</span><span class="sxs-lookup"><span data-stu-id="4da09-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="4da09-123">Weitere Informationen zu Statusübergänge während der Replikation finden Sie unter [Informationen zu der Replikation Zustandsautomat](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="4da09-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="4da09-124">Die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="4da09-124">The Replication API</span></span>

<span data-ttu-id="4da09-125">Die Replikation-API bietet die folgenden Definitionen sowie die Datentypen und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4da09-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="4da09-126">Eine beispielimplementierung von einem Anbieter für umbrochenen Persönliche Ordner-Dateien (PST) finden Sie unter [Über die umbrochen PST -Datei speichern Beispielanbieter](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4da09-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="4da09-127">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="4da09-127">Definitions:</span></span>
  
- [<span data-ttu-id="4da09-128">Konstanten für die Replikation API</span><span class="sxs-lookup"><span data-stu-id="4da09-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="4da09-129">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="4da09-129">Functions:</span></span>
  
- <span data-ttu-id="4da09-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="4da09-131">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="4da09-131">Data types:</span></span>
  
- <span data-ttu-id="4da09-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="4da09-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="4da09-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="4da09-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="4da09-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="4da09-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="4da09-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="4da09-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="4da09-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="4da09-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="4da09-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="4da09-143">**[SYNCHRONISIERUNGSSTATUS](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="4da09-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="4da09-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="4da09-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="4da09-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="4da09-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="4da09-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="4da09-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="4da09-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="4da09-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="4da09-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="4da09-154">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="4da09-154">Interfaces:</span></span>
  
- <span data-ttu-id="4da09-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="4da09-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="4da09-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="4da09-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="4da09-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="4da09-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="4da09-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="4da09-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

