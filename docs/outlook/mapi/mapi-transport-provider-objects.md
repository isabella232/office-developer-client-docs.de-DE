---
title: OBJEKTE des MAPI-Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430357"
---
# <a name="mapi-transport-provider-objects"></a>OBJEKTE des MAPI-Transportanbieters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zu den von allen Dienstanbietern implementierten Standardanbieter- und Anmeldeobjekten müssen Transportanbieter ein Statusobjekt implementieren. Für die anderen Dienstanbietertypen ist die Implementierung eines Statusobjekts optional. MapI erfordert dies jedoch für Transportanbieter. Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle. 
  
Die folgende Abbildung zeigt jedes der Objekte, die Transportanbieter mit ihren entsprechenden Schnittstellen implementieren können. Die Abbildung gibt außerdem an, ob MAPI oder ein Client der Benutzer des Objekts ist.
  
![Objekte, die Transportanbieter implementieren Objekte,](media/amapi_66.gif "die von Transportanbietern implementiert werden")
  
## <a name="see-also"></a>Siehe auch

- [OBJEKTE des MAPI-Dienstanbieters](mapi-service-provider-objects.md)

