---
title: MAPI-Status Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309534"
---
# <a name="mapi-status-objects"></a>MAPI-Status Objekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Status Objekte melden Informationen zu MAPI-Ressourcen. Beispielsweise ein Dienstanbieter, der MAPI-Übermittlungsprozess oder das Adressbuch.
  
Es gibt ein Status-Objekt, das Informationen zu jedem einzelnen Dienstanbieter im aktuellen Profil bereitstellt. MAPI ist für die Implementierung von Statusobjekten für das Subsystem, den MAPI-Sende-und Empfangsprozess und das Adressbuch verantwortlich. Das Subsystem Status-Objekt liefert globale Informationen. Das Status-Objekt für das integrierte Adressbuch liefert den Status aller Adressbuchanbieter, die derzeit in Betrieb sind.
  
Jedes Status-Objekt ist in der Statustabelle enthalten, eine von MAPI verwaltete Tabelle, die Clients alle Statusinformationen für die Sitzung bereitstellt. Weitere Informationen finden Sie unter [Status Tabellen](status-tables.md). Clients können über die Tabelle oder, bei einem Dienstanbieter, über das Anmeldeobjekt auf ein bestimmtes Statusobjekt zugreifen. Um beispielsweise auf das Statusobjekt eines Adressbuch Anbieters zuzugreifen, kann ein Client **IABLogon:: OpenStatusEntry**aufrufen. Weitere Informationen finden Sie unter [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).
  
Clients können Status-Objekte für folgende Zwecke verwenden:
  
- Erfahren Sie mehr über den Status einer Sitzung.
    
- Überwachen eines Dienstanbieters.
    
- Steuern der Nachrichtenübertragung.
    
- Anzeigen oder Ändern der Konfiguration und des Status einer Ressource.
    
Jedes Status-Objekt implementiert die **IMAPIStatus** -Schnittstelle. Weitere Informationen finden Sie unter [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). Allerdings unterstützt nicht jedes Status-Objekt vollständig jede **IMAPIStatus** -Methode. Da es in den von einem Status-Objekt unterstützten Methoden Variationen gibt, müssen sich die Clients über ein bestimmtes Statusobjekt informieren, bevor es verwendet werden kann. Status Objekte sind erforderlich, um Informationen zu Ihren Features in den folgenden drei Eigenschaften zu veröffentlichen: 
  
 **PR_RESOURCE_METHODS** ([Pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md)) 
  
Weitere Informationen zum Implementieren eines Status-Objekts finden Sie unter [Status Object Implementation](status-object-implementation.md). Weitere Informationen zur Verwendung eines Status-Objekts finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).
  

