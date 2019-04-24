---
title: Informationen über die Replikations-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329519"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="eff55-103">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="eff55-103">About the Replication API</span></span>

  
  
<span data-ttu-id="eff55-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eff55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eff55-105">Die Replikations-API bietet die Funktionalität für einen MAPI-Nachrichtenspeicher Anbieter zum Synchronisieren von Microsoft Outlook 2013-oder Microsoft Outlook 2010-Elementen zwischen einem Server und einem privaten PST-basierten lokalen Speicher, der für diesen Anbieter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eff55-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eff55-106">Ein MAPI-Nachrichtenspeicher Anbieter muss die Replikations-API gemäß den Anweisungen in [über den Replikationsstatus Computer](about-the-replication-state-machine.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="eff55-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="eff55-107">Der Anbieter muss die API nur in einem persönlichen Informationsspeicher verwenden, der für sich selbst erstellt wurde, und nicht in persönlichen speichern, die für andere Anbieter erstellt wurden, da persönliche Speicher, die für andere Anbieter erstellt wurden, möglicherweise bereits eigene Replikationsmechanismen mit dem jeweiligen Server eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="eff55-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="eff55-108">Beispielsweise pflegt eine Offlineordnerdatei (Ost) eine eigene Replikationsbeziehung mit einem Microsoft Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="eff55-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="eff55-109">Um die Replikations-API verwenden zu können, muss ein MAPI-Nachrichtenspeicher Anbieter zunächst einen PST-basierten lokalen Speicher öffnen und einbinden, indem er **[NSTServiceEntry](nstserviceentry.md)** aufruft.</span><span class="sxs-lookup"><span data-stu-id="eff55-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="eff55-110">Der Anbieter kann dann die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="eff55-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="eff55-111">**IPSTX** wird durch Abfragen in [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)und **IOSTX** von **[IPSTX::](ipstx-getsyncobject.md)** getsyncobject bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eff55-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="eff55-112">Die IOSTX-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eff55-112">The IOSTX Interface</span></span>

<span data-ttu-id="eff55-113">Die **IOSTX** -Schnittstelle ist die primäre Schnittstelle, die die Synchronisierung in der Replikations-API ausführt.</span><span class="sxs-lookup"><span data-stu-id="eff55-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="eff55-114">**IOSTX** verschiebt den lokalen Speicher über eine Reihe von Zuständen, ruft Informationen in jedem Status zu Änderungen im lokalen Speicher ab und informiert den lokalen Speicher über Änderungen auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="eff55-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="eff55-115">Die Replikations-API gibt außerdem viele Datenstrukturen an, die die Synchronisierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eff55-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="eff55-116">Ein Speicheranbieter als Client für diese API verwendet die Replikations-API zum Umschließen des lokalen Speichers und zum Durchlaufen dieser Zustände, wodurch Änderungen im lokalen Speicher (beispielsweise Änderungen an der Ordnerhierarchie oder das Hinzufügen neuer Elemente) zum Server und zum Abrufen von Informationen zu Änderungen auf dem Server und zur bereitstellungdieser Informationen für die **IOSTX** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eff55-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="eff55-117">Die **IOSTX** -Schnittstelle übernimmt die von Microsoft Exchange Server bereitgestellte inkrementelle Änderungs Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="eff55-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="eff55-118">Weitere Informationen zu ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="eff55-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="eff55-119">Über **IOSTX**verwendet der Client ICS zum Überwachen und Synchronisieren von inkrementellen Änderungen an der Hierarchie oder den Inhalten in einem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="eff55-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="eff55-120">Die IPSTX-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eff55-120">The IPSTX Interface</span></span>

 <span data-ttu-id="eff55-121">**IPSTX** und fünf weitere \* \* IPSTX *n* \* \*-Schnittstellen, die von **IPSTX** erben, bieten Hilfsfunktionen, die beim Durchführen der Replikation über die **IOSTX** -Schnittstelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="eff55-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="eff55-122">Beispielsweise ermöglicht **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** , dass der lokale Speicher den Outlook-Protokoll-Manager emuliert, um ausgehende Nachrichten an einen Server zu spoolen.</span><span class="sxs-lookup"><span data-stu-id="eff55-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="eff55-123">Weitere Informationen über Statusübergänge während der Replikation finden Sie unter Informationen zum [Replikationsstatus Computer](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="eff55-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="eff55-124">Die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="eff55-124">The Replication API</span></span>

<span data-ttu-id="eff55-125">Die Replikations-API bietet die folgenden Definitionen, Datentypen und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="eff55-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="eff55-126">Eine Beispielimplementierung eines Speicheranbieters für eingebundene persönliche Ordner-Dateien (PST) finden Sie unter Informationen zum einGebundenen [PST-Speicheranbieter](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="eff55-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="eff55-127">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="eff55-127">Definitions:</span></span>
  
- [<span data-ttu-id="eff55-128">Konstanten für die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="eff55-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="eff55-129">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="eff55-129">Functions:</span></span>
  
- <span data-ttu-id="eff55-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="eff55-131">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="eff55-131">Data types:</span></span>
  
- <span data-ttu-id="eff55-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="eff55-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="eff55-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="eff55-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="eff55-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="eff55-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="eff55-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="eff55-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="eff55-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="eff55-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="eff55-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="eff55-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="eff55-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="eff55-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="eff55-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="eff55-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="eff55-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="eff55-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="eff55-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="eff55-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="eff55-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="eff55-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="eff55-154">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="eff55-154">Interfaces:</span></span>
  
- <span data-ttu-id="eff55-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="eff55-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="eff55-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="eff55-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="eff55-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="eff55-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="eff55-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="eff55-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

