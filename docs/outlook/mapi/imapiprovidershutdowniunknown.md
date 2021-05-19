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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409657"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="48bde-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48bde-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="48bde-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48bde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48bde-105">Ermöglicht dem MAPI-Subsystem, einen MAPI-Anbieter über das schnelle Herunterfahren eines MAPI-Clients zu informieren, damit der MAPI-Anbieter auf das Herunterfahren reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="48bde-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48bde-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="48bde-106">Header file:</span></span>  <br/> |<span data-ttu-id="48bde-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48bde-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="48bde-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="48bde-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="48bde-109">Anbieterobjekte: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)oder [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="48bde-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="48bde-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="48bde-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="48bde-111">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="48bde-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="48bde-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="48bde-112">Called by:</span></span>  <br/> |<span data-ttu-id="48bde-113">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="48bde-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="48bde-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="48bde-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="48bde-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="48bde-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="48bde-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="48bde-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="48bde-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="48bde-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="48bde-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="48bde-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="48bde-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="48bde-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="48bde-120">Fragt den MAPI-Anbieter nach Unterstützung für schnelles Herunterfahren ab.</span><span class="sxs-lookup"><span data-stu-id="48bde-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="48bde-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="48bde-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="48bde-122">Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen wird, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="48bde-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="48bde-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="48bde-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="48bde-124">Gibt dem MAPI-Anbieter an, dass der MAPI-Client sofort beendet wird, sodass der MAPI-Anbieter Änderungen beibehalten wird, um Datenverluste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="48bde-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48bde-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48bde-125">Remarks</span></span>

<span data-ttu-id="48bde-126">Schnelles Herunterfahren ermöglicht es einem MAPI-Client, seinen Prozess innerhalb kurzer Zeit zu beenden, hoffentlich, nachdem der Client und die geladenen MAPI-Anbieter MAPI-Einstellungen und -Daten gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="48bde-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="48bde-127">Der MAPI-Client initiiert immer ein schnelles Herunterfahren und sollte das MAPI-Subsystem auf Unterstützung für schnelles Herunterfahren von den geladenen MAPI-Anbietern abfragen.</span><span class="sxs-lookup"><span data-stu-id="48bde-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="48bde-128">Ein Administrator kann die Windows auf Benutzerebene festlegen, um die Ebene der Anbieterunterstützung anzugeben, die erforderlich ist, um das schnelle Herunterfahren aller MAPI-Clients zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="48bde-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="48bde-129">Weitere Informationen zu den Registrierungseinstellungen finden Sie unter [Fast Shutdown User Options](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="48bde-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="48bde-130">Damit das schnelle Herunterfahren jedoch erfolgreich ohne Datenverlust erfolgt, sollten MAPI-Anbieter die **IMAPIProviderShutdown-Schnittstelle** implementieren.</span><span class="sxs-lookup"><span data-stu-id="48bde-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="48bde-131">Ein MAPI-Anbieter, der das schnelle Herunterfahren des Clients unterstützen muss, sollte S_OK an das MAPI-Subsystem in der **IMAPIProviderShutdown::QueryFastShutdown-Methode** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="48bde-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="48bde-132">Wenn das MAPI-Subsystem anschließend die **Methoden IMAPIProviderShutdown::NotifyProcessShutdown** und **IMAPIProviderShutdown::D oFastShutdown** aufruft, sollte der MAPI-Anbieter die erforderlichen Aktionen ergreifen, um MAPI-Einstellungen und -Daten zu speichern und den Clientabgang vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="48bde-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="48bde-133">MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die **IMAPIProviderShutdown-Schnittstelle** implementieren und die **IMAPIProviderShutdown::QueryFastShutdown-Methode** MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="48bde-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="48bde-134">Für Outlook als MAPI-Client führt dies dazu, dass Outlook warten, bis alle externen Verweise freigegeben werden, bevor sie beendet werden.</span><span class="sxs-lookup"><span data-stu-id="48bde-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="48bde-135">Abhängig von der Registrierungseinstellung Windows Benutzer für schnelles Herunterfahren verhindert das Nicht implementieren der **IMAPIProviderShutdown-Schnittstelle** nicht unbedingt das schnelle Herunterfahren eines Clients.</span><span class="sxs-lookup"><span data-stu-id="48bde-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="48bde-136">Weitere Informationen zum Prozess des schnellen Herunterfahrens finden Sie unter [Fast Shutdown Overview](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="48bde-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="48bde-137">Informationen zum erfolgreichen Schnellen Herunterfahren finden Sie unter [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="48bde-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48bde-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48bde-138">See also</span></span>



[<span data-ttu-id="48bde-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="48bde-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="48bde-140">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="48bde-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

