---
title: Erforderliche Funktionalität für Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795396"
---
# <a name="required-functionality-for-transport-providers"></a>Erforderliche Funktionalität für Transportanbieter

  
  
**Betrifft**: Outlook 
  
Jedes MAPI-Transportdienst muss:
  
- Führen Sie die allgemeinen Richtlinien für die Arbeit mit MAPI- und anderen Dienstanbieter. Weitere Informationen finden Sie unter [MAPI-Anwendungsentwicklung](mapi-application-development.md) und [MAPI-Dienstanbieter](mapi-service-providers.md).
    
- Der Adressbuchhierarchie DLL machen MAPI seine Initialisierungsfunktion [XPProviderInit](xpproviderinit.md) haben. 
    
- Die Implementierung von MAPI verfügbar machen die [IXPProvider: IUnknown](ixpprovideriunknown.md) und [IXPLogon: IUnknown](ixplogoniunknown.md) Schnittstellen. 
    
- Die Implementierung von für MAPI-und Clientanwendungen verfügbar machen die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle. Weitere Informationen zum Implementieren von **IMAPIStatus**finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md). 
    
- Implementieren Sie ein Blatt Eigenschaftendialogfeld für die Konfiguration. Weitere Informationen zum Implementieren von Eigenschaftenseiten finden Sie unter [Implementierung von Eigenschaften Blatt](property-sheet-implementation.md).
    

