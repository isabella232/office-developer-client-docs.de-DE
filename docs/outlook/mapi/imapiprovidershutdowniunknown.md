---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322406"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="4538f-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4538f-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="4538f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4538f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4538f-105">Ermöglicht dem MAPI-Subsystem, einen MAPI-Anbieter über das schnelle Herunterfahren eines MAPI-Clients zu informieren, damit der MAPI-Anbieter auf das Herunterfahren reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="4538f-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4538f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4538f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4538f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4538f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4538f-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="4538f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4538f-109">Anbieterobjekte: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)oder [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="4538f-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="4538f-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4538f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4538f-111">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="4538f-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="4538f-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4538f-112">Called by:</span></span>  <br/> |<span data-ttu-id="4538f-113">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="4538f-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="4538f-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="4538f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4538f-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="4538f-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="4538f-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="4538f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4538f-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="4538f-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4538f-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="4538f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4538f-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="4538f-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="4538f-120">Fragt den MAPI-Anbieter ab, um das schnelle Herunterfahren zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4538f-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="4538f-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="4538f-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="4538f-122">Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen soll, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4538f-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="4538f-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="4538f-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="4538f-124">Gibt dem MAPI-Anbieter an, dass der MAPI-Client sofort beendet wird, sodass der MAPI-Anbieter Änderungen anhält, um Datenverluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4538f-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4538f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4538f-125">Remarks</span></span>

<span data-ttu-id="4538f-126">Das schnelle Herunterfahren ermöglicht es einem MAPI-Client, seinen Prozess innerhalb kurzer Zeit zu beenden, hoffentlich nachdem der Client und die geladenen MAPI-Anbieter MAPI-Einstellungen und-Daten gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="4538f-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="4538f-127">Der MAPI-Client initiiert immer ein schnelles Herunterfahren und sollte das MAPI-Subsystem Abfragen, um die Unterstützung für das schnelle Herunterfahren von den geladenen MAPI-Anbietern zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4538f-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="4538f-128">Ein Administrator kann die Windows-Registrierung auf Benutzerebene festlegen, um die Ebene der Anbieterunterstützung anzugeben, die erforderlich ist, um das schnelle Herunterfahren aller MAPI-Clients zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4538f-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="4538f-129">Weitere Informationen zu den Registrierungseinstellungen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="4538f-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="4538f-130">Damit jedoch das schnelle Herunterfahren ohne Datenverlust erfolgreich ausgeführt werden kann, sollten MAPI-Anbieter die **IMAPIProviderShutdown** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="4538f-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="4538f-131">Ein MAPI-Anbieter, der das schnelle Herunterfahren des Clients unterstützen muss, sollte S_OK in der **IMAPIProviderShutdown:: QueryFastShutdown** -Methode an das MAPI-Subsystem zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4538f-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="4538f-132">Wenn das MAPI-Subsystem anschließend die Methoden **IMAPIProviderShutdown:: NotifyProcessShutdown** und **IMAPIProviderShutdown::D ofastshutdown** aufruft, sollte der MAPI-Anbieter die erforderlichen Aktionen zum Speichern von MAPI-Einstellungen und-Daten ergreifen und bereiten Sie den Exit des Clients vor.</span><span class="sxs-lookup"><span data-stu-id="4538f-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="4538f-133">MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die **IMAPIProviderShutdown** -Schnittstelle implementieren und die **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** -Methode MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4538f-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="4538f-134">Für Outlook als MAPI-Client bewirkt dies, dass Outlook auf alle externen Verweise wartet, bevor es beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4538f-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="4538f-135">Abhängig von der Windows-Registrierungseinstellung des Benutzers für das schnelle Herunterfahren verhindert die Implementierung der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt, dass ein Client schnell heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="4538f-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="4538f-136">Weitere Informationen zum Prozess des schnellen Herunterfahrens finden Sie unter [Übersicht über Schnelles Herunterfahren](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4538f-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="4538f-137">Weitere Informationen dazu, wie Sie das schnelle Herunterfahren erfolgreich ausführen können, finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="4538f-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4538f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4538f-138">See also</span></span>



[<span data-ttu-id="4538f-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4538f-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="4538f-140">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="4538f-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

