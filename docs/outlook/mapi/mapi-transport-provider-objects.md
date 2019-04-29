---
title: MAPI-Transportanbieter Objekte
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
# <a name="mapi-transport-provider-objects"></a>MAPI-Transportanbieter Objekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zu den Standardanbieter-und anmeldeobjekten, die von allen Dienstanbietern implementiert werden, müssen Transportanbieter ein Status-Objekt implementieren. Für die anderen Dienstanbieter Typen ist die Implementierung eines Status-Objekts optional. MAPI ist jedoch für Transportanbieter erforderlich. Transport Anbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle. 
  
In der folgenden Abbildung sind alle Objekte dargestellt, die Transportanbieter mit den entsprechenden Schnittstellen implementieren können. Die Abbildung gibt auch an, ob MAPI oder ein Client der Benutzer des Objekts ist.
  
Von ![Transportanbietern implementierte Objekte] Von (media/amapi_66.gif "Transportanbietern implementierte Objekte")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieter Objekte](mapi-service-provider-objects.md)

