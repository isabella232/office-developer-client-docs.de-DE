---
title: Implementierung des Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434032"
---
# <a name="message-service-implementation"></a>Implementierung des Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einem Nachrichtendienst handelt es sich um einen oder mehrere verwandte Dienstanbieter, die zum Zweck der Vereinfachung der Installation und Konfiguration zusammen gruppieren. Alle Dienstanbieter sollten in einen Nachrichtendienst einbezogen werden.
  
Verwenden Sie das folgende Verfahren, um einen Nachrichtendienst mit einem oder mehreren Anbietern zu implementieren:
  
1. Entwerfen Sie den Nachrichtendienst, und bestimmen Sie die Anzahl und den Typ der Dienstanbieter, die einbezogen werden sollen. Weitere Informationen zum Entwerfen eines Nachrichtendiensts finden Sie unter [Designing a Message Service](designing-a-message-service.md).
    
2. Erstellen Sie ein Setupprogramm, um die Dienstanbieter im Nachrichtendienst zu installieren. Weitere Informationen zum Schreiben eines Nachrichtendienst-Setupprogramms finden Sie unter [Supporting Message Service Installation](supporting-message-service-installation.md). 
    
3. Erstellen Sie eine Einstiegspunktfunktion zum Ausführen der Konfiguration. Weitere Informationen zum Schreiben einer Nachrichtendienst-Einstiegspunktfunktion finden Sie unter [Supporting Message Service Configuration](supporting-message-service-configuration.md) und [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Erstellen Sie eine öffentliche Headerdatei, die die Eigenschaftstags und Beschreibungen gültiger Werte für alle benutzerdefinierten Eigenschaften enthält, die vom Nachrichtendienst unterstützt werden. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

