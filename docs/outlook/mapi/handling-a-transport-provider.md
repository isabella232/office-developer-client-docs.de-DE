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
# <a name="handling-a-transport-provider"></a>Behandeln eines Transportdienstes
  
**Betrifft**: Outlook 
  
Clients kommunizieren mit Transportanbieter über Status Objekte von Transportanbieter sowie die MAPI-Warteschlange bereitgestellt wird. Clientzugriff Status Objekte durch Aufrufen von [IMAPISession::GetStatusTable](imapisession-getstatustable.md) zum Abrufen der Statustabelle. Status-Objekten Implementieren der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle, die verfügt über Methoden für das Konfigurieren von Anbietern, das leeren eingehende und ausgehende Warteschlangen, Festlegen von Kennwörtern und Zustand Validierung Nachricht. Weitere Informationen zu Status-Objekten finden Sie unter [Statustabelle und Status Objekte](status-table-and-status-objects.md).


- [Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt, wie Sie senden oder Empfangen einer Nachricht bei Bedarf.
    
- [Einstellung Transport Reihenfolge](setting-transport-order.md): Beschreibt, wie Sie die Transport-Reihenfolge festlegen.
    
- [Neukonfigurieren eines Transportdienstes](reconfiguring-a-transport-provider.md): Beschreibt, wie ein Transportdienst neu konfigurieren, und welche Eigenschaften festlegen zur Verfügung stehen.
    

