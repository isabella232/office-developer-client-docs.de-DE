---
title: Nachrichtendienst Implementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356917"
---
# <a name="message-service-implementation"></a>Nachrichtendienst Implementierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Nachrichtendienst ist ein oder mehrere verwandte Dienstanbieter, die zum Zweck der Vereinfachung der Installation und Konfiguration gruppiert sind. Alle Dienstanbieter sollten in einen Nachrichtendienst aufgenommen werden.
  
Gehen Sie folgendermaßen vor, um einen Nachrichtendienst mit einem oder mehreren Anbietern zu implementieren:
  
1. Entwerfen Sie den Nachrichtendienst, und bestimmen Sie die Anzahl und den Typ der einzuschließenden Dienstanbieter. Weitere Informationen zum Entwerfen eines Nachrichtendiensts finden Sie unter [Entwerfen eines Nachrichtendiensts](designing-a-message-service.md).
    
2. Erstellen Sie ein Setupprogramm zum Installieren der Dienstanbieter im Nachrichtendienst. Weitere Informationen zum Schreiben eines Nachrichtendienst-Setupprogramms finden Sie unter [unterstützen der Nachrichtendienst Installation](supporting-message-service-installation.md). 
    
3. Erstellen Sie eine Einstiegspunktfunktion, um die Konfiguration auszuführen. Weitere Informationen zum Schreiben einer Einstiegspunktfunktion für den Nachrichtendienst finden Sie unter [unterstützen von Nachrichtendienst Konfiguration](supporting-message-service-configuration.md) und [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Erstellen Sie eine öffentliche Headerdatei, die die Eigenschaftentags und Beschreibungen gültiger Werte für benutzerdefinierte Eigenschaften enthält, die vom Nachrichtendienst unterstützt werden. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

