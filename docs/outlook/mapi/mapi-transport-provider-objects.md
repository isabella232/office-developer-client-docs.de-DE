---
title: MAPI-Transport-Anbieter-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de0334ee9a90da38e472571314136195c84a7866
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592703"
---
# <a name="mapi-transport-provider-objects"></a>MAPI-Transport-Anbieter-Objekte
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zu den standardmäßigen Provider und Logon-Objekten, die von allen Dienstanbietern implementiert werden Transportanbieter erforderlich, um einem Statusobjekt implementiert werden. Implementieren ein Statusobjekt ist für die anderen Anbieter Diensttypen optional. Muss allerdings MAPI für Transportanbieter. Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle. 
  
Die folgende Abbildung zeigt alle Objekte, die Transportanbieter mit ihren entsprechenden Schnittstellen implementieren können. Die Abbildung wird angegeben, ob MAPI oder ein Client das Objekt-Benutzer ist.
  
![Objekte, mit denen Transportanbieter implementiert] (media/amapi_66.gif "Objekte, mit denen Transportanbieter implementiert")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieterobjekten](mapi-service-provider-objects.md)

