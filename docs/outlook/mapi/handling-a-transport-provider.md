---
title: Behandeln eines Transportdienstes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567951"
---
# <a name="handling-a-transport-provider"></a>Behandeln eines Transportdienstes
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clients kommunizieren mit Transportanbieter über Status Objekte von Transportanbieter sowie die MAPI-Warteschlange bereitgestellt wird. Clientzugriff Status Objekte durch Aufrufen von [IMAPISession::GetStatusTable](imapisession-getstatustable.md) zum Abrufen der Statustabelle. Status-Objekten Implementieren der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle, die verfügt über Methoden für das Konfigurieren von Anbietern, das leeren eingehende und ausgehende Warteschlangen, Festlegen von Kennwörtern und Zustand Validierung Nachricht. Weitere Informationen zu Status-Objekten finden Sie unter [Statustabelle und Status Objekte](status-table-and-status-objects.md).


- [Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt, wie Sie senden oder Empfangen einer Nachricht bei Bedarf.
    
- [Einstellung Transport Reihenfolge](setting-transport-order.md): Beschreibt, wie Sie die Transport-Reihenfolge festlegen.
    
- [Neukonfigurieren eines Transportdienstes](reconfiguring-a-transport-provider.md): Beschreibt, wie ein Transportdienst neu konfigurieren, und welche Eigenschaften festlegen zur Verfügung stehen.
    

