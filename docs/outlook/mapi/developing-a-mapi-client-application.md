---
title: Entwickeln einer MAPI-Clientanwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f33616b8dcf37179ea1acf33416ee3e1e0ad617
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561852"
---
# <a name="developing-a-mapi-client-application"></a>Entwickeln einer MAPI-Clientanwendung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Clientanwendungen werden mit der objektorientierten MAPI-Clientschnittstelle geschrieben. MAPI-Clients interagieren mit einem oder mehreren Messagingsystemen über das MAPI-Subsystem und MAPI-kompatible Dienstanbieter. Diese Interaktion kann auf viele verschiedene Arten erfolgen. Es gibt eine enorme Vielfalt in Clientanwendungen. Bei den meisten Clients handelt es sich um Messagingclients, die entweder Messaging in ihren eingerichteten Featuresatz integrieren oder Nachrichten als primäres Feature ausführen. Weitere Features, die MAPI-Clients möglicherweise bereitstellen, sind profilverwaltung oder Adressbuch- und Nachrichtenspeicherverwaltung.
  
Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten eine **Sitzung** mit dem MAPI-Subsystem. Weitere Informationen finden Sie unter [Zugreifen auf Objekte mithilfe der Sitzung.](accessing-objects-by-using-the-session.md) Nachdem eine Sitzung eingerichtet wurde, kann ein Client:
  
- Behandeln ausgehender Nachrichten, einschließlich Antworten, weitergeleiteter Nachrichten und erneuter Übermittlungen.
    
- Behandeln eingehender Nachrichten.
    
- Behandeln Sie den Nachrichtenspeicher, indem Sie Ordner und Nachrichten öffnen, Nachrichten erstellen, ändern, kopieren und senden, Unterhaltungen nachverfolgen und einen oder mehrere Ordner durchsuchen.
    
- Behandeln Sie das Adressbuch, indem Sie Empfänger erstellen und ändern, Einträge suchen und die Containerhierarchie durchlaufen.
    
- Behandeln Sie einen Transportanbieter, indem Sie neu konfigurieren, Optionen und Transportreihenfolge festlegen und Nachrichten bei Bedarf senden.
    
- Behandeln von Ereignisbenachrichtigungen.
    
- Verarbeiten von Formularen.
    
- Behandeln von Profilen und Nachrichtendiensten.
    
Verwenden Sie die Themen in diesem Abschnitt, um Ihnen bei der Implementierung dieser grundlegenden Aufgaben und der spezifischen Features zu helfen, die Ihren MAPI-Client einzigartig machen.
  

