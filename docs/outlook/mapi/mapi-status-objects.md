---
title: MAPI-Statusobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406745"
---
# <a name="mapi-status-objects"></a>MAPI-Statusobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Statusobjekte melden Informationen zu MAPI-Ressourcen. Beispielsweise ein Dienstanbieter, der MAPI-Sende-/Empfangsvorgang oder das Adressbuch.
  
Es gibt ein Statusobjekt, das Informationen zu den einzelnen Dienstanbietern im aktuellen Profil enthält. MAPI ist für die Implementierung von Statusobjekten für das Subsystem, den MAPI-Sende-/Empfangsvorgang und das Adressbuch verantwortlich. Das Subsystemstatusobjekt stellt globale Informationen zur Verfügung. Das Statusobjekt für das integrierte Adressbuch gibt den Status aller derzeit verwendeten Adressbuchanbieter an.
  
Jedes Statusobjekt ist in der Statustabelle enthalten, einer von MAPI verwalteten Tabelle, die Clients alle Statusinformationen für die Sitzung zur Verfügung stellt. Weitere Informationen finden Sie unter [Status Tables](status-tables.md). Clients können über die Tabelle oder für einen Dienstanbieter über das Anmeldeobjekt auf ein bestimmtes Statusobjekt zugreifen. Um beispielsweise auf das Statusobjekt eines Adressbuchanbieters zu zugreifen, kann ein Client **IABLogon::OpenStatusEntry aufrufen.** Weitere Informationen finden Sie unter [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Clients können Statusobjekte verwenden, um:
  
- Erfahren Sie mehr über den Status einer Sitzung.
    
- Überwachen eines Dienstanbieters.
    
- Steuern der Nachrichtenübertragung.
    
- Anzeigen oder Ändern der Konfiguration und des Status einer Ressource.
    
Jedes Statusobjekt implementiert die **IMAPIStatus-Schnittstelle.** Weitere Informationen finden Sie unter [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md). Nicht jedes Statusobjekt unterstützt jedoch jede **IMAPIStatus-Methode** vollständig. Da es Variationen in den Methoden gibt, die von einem Statusobjekt unterstützt werden, müssen Clients mehr über ein bestimmtes Statusobjekt erfahren, bevor sie es verwenden können. Statusobjekte müssen Informationen zu ihren Features in den folgenden drei Eigenschaften veröffentlichen: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Weitere Informationen zum Implementieren eines Statusobjekts finden Sie unter [Status Object Implementation](status-object-implementation.md). Weitere Informationen zur Verwendung eines Statusobjekts finden Sie unter [Status Table und Status Objects](status-table-and-status-objects.md).
  

