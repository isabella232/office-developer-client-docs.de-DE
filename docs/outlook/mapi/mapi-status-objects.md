---
title: MAPI-Statusobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2572e7d5d203a53de5c28a5eed0acbf415b81da2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579488"
---
# <a name="mapi-status-objects"></a>MAPI-Statusobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Statusobjekte melden Informationen zu MAPI-Ressourcen. Beispielsweise ein Dienstanbieter, der MAPI-Sende-/Empfangsprozess oder das Adressbuch.
  
Es gibt ein Statusobjekt, das Informationen zu jedem einzelnen Dienstanbieter im aktuellen Profil angibt. Die MAPI ist für die Implementierung von Statusobjekten für das Subsystem, den MAPI-Sende-/Empfangsprozess und das Adressbuch verantwortlich. Das Subsystemstatusobjekt liefert globale Informationen. Das Statusobjekt für das integrierte Adressbuch gibt den Status aller derzeit tätigen Adressbuchanbieter an.
  
Jedes Statusobjekt ist in der Statustabelle enthalten, einer Von MAPI verwalteten Tabelle, die Clients alle Statusinformationen für die Sitzung bereitstellt. Weitere Informationen finden Sie unter [Statustabellen.](status-tables.md) Clients können auf ein bestimmtes Statusobjekt entweder über die Tabelle oder für einen Dienstanbieter über sein Anmeldeobjekt zugreifen. Um beispielsweise auf das Statusobjekt eines Adressbuchanbieters zuzugreifen, kann ein Client **IABLogon::OpenStatusEntry** aufrufen. Weitere Informationen finden Sie unter [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Clients können Statusobjekte für Folgendes verwenden:
  
- Erfahren Sie mehr über den Status einer Sitzung.
    
- Überwachen eines Dienstanbieters.
    
- Steuern der Nachrichtenübertragung.
    
- Anzeigen oder Ändern der Konfiguration und des Status einer Ressource.
    
Jedes Statusobjekt implementiert die **IMAPIStatus-Schnittstelle.** Weitere Informationen finden Sie unter [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md). Nicht jedes Statusobjekt unterstützt jedoch alle **IMAPIStatus-Methoden** vollständig. Da es unterschiedliche Methoden gibt, die von einem Statusobjekt unterstützt werden, müssen Clients sich über ein bestimmtes Statusobjekt informieren, bevor sie es verwenden können. Statusobjekte sind erforderlich, um Informationen zu ihren Features in den folgenden drei Eigenschaften zu veröffentlichen: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Weitere Informationen zum Implementieren eines Statusobjekts finden Sie unter [Status Object Implementation](status-object-implementation.md). Weitere Informationen zur Verwendung eines Statusobjekts finden Sie unter [Status Table and Status Objects](status-table-and-status-objects.md).
  

