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
# <a name="handling-a-transport-provider"></a><span data-ttu-id="b1fbb-103">Behandeln eines Transportanbieters</span><span class="sxs-lookup"><span data-stu-id="b1fbb-103">Handling a transport provider</span></span>
  
<span data-ttu-id="b1fbb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1fbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1fbb-105">Clients kommunizieren mit Transportanbietern über Statusobjekte, die von Transportanbietern und dem MAPI-Spooler bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b1fbb-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="b1fbb-106">Clients greifen auf Statusobjekte zu, indem Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable aufrufen, um die Statustabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b1fbb-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="b1fbb-107">Status Objekte implementieren Sie die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle, die über Methoden zum Konfigurieren von Anbietern, das Leeren von eingehenden und ausgehenden Nachrichtenwarteschlangen, das Festlegen von Kennwörtern und die Statusüberprüfung verfügt.</span><span class="sxs-lookup"><span data-stu-id="b1fbb-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="b1fbb-108">Weitere Informationen zu Statusobjekten finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b1fbb-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="b1fbb-109">[Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt das Senden oder Empfangen einer Nachricht bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="b1fbb-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="b1fbb-110">[Festlegen des Transportauftrags](setting-transport-order.md): Beschreibt das Festlegen des Transportauftrags.</span><span class="sxs-lookup"><span data-stu-id="b1fbb-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="b1fbb-111">[Neukonfigurieren eines Transportanbieters](reconfiguring-a-transport-provider.md): Beschreibt, wie ein Transportanbieter neu konfiguriert wird und welche Eigenschaften festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="b1fbb-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

