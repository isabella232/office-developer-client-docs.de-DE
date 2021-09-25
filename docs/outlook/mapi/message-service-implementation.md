---
title: Message Service-Implementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83fdf520f3e4b8acaa5d304f4c5a2b642ebcd71e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625217"
---
# <a name="message-service-implementation"></a>Message Service-Implementierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Nachrichtendienst ist ein oder mehrere verwandte Dienstanbieter, die gruppiert sind, um die Installation und Konfiguration zu vereinfachen. Alle Dienstanbieter sollten in einen Nachrichtendienst eingeschlossen werden.
  
Verwenden Sie das folgende Verfahren, um einen Nachrichtendienst mit einem oder mehreren Anbietern zu implementieren:
  
1. Entwerfen Sie den Nachrichtendienst, und bestimmen Sie die Anzahl und den Typ der Dienstanbieter, die einbezogen werden sollen. Weitere Informationen zum Entwerfen eines Nachrichtendiensts finden Sie unter [Entwerfen eines Nachrichtendiensts.](designing-a-message-service.md)
    
2. Erstellen Sie ein Setupprogramm, um die Dienstanbieter im Nachrichtendienst zu installieren. Weitere Informationen zum Schreiben eines Nachrichtendienst-Setupprogramms finden Sie unter Unterstützen der [Nachrichtendienstinstallation.](supporting-message-service-installation.md) 
    
3. Erstellen Sie eine Einstiegspunktfunktion zum Ausführen der Konfiguration. Weitere Informationen zum Schreiben einer Nachrichtendienst-Einstiegspunktfunktion finden Sie unter "Unterstützen der [Nachrichtendienstkonfiguration"](supporting-message-service-configuration.md) und ["MSGSERVICEENTRY".](msgserviceentry.md) 
    
4. Erstellen Sie eine öffentliche Headerdatei, die die Eigenschaftentags und Beschreibungen gültiger Werte für alle benutzerdefinierten Eigenschaften enthält, die der Nachrichtendienst unterstützt. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

