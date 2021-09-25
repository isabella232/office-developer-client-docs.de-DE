---
title: MAPI-Transportanbieterobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b40413a67c3f2f91ece77b929c658c1b5256567e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556134"
---
# <a name="mapi-transport-provider-objects"></a>MAPI-Transportanbieterobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zu den Standardanbieter- und Anmeldeobjekten, die von allen Dienstanbietern implementiert werden, müssen Transportanbieter ein Statusobjekt implementieren. Für die anderen Dienstanbietertypen ist die Implementierung eines Statusobjekts optional. Die MAPI erfordert sie jedoch für Transportanbieter. Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle. 
  
Die folgende Abbildung zeigt jedes der Objekte, die Transportanbieter mit den entsprechenden Schnittstellen implementieren können. Die Abbildung zeigt auch an, ob MAPI oder ein Client der Benutzer des Objekts ist.
  
![Von Transportanbietern implementierte Objekte](media/amapi_66.gif "Von Transportanbietern implementierte Objekte")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieterobjekte](mapi-service-provider-objects.md)

