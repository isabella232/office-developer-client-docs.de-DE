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
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410035"
---
# <a name="developing-a-mapi-client-application"></a>Entwickeln einer MAPI-Clientanwendung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Clientanwendungen werden mit der objektorientierten MAPI-Clientschnittstelle geschrieben. MAPI-Clients interagieren mit einem oder mehreren Messagingsystemen über das MAPI-Subsystem und MAPI-kompatible Dienstanbieter. Diese Interaktion kann auf unterschiedliche Weise erfolgen. Es gibt eine enorme Vielfalt an Clientanwendungen. Bei den meisten Clients handelt es sich um Messagingclients, die Messaging entweder in ihren etablierten Featuresatz integrieren oder Messaging als primäres Feature ausführen. Zu den weiteren Features, die MAPI-Clients bereitstellen können, gehören die Profilverwaltung oder die Adressbuch- und Nachrichtenspeicherverwaltung.
  
Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten **eine** Sitzung mit dem MAPI-Subsystem. Weitere Informationen finden Sie unter [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md). Nachdem eine Sitzung eingerichtet wurde, kann ein Client:
  
- Behandeln sie ausgehende Nachrichten, einschließlich Antworten, weitergeleitete Nachrichten und erneute Übertragungen.
    
- Behandeln eingehender Nachrichten.
    
- Behandeln Sie den Nachrichtenspeicher, indem Sie Ordner und Nachrichten öffnen, Nachrichten erstellen, ändern, kopieren und senden, Unterhaltungen nachverfolgen und einen oder mehrere Ordner durchsuchen.
    
- Behandeln Sie das Adressbuch, indem Sie Empfänger erstellen und ändern, Einträge suchen und die Containerhierarchie durchlaufen.
    
- Behandeln Sie einen Transportanbieter, indem Sie eine Neukonfiguration durchführen, Optionen und Transportreihenfolge festlegen und Nachrichten bei Bedarf senden.
    
- Behandeln der Ereignisbenachrichtigung.
    
- Behandeln von Formularen
    
- Behandeln von Profilen und Nachrichtendiensten.
    
Verwenden Sie die Themen in diesem Abschnitt, um Ihnen bei der Implementierung dieser grundlegenden Aufgaben und der spezifischen Features zu helfen, die Ihren MAPI-Client eindeutig machen.
  

