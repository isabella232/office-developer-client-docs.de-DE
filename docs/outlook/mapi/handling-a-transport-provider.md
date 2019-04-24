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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299496"
---
# <a name="handling-a-transport-provider"></a>Behandeln eines Transportanbieters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients kommunizieren mit Transportanbietern über Statusobjekte, die von Transportanbietern und dem MAPI-Spooler bereitgestellt werden. Clients greifen auf Statusobjekte zu, indem Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable aufrufen, um die Statustabelle abzurufen. Status Objekte implementieren Sie die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle, die über Methoden zum Konfigurieren von Anbietern, das Leeren von eingehenden und ausgehenden Nachrichtenwarteschlangen, das Festlegen von Kennwörtern und die Statusüberprüfung verfügt. Weitere Informationen zu Statusobjekten finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).


- [Senden oder Empfangen einer Nachricht bei Bedarf](sending-or-receiving-a-message-on-demand.md): Beschreibt das Senden oder Empfangen einer Nachricht bei Bedarf.
    
- [Festlegen des Transportauftrags](setting-transport-order.md): Beschreibt das Festlegen des Transportauftrags.
    
- [Neukonfigurieren eines Transportanbieters](reconfiguring-a-transport-provider.md): Beschreibt, wie ein Transportanbieter neu konfiguriert wird und welche Eigenschaften festgelegt werden können.
    

