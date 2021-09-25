---
title: Erforderliche Funktionen für Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b08057ce597459988fc443f5e7495b45fdef56a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578795"
---
# <a name="required-functionality-for-transport-providers"></a>Erforderliche Funktionen für Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jeder MAPI-Transportanbieter muss:
  
- Befolgen Sie die allgemeinen Richtlinien für die Arbeit mit MAPI und anderen Dienstanbietern. Weitere Informationen finden Sie unter [MAPI-Anwendungsentwicklung](mapi-application-development.md) und [MAPI-Dienstanbieter.](mapi-service-providers.md)
    
- Lassen Sie die DLL des Transportanbieters für MAPI die [XPProviderInit-Initialisierungsfunktion](xpproviderinit.md) verfügbar. 
    
- Verfügbarmachen der MAPI-Implementierung der [IXPProvider: IUnknown-](ixpprovideriunknown.md) und [IXPLogon : IUnknown-Schnittstellen.](ixplogoniunknown.md) 
    
- Machen Sie die Implementierung der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) für MAPI- und Clientanwendungen verfügbar. Weitere Informationen zum Implementieren von **IMAPIStatus** finden Sie unter [Status Object Implementation](status-object-implementation.md). 
    
- Implementieren eines Eigenschaftenfenster-Dialogfelds für die Konfiguration. Weitere Informationen zum Implementieren von Eigenschaftenblättern finden Sie unter [Property Sheet-Implementierung.](property-sheet-implementation.md)
    

