---
title: Nachrichtendienstimplementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c7007c01803676412b3efca8b7825b2ed8d863e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582483"
---
# <a name="message-service-implementation"></a>Nachrichtendienstimplementierung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Nachrichtendienst ist eine oder mehrere verwandte Dienstanbieter zur Vereinfachung der Installation und Konfiguration von gruppiert. Alle-Dienstanbieter sollten in einem Nachrichtendienst enthalten sein.
  
Um einen Nachrichtendienst mit einem oder mehreren Dienstanbietern implementieren möchten, verwenden Sie die folgende Schritte aus:
  
1. Entwerfen Sie den Dienst, Bestimmen der Anzahl und Typ der Dienstanbieter eingeschlossen werden. Weitere Informationen zum Entwerfen einer Messagingdiensts finden Sie unter [Entwerfen einer Messagingdiensts](designing-a-message-service.md).
    
2. Erstellen Sie ein Setup-Programm, die-Dienstanbieter in den Dienst zu installieren. Weitere Informationen zum Schreiben einer Nachricht Service Setup-Programm finden Sie unter [Message Service-Installation unterstützt](supporting-message-service-installation.md). 
    
3. Erstellen Sie eine Eintrag Point-Funktion zum Konfigurationsschritte ausführen. Weitere Informationen zum Schreiben eines Nachricht Diensteintrag Funktion finden Sie [Unterstützung Nachricht Dienstkonfiguration](supporting-message-service-configuration.md) und [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Erstellen Sie eine öffentliche Headerdatei die Eigenschaftentags und enthält eine Beschreibung der gültigen Werte für alle benutzerdefinierten Eigenschaften, die der Dienst unterstützt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

