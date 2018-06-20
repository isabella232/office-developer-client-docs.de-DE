---
title: Nachricht Service-Implementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793258"
---
# <a name="message-service-implementation"></a>Nachricht Service-Implementierung

  
  
**Betrifft**: Outlook 
  
Ein Nachrichtendienst ist eine oder mehrere verwandte Dienstanbieter zur Vereinfachung der Installation und Konfiguration von gruppiert. Alle-Dienstanbieter sollten in einem Nachrichtendienst enthalten sein.
  
Um einen Nachrichtendienst mit einem oder mehreren Dienstanbietern implementieren möchten, verwenden Sie die folgende Schritte aus:
  
1. Entwerfen Sie den Dienst, Bestimmen der Anzahl und Typ der Dienstanbieter eingeschlossen werden. Weitere Informationen zum Entwerfen einer Messagingdiensts finden Sie unter [Entwerfen einer Messagingdiensts](designing-a-message-service.md).
    
2. Erstellen Sie ein Setup-Programm, die-Dienstanbieter in den Dienst zu installieren. Weitere Informationen zum Schreiben einer Nachricht Service Setup-Programm finden Sie unter [Message Service-Installation unterstützt](supporting-message-service-installation.md). 
    
3. Erstellen Sie eine Eintrag Point-Funktion zum Konfigurationsschritte ausführen. Weitere Informationen zum Schreiben eines Nachricht Diensteintrag Funktion finden Sie [Unterstützung Nachricht Dienstkonfiguration](supporting-message-service-configuration.md) und [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Erstellen Sie eine öffentliche Headerdatei die Eigenschaftentags und enthält eine Beschreibung der gültigen Werte für alle benutzerdefinierten Eigenschaften, die der Dienst unterstützt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

