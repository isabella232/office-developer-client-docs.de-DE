---
title: Erforderliche Funktionen für Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580495"
---
# <a name="required-functionality-for-transport-providers"></a>Erforderliche Funktionen für Transportanbieter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Jedes MAPI-Transportdienst muss:
  
- Führen Sie die allgemeinen Richtlinien für die Arbeit mit MAPI- und anderen Dienstanbieter. Weitere Informationen finden Sie unter [MAPI-Anwendungsentwicklung](mapi-application-development.md) und [MAPI-Dienstanbieter](mapi-service-providers.md).
    
- Der Adressbuchhierarchie DLL machen MAPI seine Initialisierungsfunktion [XPProviderInit](xpproviderinit.md) haben. 
    
- Die Implementierung von MAPI verfügbar machen die [IXPProvider: IUnknown](ixpprovideriunknown.md) und [IXPLogon: IUnknown](ixplogoniunknown.md) Schnittstellen. 
    
- Die Implementierung von für MAPI-und Clientanwendungen verfügbar machen die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle. Weitere Informationen zum Implementieren von **IMAPIStatus**finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md). 
    
- Implementieren Sie ein Blatt Eigenschaftendialogfeld für die Konfiguration. Weitere Informationen zum Implementieren von Eigenschaftenseiten finden Sie unter [Implementierung von Eigenschaften Blatt](property-sheet-implementation.md).
    

