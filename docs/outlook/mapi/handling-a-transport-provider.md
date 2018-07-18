---
title: Behandeln eines Transportdienstes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 140fe97662f7a2ce68c18d8e0eb991d0819da6dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791786"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="39989-103">Behandeln eines Transportdienstes</span><span class="sxs-lookup"><span data-stu-id="39989-103">Handling a transport provider</span></span>
  
<span data-ttu-id="39989-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39989-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39989-105">Clients kommunizieren mit Transportanbieter über Status Objekte von Transportanbieter sowie die MAPI-Warteschlange bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="39989-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="39989-106">Clientzugriff Status Objekte durch Aufrufen von [IMAPISession::GetStatusTable](imapisession-getstatustable.md) zum Abrufen der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="39989-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="39989-107">Status-Objekten Implementieren der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle, die verfügt über Methoden für das Konfigurieren von Anbietern, das leeren eingehende und ausgehende Warteschlangen, Festlegen von Kennwörtern und Zustand Validierung Nachricht.</span><span class="sxs-lookup"><span data-stu-id="39989-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="39989-108">Weitere Informationen zu Status-Objekten finden Sie unter [Statustabelle und Status Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="39989-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="39989-109">[Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt, wie Sie senden oder Empfangen einer Nachricht bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="39989-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="39989-110">[Einstellung Transport Reihenfolge](setting-transport-order.md): Beschreibt, wie Sie die Transport-Reihenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="39989-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="39989-111">[Neukonfigurieren eines Transportdienstes](reconfiguring-a-transport-provider.md): Beschreibt, wie ein Transportdienst neu konfigurieren, und welche Eigenschaften festlegen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="39989-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

