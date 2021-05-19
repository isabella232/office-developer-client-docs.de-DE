---
title: Behandeln eines Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416538"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="162b8-103">Behandeln eines Transportanbieters</span><span class="sxs-lookup"><span data-stu-id="162b8-103">Handling a transport provider</span></span>
  
<span data-ttu-id="162b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="162b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="162b8-105">Clients kommunizieren mit Transportanbietern über Statusobjekte, die von Transportanbietern und dem MAPI-Spooler bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="162b8-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="162b8-106">Clients greifen auf Statusobjekte zu, indem [SIE IMAPISession::GetStatusTable aufrufen,](imapisession-getstatustable.md) um die Statustabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="162b8-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="162b8-107">Status-Objekte implementieren die [IMAPIStatus : IMAPIProp-Schnittstelle,](imapistatusimapiprop.md) die Methoden zum Konfigurieren von Anbietern, Leeren eingehender und ausgehender Nachrichtenwarteschlangen, Festlegen von Kennwörtern und Statusüberprüfung enthält.</span><span class="sxs-lookup"><span data-stu-id="162b8-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="162b8-108">Weitere Informationen zu Statusobjekten finden Sie unter [Statustabelle und Statusobjekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="162b8-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="162b8-109">[Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt, wie eine Nachricht bei Bedarf gesendet oder empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="162b8-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="162b8-110">[Festlegen der Transportreihenfolge](setting-transport-order.md): Beschreibt, wie Transportreihenfolge festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="162b8-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="162b8-111">[Neukonfigurieren eines Transportanbieters:](reconfiguring-a-transport-provider.md)Beschreibt, wie ein Transportanbieter neu konfiguriert wird und welche Eigenschaften festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="162b8-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

