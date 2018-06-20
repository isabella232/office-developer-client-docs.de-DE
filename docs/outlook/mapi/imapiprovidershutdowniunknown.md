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
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792327"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="44d28-103">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="44d28-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="44d28-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44d28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44d28-105">Ermöglicht das MAPI-Subsystem, um einen MAPI-Anbieter für das schnelle Herunterfahren von einem MAPI-Client zu informieren, damit der MAPI-Anbieter auf das Herunterfahren reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="44d28-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44d28-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="44d28-106">Header file:</span></span>  <br/> |<span data-ttu-id="44d28-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44d28-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="44d28-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="44d28-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="44d28-109">Provider-Objekte: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)oder [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="44d28-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="44d28-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="44d28-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="44d28-111">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="44d28-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="44d28-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="44d28-112">Called by:</span></span>  <br/> |<span data-ttu-id="44d28-113">MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="44d28-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="44d28-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="44d28-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="44d28-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="44d28-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="44d28-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="44d28-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="44d28-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="44d28-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="44d28-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="44d28-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="44d28-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="44d28-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="44d28-120">Abfragen der MAPI-Anbieter für Schnelles Herunterfahren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="44d28-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="44d28-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="44d28-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="44d28-122">Zeigt den MAPI-Anbieter, dass ein MAPI-Client ausführt, ein Schnelles Herunterfahren, so dass der Anbieter Aktionen, um Datenverlust zu vermeiden nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="44d28-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="44d28-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="44d28-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="44d28-124">Gibt an, an den MAPI-Anbieter, dass der MAPI-Client sofort beendet wird, damit der MAPI-Anbieter ändert sich, um Datenverlust zu vermeiden beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="44d28-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44d28-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44d28-125">Remarks</span></span>

<span data-ttu-id="44d28-126">Schnelles Herunterfahren kann ein MAPI-Client seine in kurzer Zeit zu beenden, hoffentlich geladen, nachdem sich der Client und MAPI-Anbieter haben gespeichert MAPI-Einstellungen und Daten.</span><span class="sxs-lookup"><span data-stu-id="44d28-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="44d28-127">Der MAPI-Client initiiert ein Schnelles Herunterfahren immer und sollte Abfragen des MAPI-Subsystems für Schnelles Herunterfahren Unterstützung von MAPI-Anbieter geladen.</span><span class="sxs-lookup"><span data-stu-id="44d28-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="44d28-128">Ein Administrator kann die Windows-Registrierung können Sie die anbieterunterstützung angeben, die erforderlich sind, um das Schnelles Herunterfahren aller MAPI-Clients zulassen wird auf Benutzerebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44d28-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="44d28-129">Weitere Informationen zu den Einstellungen in der Registrierung finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="44d28-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="44d28-130">Für schnelle Herunterfahren ohne Datenverlust erfolgreich ausgeführt wurde, sollte MAPI-Anbieter jedoch die **IMAPIProviderShutdown** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="44d28-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="44d28-131">Ein MAPI-Anbieter, der schnelle Herunterfahren von Clients unterstützen muss, sollte zu MAPI-Subsystems in der **IMAPIProviderShutdown::QueryFastShutdown** -Methode S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="44d28-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="44d28-132">Wenn MAPI-Subsystems anschließend die Methoden **IMAPIProviderShutdown::NotifyProcessShutdown** und **IMAPIProviderShutdown::DoFastShutdown** aufruft, dauert der MAPI-Anbieter erforderliche Aktionen für das MAPI-Einstellungen und Daten zu speichern und Vorbereiten der Client beenden.</span><span class="sxs-lookup"><span data-stu-id="44d28-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="44d28-133">MAPI-Anbieter, die keine schnelle Herunterfahren von Clients unterstützen müssen sollten weiterhin die **IMAPIProviderShutdown** -Schnittstelle implementieren, und haben die **IMAPIProviderShutdown::QueryFastShutdown** -Methode MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="44d28-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="44d28-134">Für Outlook als MAPI-Client bewirkt, dass dieser Outlook warten, dass alle externen Verweise freigegeben werden muss, bevor sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="44d28-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="44d28-135">Je nach Windows-Registrierung des Benutzers verhindert Einstellung für das schnelle Herunterfahren nicht implementieren der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt ein schnelle Herunterfahren von Clients.</span><span class="sxs-lookup"><span data-stu-id="44d28-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="44d28-136">Weitere Informationen über den Prozess der Schnelles Herunterfahren finden Sie unter [Übersicht über die schnelle Herunterfahren](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="44d28-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="44d28-137">Informationen dazu, wie Sie das schnelle Herunterfahren erfolgreich durchzuführen finden Sie unter [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="44d28-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44d28-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44d28-138">See also</span></span>



[<span data-ttu-id="44d28-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="44d28-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="44d28-140">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="44d28-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

