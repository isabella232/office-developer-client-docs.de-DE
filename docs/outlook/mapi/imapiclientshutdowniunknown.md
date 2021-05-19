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
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435334"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="23651-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23651-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="23651-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23651-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23651-105">Ermöglicht einem MAPI-Client das schnelle Herunterfahren des Clientprozesses.</span><span class="sxs-lookup"><span data-stu-id="23651-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23651-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="23651-106">Header file:</span></span>  <br/> |<span data-ttu-id="23651-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23651-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="23651-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="23651-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="23651-109">[IMAPISession-Objekt](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="23651-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="23651-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="23651-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="23651-111">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="23651-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="23651-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="23651-112">Called by:</span></span>  <br/> |<span data-ttu-id="23651-113">MAPI-Client</span><span class="sxs-lookup"><span data-stu-id="23651-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="23651-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="23651-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="23651-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="23651-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="23651-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="23651-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="23651-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="23651-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="23651-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="23651-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="23651-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="23651-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="23651-120">Fragt das MAPI-Subsystem nach Unterstützung für schnelles Herunterfahren ab, die von geladenen MAPI-Anbietern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="23651-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="23651-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="23651-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="23651-122">Gibt die Absicht des MAPI-Clients an, mit dem Herunterfahren fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="23651-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="23651-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="23651-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="23651-124">Gibt die Absicht des MAPI-Clients an, den Clientprozess sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="23651-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23651-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23651-125">Remarks</span></span>

<span data-ttu-id="23651-126">Der Zweck des schnellen Herunterfahrens besteht im Zulassen eines MAPI-Clients und eines beliebigen geladenen MAPI-Anbieters, mit dem der MAPI-Client über eine aktive MAPI-Sitzung zum Speichern von MAPI-Einstellungen und -Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="23651-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="23651-127">Dadurch kann der MAPI-Client alle externen Verweise trennen und beenden, ohne Datenverlust zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="23651-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="23651-128">Ein MAPI-Client, der schnelles Herunterfahren ausführen muss, muss die **IMAPIClientShutdown-Schnittstelle** verwenden.</span><span class="sxs-lookup"><span data-stu-id="23651-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="23651-129">Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, indem er die IUnknown::QueryInterface-Methode für jedes [IMAPISession-Objekt](imapisessioniunknown.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="23651-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="23651-130">Ein MAPI-Client initiiert immer ein schnelles Herunterfahren, indem die **IMAPIClientShutdown::QueryFastShutdown-Methode aufgerufen** wird.</span><span class="sxs-lookup"><span data-stu-id="23651-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="23651-131">Das MAPI-Subsystem antwortet auf die Abfrage des MAPI-Clients, indem es überprüft, ob geladene MAPI-Anbieter das schnelle Herunterfahren des Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="23651-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="23651-132">Der Administrator kann mithilfe Windows Registrierungseinstellungen bestimmen, welche Stufe der Anbieterunterstützung erforderlich ist, damit MAPI-Clients mit dem schnellen Herunterfahren fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="23651-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="23651-133">Weitere Informationen finden Sie unter [Fast Shutdown User Options](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="23651-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="23651-134">Um mit dem schnellen Herunterfahren fortzufahren, ruft der Client die **IMAPIClientShutdown::NotifyProcessShutdown-Methode** auf, um dem MAPI-Subsystem die Absicht zum Herunterfahren anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="23651-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="23651-135">Der Client ruft dann die **IMAPIClientShutdown::D oFastShutdown-Methode** auf, um anzugeben, dass der Clientprozess sofort beendet wird.</span><span class="sxs-lookup"><span data-stu-id="23651-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="23651-136">Weitere Informationen zum schnellen Herunterfahren finden Sie unter [Fast Shutdown Overview](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="23651-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="23651-137">Informationen zum erfolgreichen Schnellen Herunterfahren finden Sie unter [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="23651-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23651-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23651-138">See also</span></span>



[<span data-ttu-id="23651-139">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="23651-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="23651-140">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="23651-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

