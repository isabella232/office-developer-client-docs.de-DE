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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350876"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="6906d-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6906d-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="6906d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6906d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6906d-105">Ermöglicht einem MAPI-Client das schnelle Herunterfahren des Clientprozesses.</span><span class="sxs-lookup"><span data-stu-id="6906d-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6906d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6906d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6906d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6906d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6906d-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="6906d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6906d-109">[IMAPISession](imapisessioniunknown.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="6906d-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="6906d-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6906d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6906d-111">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="6906d-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="6906d-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6906d-112">Called by:</span></span>  <br/> |<span data-ttu-id="6906d-113">MAPI-Client</span><span class="sxs-lookup"><span data-stu-id="6906d-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="6906d-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6906d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6906d-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="6906d-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="6906d-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="6906d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6906d-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="6906d-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6906d-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6906d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6906d-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="6906d-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="6906d-120">Fragt das MAPI-Subsystem zur Unterstützung des schnellen Herunterfahrens ab, das von geladenen MAPI-Anbietern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6906d-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="6906d-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="6906d-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="6906d-122">Gibt an, dass der MAPI-Client mit dem Herunterfahren fortfahren soll.</span><span class="sxs-lookup"><span data-stu-id="6906d-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="6906d-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="6906d-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="6906d-124">Gibt an, dass der MAPI-Client sofort den Clientprozess beenden soll.</span><span class="sxs-lookup"><span data-stu-id="6906d-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6906d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6906d-125">Remarks</span></span>

<span data-ttu-id="6906d-126">Der Zweck des schnellen Herunterfahrens besteht darin, einem MAPI-Client und einem beliebigen geladenen MAPI-Anbieter, mit dem der MAPI-Client über eine aktive MAPI-Sitzung verfügt, die MAPI-Einstellungen und-Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6906d-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="6906d-127">Dadurch kann der MAPI-Client alle externen Verweise trennen und beenden, ohne Datenverluste zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="6906d-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="6906d-128">Ein MAPI-Client, der Schnelles Herunterfahren durchführen muss, muss die **IMAPIClientShutdown** -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="6906d-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="6906d-129">Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, indem er die IUnknown:: QueryInterface-Methode für ein beliebiges [IMAPISession](imapisessioniunknown.md) -Objekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="6906d-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="6906d-130">Ein MAPI-Client initiiert immer ein schnelles Herunterfahren durch Aufrufen der **IMAPIClientShutdown:: QueryFastShutdown** -Methode.</span><span class="sxs-lookup"><span data-stu-id="6906d-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="6906d-131">Das MAPI-Subsystem antwortet auf die Abfrage des MAPI-Clients, indem überprüft wird, ob geladene MAPI-Anbieter das schnelle Herunterfahren des Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6906d-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="6906d-132">Der Administrator kann mithilfe der Windows-Registrierungseinstellungen die Ebene der Anbieterunterstützung ermitteln, die für MAPI-Clients erforderlich ist, um das schnelle Herunterfahren zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6906d-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="6906d-133">Weitere Informationen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="6906d-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="6906d-134">Um mit dem schnellen Herunterfahren fortzufahren, ruft der Client die **IMAPIClientShutdown:: NotifyProcessShutdown** -Methode auf, um dem MAPI-Subsystem anzuzeigen, dass das Herunterfahren beabsichtigt ist.</span><span class="sxs-lookup"><span data-stu-id="6906d-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="6906d-135">Der Client ruft dann die **IMAPIClientShutdown::D ofastshutdown** -Methode auf, um anzugeben, dass der Clientprozess sofort beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6906d-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="6906d-136">Weitere Informationen zum schnellen Herunterfahren finden Sie unter [Übersicht über Schnelles Herunterfahren](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6906d-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="6906d-137">Informationen dazu, wie Sie das schnelle Herunterfahren erfolgreich durchführen können, finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="6906d-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6906d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6906d-138">See also</span></span>



[<span data-ttu-id="6906d-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6906d-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="6906d-140">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="6906d-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

