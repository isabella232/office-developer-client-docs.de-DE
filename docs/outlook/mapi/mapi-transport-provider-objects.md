---
title: MAPI-Transport-Anbieter-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793099"
---
# <a name="mapi-transport-provider-objects"></a>MAPI-Transport-Anbieter-Objekte
  
**Betrifft**: Outlook 
  
Zusätzlich zu den standardmäßigen Provider und Logon-Objekten, die von allen Dienstanbietern implementiert werden Transportanbieter erforderlich, um einem Statusobjekt implementiert werden. Implementieren ein Statusobjekt ist für die anderen Anbieter Diensttypen optional. Muss allerdings MAPI für Transportanbieter. Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle. 
  
Die folgende Abbildung zeigt alle Objekte, die Transportanbieter mit ihren entsprechenden Schnittstellen implementieren können. Die Abbildung wird angegeben, ob MAPI oder ein Client das Objekt-Benutzer ist.
  
![Objekte, mit denen Transportanbieter implementiert] (media/amapi_66.gif "Objekte, mit denen Transportanbieter implementiert")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieterobjekten](mapi-service-provider-objects.md)

