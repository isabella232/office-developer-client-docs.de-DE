---
title: Arten von Transportanbietern
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
# <a name="types-of-transport-providers"></a>Arten von Transportanbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Transportanbieter unterstützen eine Reihe von Standardfeatures, z. B.:
  
- Bereitstellen der richtigen Sicherheit für das zugrunde liegende Messagingsystem.
    
- Senden und Empfangen von Nachrichten vom zugrunde liegenden Messagingsystem.
    
- Das Verfügbar machen der Adresstypen, die von den Transportanbietern unterstützt werden, damit der MAPI-Spooler und Clientanwendungen sie entsprechend verwenden können.
    
- Akzeptieren der Zustellung für bestimmte Empfänger.
    
Darüber hinaus unterstützt MAPI zwei spezielle Anbietertypen für bestimmte Messagingsysteme.
  
|**Transporttyp**|**Funktionalität hinzugefügt**|
|:-----|:-----|
|Remote-Transport  <br/> |Ermöglicht die Interoperabilität mit Remoteclients.  <br/> |
|TNEF-Transport  <br/> |Ermöglicht das Beibehalten von MAPI-Eigenschaften auf Messagingsystemen, die sie nicht unterstützen.  <br/> |
   
TNEF-Transporte werden zum Übersetzen von Nachrichten zwischen Messagingsystemen verwendet, die unterschiedliche Sätze von MAPI-Eigenschaften unterstützen. TNEF-Transporte verwenden die MAPI [ITnef : IUnknown-Schnittstelle,](itnefiunknown.md) um eigenschaften, die das Zielsystem nicht direkt darstellen kann, in einen binären Datenstrom zu konvertieren, der an die Nachricht angefügt werden kann. Später kann ein anderer TNEF-Transport **ITnef** verwenden, um den Datenstrom zu decodieren und die ursprünglichen MAPI-Eigenschaften clientanwendungen zur Verfügung zu stellen. Darüber hinaus ist TNEF-Unterstützung erforderlich, wenn Ihr Transport benutzerdefinierte Nachrichtenklassen unterstützen muss. Informationen zum Implementieren von TNEF-Transporten finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
  
Wenn Ihr Transportanbieter nicht einer dieser Typen ist, müssen Sie ihn mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen implementieren, die auf Ihrer Zielplattform verfügbar sind.
  

