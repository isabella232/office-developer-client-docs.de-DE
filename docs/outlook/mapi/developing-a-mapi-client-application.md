---
title: Entwickeln einer MAPI-Client Anwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410035"
---
# <a name="developing-a-mapi-client-application"></a>Entwickeln einer MAPI-Client Anwendung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Clientanwendungen werden mit der objektorientierten MAPI-Clientschnittstelle geschrieben. MAPI-Clients interagieren mit einem oder mehreren Messagingsystemen über das MAPI-Subsystem und die MAPI-kompatiblen Dienstanbieter. Diese Interaktion kann auf viele verschiedene Arten erfolgen. Es gibt eine enorme Vielfalt in Clientanwendungen. Bei den meisten Clients handelt es sich um Messagingclients, die entweder Messaging in den festgelegten Featuresatz integrieren oder Messaging als primäres Feature ausführen. Zu den weiteren Features, die MAPI-Clients bieten können, gehören die Profilverwaltung oder das Adressbuch-und Nachrichtenspeicher Management.
  
Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten eine **Sitzung** mit dem MAPI-Subsystem. Weitere Informationen finden Sie unter [zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md). Nachdem eine Sitzung eingerichtet wurde, kann ein Client:
  
- Behandeln Sie ausgehende Nachrichten, einschließlich Antworten, weitergeleiteten Nachrichten und erneuten Übertragungen.
    
- Behandeln eingehender Nachrichten.
    
- Behandeln Sie den Nachrichtenspeicher, indem Sie Ordner und Nachrichten öffnen, Nachrichten erstellen, ändern, kopieren und senden, Unterhaltungen nachverfolgen und einen oder mehrere Ordner durchsuchen.
    
- Behandeln des Adressbuchs durch Erstellen und Ändern von Empfängern, Suchen von Einträgen und durchlaufen der Containerhierarchie.
    
- Behandeln eines Transportanbieters durch Ausführen einer Neukonfiguration, Festlegen von Optionen und Transport Reihenfolge und Senden von Nachrichten bei Bedarf.
    
- Ereignisbenachrichtigung behandeln.
    
- Behandeln von Formularen
    
- Behandeln von Profilen und Nachrichtendiensten
    
Verwenden Sie die Themen in diesem Abschnitt, um Sie bei der Implementierung dieser grundlegenden Aufgaben und der spezifischen Features zu unterstützen, mit denen Ihr MAPI-Client eindeutig wird.
  

