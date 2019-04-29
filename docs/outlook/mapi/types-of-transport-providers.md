---
title: Arten von Transport Anbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406164"
---
# <a name="types-of-transport-providers"></a>Arten von Transport Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Transportanbieter unterstützen eine Reihe von Standardfunktionen, wie zum Beispiel:
  
- Bereitstelleneiner ordnungsgemäßen Sicherheit für das zugrunde liegende Messagingsystem
    
- Senden und empfangen von Nachrichten vom zugrunde liegenden Messagingsystem.
    
- Verfügbar machen der Adresstypen, die von den Transportanbietern unterstützt werden, damit die MAPI-Spooler-und Clientanwendungen Sie entsprechend verwenden können.
    
- Annehmen der Lieferung für bestimmte Empfänger.
    
Darüber hinaus unterstützt MAPI zwei spezielle Typen von Anbietern für bestimmte Messagingsysteme.
  
|**Transporttyp**|**HinzugeFügte Funktionalität**|
|:-----|:-----|
|Remote Transport  <br/> |Ermöglicht die Interoperabilität mit Clients, die Remote verbunden sind.  <br/> |
|TNEF-Transport  <br/> |Ermöglicht die Bewahrung von MAPI-Eigenschaften auf Messagingsystemen, die Sie nicht unterstützen.  <br/> |
   
TNEF-Übertragungen werden zum Übersetzen von Nachrichten zwischen Messagingsystemen verwendet, die unterschiedliche MAPI-Eigenschaften unterstützen. TNEF-Übertragungen verwenden die MAPI- [ITnef: IUnknown](itnefiunknown.md) -Schnittstelle zum Konvertieren von Eigenschaften, die vom Zielsystem nicht direkt in einen binären Datenstrom, der an die Nachricht angefügt werden kann, dargestellt werden können. Später kann ein anderer TNEF-Transport **ITnef** verwenden, um den Datenstrom zu decodieren und die ursprünglichen MAPI-Eigenschaften für Clientanwendungen zur Verfügung zu stellen. Darüber hinaus ist die TNEF-Unterstützung erforderlich, wenn der Transport benutzerdefinierte Nachrichtenklassen unterstützen muss. Weitere Informationen zum Implementieren von TNEF-Transporten finden Sie unter [Entwickeln eines TNEF-fähigen](developing-a-tnef-enabled-transport-provider.md)Transportanbieters.
  
Wenn es sich bei Ihrem Transportanbieter nicht um einen dieser Typen handelt, müssen Sie ihn mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen implementieren, die auf der Zielplattform zur Verfügung stehen.
  

