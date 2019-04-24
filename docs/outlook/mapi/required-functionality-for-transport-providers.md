---
title: Erforderliche Funktionen für Transport Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328686"
---
# <a name="required-functionality-for-transport-providers"></a>Erforderliche Funktionen für Transport Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jeder MAPI-Transportanbieter muss:
  
- BeFolgen Sie die allgemeinen Richtlinien für das Arbeiten mit MAPI und anderen Dienstanbietern. Weitere Informationen finden Sie unter [MAPI-Anwendungsentwicklung](mapi-application-development.md) und [MAPI-Dienstanbieter](mapi-service-providers.md).
    
- Lassen Sie die [XPProviderInit](xpproviderinit.md) -Initialisierungsfunktion ihrer Transportanbieter-dll für MAPI verfügbar. 
    
- Machen Sie für MAPI die Implementierung der [IXPProvider: IUnknown](ixpprovideriunknown.md) -und [IXPLogon: IUnknown](ixplogoniunknown.md) -Schnittstellen verfügbar. 
    
- Verfügbar machen für MAPI-und Clientanwendungen die Implementierung der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle. Weitere Informationen zum Implementieren von **IMAPIStatus**finden Sie unter [Status Object Implementation](status-object-implementation.md). 
    
- Implementieren Sie ein Eigenschaftenblatt-Dialogfeld für die Konfiguration. Weitere Informationen zum Implementieren von Eigenschaftenblättern finden Sie unter [Eigenschaftenblatt Implementierung](property-sheet-implementation.md).
    

