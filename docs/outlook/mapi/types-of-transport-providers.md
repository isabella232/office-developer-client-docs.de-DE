---
title: Arten von Transportanbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 38cf068c8f05dcd540973760ffe228eb81dbeef8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566262"
---
# <a name="types-of-transport-providers"></a>Arten von Transportanbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Transportanbieter unterstützen eine Reihe von Standardfeatures, z. B.:
  
- Bereitstellen der richtigen Sicherheit für das zugrunde liegende Messagingsystem.
    
- Senden und Empfangen von Nachrichten aus dem zugrunde liegenden Messagingsystem.
    
- Verfügbarmachen der Adresstypen, die von den Transportanbietern unterstützt werden, damit die MAPI-Spooler und Clientanwendungen diese ordnungsgemäß verwenden können.
    
- Akzeptieren der Zustellung für bestimmte Empfänger.
    
Darüber hinaus unterstützt die MAPI zwei spezielle Anbietertypen für bestimmte Messagingsysteme.
  
|**Transporttyp**|**Funktionalität hinzugefügt**|
|:-----|:-----|
|Remote-Transport  <br/> |Ermöglicht die Interoperabilität mit remote verbundenen Clients.  <br/> |
|TNEF-Transport  <br/> |Ermöglicht das Beibehalten von MAPI-Eigenschaften auf Messagingsystemen, die diese nicht unterstützen.  <br/> |
   
TNEF-Transporte werden zum Übersetzen von Nachrichten zwischen Messagingsystemen verwendet, die unterschiedliche Sätze von MAPI-Eigenschaften unterstützen. TNEF-Transporte verwenden die MAPI [ITnef : IUnknown-Schnittstelle,](itnefiunknown.md) um alle Eigenschaften zu konvertieren, die das Zielsystem nicht direkt in einen binären Datenstrom darstellen kann, der an die Nachricht angefügt werden kann. Später kann ein anderer TNEF-Transport **ITnef** verwenden, um den Datenstrom zu decodieren und die ursprünglichen MAPI-Eigenschaften für Clientanwendungen verfügbar zu machen. Darüber hinaus ist TNEF-Unterstützung erforderlich, wenn Ihr Transport benutzerdefinierte Nachrichtenklassen unterstützen muss. Informationen zum Implementieren von TNEF-Transporten finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
  
Wenn Ihr Transportanbieter keiner dieser Typen ist, müssen Sie ihn mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen implementieren, die auf Ihrer Zielplattform verfügbar sind.
  

