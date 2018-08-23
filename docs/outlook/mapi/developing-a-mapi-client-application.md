---
title: Entwickeln einer MAPI-Clientanwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bffcfdd6d688c483655b97d61075b147430e3fcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564976"
---
# <a name="developing-a-mapi-client-application"></a>Entwickeln einer MAPI-Clientanwendung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI-Clientanwendungen werden mit der objektorientierte MAPI-Client-Schnittstelle geschrieben. MAPI-Clients interagieren mit Messagingsystemen über die MAPI-Subsystems und MAPI-kompatible-Dienstanbieter. Diese Interaktion kann auf verschiedene Weise auftreten. Es gibt eine enorme Vielfalt an in-Clientanwendungen. Die meisten Clients werden entweder Integration von messaging in ihren eingerichteten Featuregruppe oder Ausführen als ihre primäre Feature messaging-Clients messaging. Andere Features, die möglicherweise MAPI-Clients bereitstellen sind profilverwaltung oder Adressbuch und Nachricht Management zu speichern.
  
Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten Sie eine **Sitzung** mit MAPI-Subsystems. Weitere Informationen finden Sie unter [Zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md). Nachdem eine Sitzung eingerichtet wurde, können ein Client:
  
- Ausgehende Nachrichten, einschließlich Antworten, Nachrichten und hohem weitergeleitet behandelt.
    
- Eingehende Nachrichten behandelt.
    
- Behandeln des Nachrichtenspeichers durch Öffnen Ordner und Nachrichten, erstellen, ändern, kopieren, und Senden von Nachrichten, Nachverfolgen von Unterhaltungen, und suchen einen oder mehrere Ordner.
    
- Behandeln Sie das Adressbuch durch Erstellen und Ändern von Empfängern, Einträge suchen und Durchlaufen der Containerhierarchie.
    
- Behandeln eines Transportdienstes Neukonfiguration durchführen, Optionen und Transport-Reihenfolge festlegen und Senden von Nachrichten bei Bedarf.
    
- Benachrichtigung zu behandeln.
    
- Behandeln von Formularen.
    
- Behandeln von Benutzerprofilen und Message-Dienste.
    
Mithilfe der Themen in diesem Abschnitt können Sie das Implementieren dieser grundlegenden Aufgaben und Features, die MAPI-Client eindeutige zuständig ist.
  

