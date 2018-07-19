---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792087"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="91774-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91774-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="91774-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91774-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91774-105">Ermöglicht einen MAPI-Client, um das schnelle Herunterfahren des Clientprozesses auszuführen.</span><span class="sxs-lookup"><span data-stu-id="91774-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91774-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="91774-106">Header file:</span></span>  <br/> |<span data-ttu-id="91774-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91774-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="91774-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="91774-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="91774-109">[IMAPISession](imapisessioniunknown.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="91774-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="91774-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="91774-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="91774-111">MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="91774-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="91774-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="91774-112">Called by:</span></span>  <br/> |<span data-ttu-id="91774-113">MAPI-client</span><span class="sxs-lookup"><span data-stu-id="91774-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="91774-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="91774-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="91774-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="91774-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="91774-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="91774-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="91774-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="91774-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="91774-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="91774-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="91774-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="91774-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="91774-120">Abfragen des MAPI-Subsystems für Schnelles Herunterfahren unterstützt, die von geladenen MAPI-Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="91774-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="91774-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="91774-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="91774-122">Gibt an, fahren Sie der Zweck der MAPI-Client, fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="91774-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="91774-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="91774-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="91774-124">Gibt an, dass der MAPI-Client der Client sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="91774-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91774-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91774-125">Remarks</span></span>

<span data-ttu-id="91774-126">Schnelles Herunterfahren dient, dass ein MAPI-Client und alle geladenen MAPI-Anbieter mit dem der MAPI-Client eine aktive MAPI-Sitzung MAPI-Einstellungen und Daten gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="91774-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="91774-127">Auf diese Weise können den MAPI-Client, trennen alle externen Verweise und zu beenden, ohne Datenverlust verursacht.</span><span class="sxs-lookup"><span data-stu-id="91774-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="91774-128">Ein MAPI-Client, der muss Schnelles Herunterfahren ausführen, muss die **IMAPIClientShutdown** -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="91774-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="91774-129">Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, durch die QueryInterface-Methode für jedes Objekt [IMAPISession](imapisessioniunknown.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="91774-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="91774-130">Ein MAPI-Client wird stets ein Schnelles Herunterfahren durch Aufrufen der Methode **IMAPIClientShutdown::QueryFastShutdown** initiiert.</span><span class="sxs-lookup"><span data-stu-id="91774-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="91774-131">MAPI-Subsystems reagiert auf die MAPI-Client-Abfrage, indem Sie überprüfen, ob die geladene MAPI-Anbieter Schnelles Herunterfahren des Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="91774-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="91774-132">Der Administrator kann Einstellungen der Windows-Registrierung verwenden, um die Ebene der anbieterunterstützung zu ermitteln, die für MAPI-Clients zu Schnelles Herunterfahren fortsetzen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="91774-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="91774-133">Weitere Informationen finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="91774-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="91774-134">Um Schnelles Herunterfahren fortzusetzen, ruft der Client die **IMAPIClientShutdown::NotifyProcessShutdown** -Methode, um die Absicht Herunterfahren des MAPI-Subsystems anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="91774-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="91774-135">Der Client ruft dann die **IMAPIClientShutdown::DoFastShutdown** -Methode, um darauf hinzuweisen, dass der Clientprozess sofort beendet wird.</span><span class="sxs-lookup"><span data-stu-id="91774-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="91774-136">Weitere Informationen zu Schnelles Herunterfahren finden Sie unter [Übersicht über die schnelle Herunterfahren](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="91774-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="91774-137">Informationen über das Schnelles Herunterfahren erfolgreich ausführen finden Sie unter [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="91774-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="91774-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91774-138">See also</span></span>



[<span data-ttu-id="91774-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="91774-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="91774-140">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="91774-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

