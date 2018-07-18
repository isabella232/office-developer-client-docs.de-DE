---
title: MAPI-Status-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793094"
---
# <a name="mapi-status-objects"></a>MAPI-Status-Objekte

  
  
**Betrifft**: Outlook 
  
Status-Objekten ein Bericht mit Informationen zu MAPI-Ressourcen. Beispielsweise einem Dienstanbieter, die MAPI-senden-empfangen-Prozess oder im Adressbuch.
  
Es ist ein Statusobjekt, das Informationen zu jeder einzelnen Dienstanbieter im aktuellen Profil angeben. MAPI ist verantwortlich für die Implementierung der Status-Objekte für das Subsystem, der MAPI-Prozess senden/empfangen und im Adressbuch. Das Subsystem Status-Objekt stellt globalen Informationen zur Verfügung. Das Statusobjekt für das integrierte-Adressbuch liefert den Status aller Address Book Anbieter aktuell ausgeführten.
  
Jedes Statusobjekt ist in der Statustabelle, einer Tabelle, MAPI, das mit allen die Statusinformationen für die Sitzung Clients bietet verwaltet enthalten. Weitere Informationen finden Sie unter [Statustabellen](status-tables.md). Clients können einen bestimmten Status-Objekt entweder durch die Tabelle oder bei einem Dienstanbieter, über die Anmeldung-Objekt zugreifen. Um eine Adressbuchanbieter Statusobjekt zuzugreifen, kann ein Client beispielsweise **IABLogon::OpenStatusEntry**aufrufen. Weitere Informationen finden Sie unter [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Clients können Status-Objekte zu verwenden:
  
- Informationen Sie zu den Status einer Sitzung.
    
- Überwachen von einem Dienstanbieter.
    
- Steuern Sie Nachrichtenübermittlung.
    
- Zeigen Sie an oder ändern Sie einer Ressource Konfigurations- und Statusinformationen.
    
Jedes Statusobjekt implementiert die **IMAPIStatus** -Schnittstelle. Weitere Informationen finden Sie unter [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). Allerdings werden nicht jedes Statusobjekt jede Methode **IMAPIStatus** vollständig unterstützt. Da es Variation in den Methoden, die durch ein Statusobjekt unterstützt werden ist, müssen Clients über einen bestimmten Status-Objekt zu informieren, bevor es verwendet werden kann. Status-Objekte sind zum Veröffentlichen von Informationen über ihre Features in den folgenden drei Eigenschaften erforderlich: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Weitere Informationen zum Implementieren eines Objekts Status finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md). Weitere Informationen zum Verwenden einer Status-Objekts finden Sie unter [Statustabelle und Status-Objekte](status-table-and-status-objects.md).
  

