---
title: Behandeln eines Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7196800185f2bd4216324ac9a5d65835e61582f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551527"
---
# <a name="handling-a-transport-provider"></a>Behandeln eines Transportanbieters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients kommunizieren mit Transportanbietern über Statusobjekte, die von Transportanbietern und dem MAPI-Spooler bereitgestellt werden. Clients greifen auf Statusobjekte zu, indem [sie IMAPISession::GetStatusTable](imapisession-getstatustable.md) aufrufen, um die Statustabelle abzurufen. Statusobjekte implementieren die [IMAPIStatus : IMAPIProp-Schnittstelle,](imapistatusimapiprop.md) die Methoden zum Konfigurieren von Anbietern, Leeren von Warteschlangen für eingehende und ausgehende Nachrichten, Festlegen von Kennwörtern und Statusüberprüfung enthält. Weitere Informationen zu Statusobjekten finden Sie unter [StatusTabelle und Statusobjekte.](status-table-and-status-objects.md)


- [Senden oder Empfangen einer Nachricht bei Bedarf:](sending-or-receiving-a-message-on-demand.md)Beschreibt, wie eine Nachricht bei Bedarf gesendet oder empfangen wird.
    
- [Festlegen der Transportreihenfolge:](setting-transport-order.md)Beschreibt das Festlegen der Transportreihenfolge.
    
- [Neukonfiguration eines Transportanbieters:](reconfiguring-a-transport-provider.md)Beschreibt, wie ein Transportanbieter neu konfiguriert wird und welche Eigenschaften festgelegt werden können.
    

