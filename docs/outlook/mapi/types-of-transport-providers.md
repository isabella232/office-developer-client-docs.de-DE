---
title: Typen der Transportanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795767"
---
# <a name="types-of-transport-providers"></a>Typen der Transportanbieter

  
  
**Betrifft**: Outlook 
  
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
  

