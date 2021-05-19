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
# <a name="handling-a-transport-provider"></a>Behandeln eines Transportanbieters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients kommunizieren mit Transportanbietern über Statusobjekte, die von Transportanbietern und dem MAPI-Spooler bereitgestellt werden. Clients greifen auf Statusobjekte zu, indem [SIE IMAPISession::GetStatusTable aufrufen,](imapisession-getstatustable.md) um die Statustabelle abzurufen. Status-Objekte implementieren die [IMAPIStatus : IMAPIProp-Schnittstelle,](imapistatusimapiprop.md) die Methoden zum Konfigurieren von Anbietern, Leeren eingehender und ausgehender Nachrichtenwarteschlangen, Festlegen von Kennwörtern und Statusüberprüfung enthält. Weitere Informationen zu Statusobjekten finden Sie unter [Statustabelle und Statusobjekte](status-table-and-status-objects.md).


- [Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt, wie eine Nachricht bei Bedarf gesendet oder empfangen wird.
    
- [Festlegen der Transportreihenfolge](setting-transport-order.md): Beschreibt, wie Transportreihenfolge festgelegt wird.
    
- [Neukonfigurieren eines Transportanbieters:](reconfiguring-a-transport-provider.md)Beschreibt, wie ein Transportanbieter neu konfiguriert wird und welche Eigenschaften festgelegt werden können.
    

