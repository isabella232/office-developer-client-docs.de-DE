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
ms.openlocfilehash: a9bba55b585b09d6a5779ba41a283b20c645656f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576232"
---
# <a name="types-of-transport-providers"></a>Arten von Transportanbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Transportanbieter für unterstützen einen Bereich von Standardfeatures, z. B.:
  
- Bereitstellen von ordnungsgemäße Sicherheit für die zugrunde liegenden messaging-System.
    
- Senden und Empfangen von Nachrichten aus dem zugrunde liegenden messaging-System.
    
- Verfügbarmachen der Adresstypen unterstützen die Transportanbieter, damit der MAPI-Warteschlange und Clientanwendungen entsprechend verwendet können.
    
- Akzeptieren von Übermittlung für bestimmte Empfänger.
    
MAPI unterstützt darüber hinaus zwei spezielle Arten von Anbietern für bestimmte messaging-Systeme.
  
|**Transporttyp**|**Zusätzliche Funktionalität**|
|:-----|:-----|
|Remote-Transport  <br/> |Ermöglicht die Interoperabilität mit Clients Remote verbunden.  <br/> |
|TNEF-Transport  <br/> |MAPI-Eigenschaften auf die messaging-Systeme, die diese nicht unterstützen beibehalten werden können.  <br/> |
   
TNEF Transporten dienen zum Übersetzen von Nachrichten zwischen messaging-Systemen, die verschiedene Sätze von MAPI-Eigenschaften zu unterstützen. TNEF Transporten verwenden Sie die MAPI [ITnef: IUnknown](itnefiunknown.md) -Schnittstelle für alle Eigenschaften, die das Zielsystem darstellen kann nicht direkt in einem binären Datenstrom zu konvertieren, die an die Nachricht angefügt werden können. Eine andere TNEF Transport kann später **ITnef** verwenden, um den Datenstrom decodieren und die ursprünglichen MAPI-Eigenschaften-Clientanwendungen zur Verfügung stellen. Darüber hinaus ist die TNEF-Unterstützung erforderlich, wenn Ihre Transport benutzerdefinierte Nachrichtenklassen unterstützen muss. Informationen zum Implementieren von TNEF Transporten finden Sie unter [Developing eines Transportdienstes TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
  
Wenn Ihre Adressbuchhierarchie nicht dieser Typen ist, müssen Sie mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen der Zielplattform verfügbar zu implementieren.
  

