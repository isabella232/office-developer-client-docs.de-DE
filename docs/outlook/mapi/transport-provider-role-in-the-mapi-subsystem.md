---
title: Transportanbieterrolle des MAPI-Subsystems
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 263370590a35f19482cc5ad7e56c65f6df0087fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581300"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Transportanbieterrolle des MAPI-Subsystems
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Transport-Anbieter Dynamic Link Libraries (DLLs) stellen die Schnittstelle zwischen der MAPI-Warteschlange und das Webpart von einem verantwortlich für die Nachricht senden und Empfangen von messaging-System. Die MAPI-Warteschlange und der Adressbuchhierarchie arbeiten zusammen, um die Aufgaben der eine Nachricht senden oder Empfangen einer Nachricht zu verarbeiten. Die MAPI-Warteschlange wird der Adressbuchhierarchie DLL geladen, wenn es zuerst verwendet wird, und gibt es frei, wenn es nicht mehr benötigt wird. Mehrere Transportanbieter auf dem gleichen System installiert werden können, aber MAPI bereitstellt, die eine Warteschlange erforderlich.
  
Clientanwendungen kommunizieren in der Regel nicht direkt mit der Adressbuchhierarchie. Vielmehr Clients Übermitteln von Nachrichten über einen Anbieter anmelden und die MAPI-Warteschlange ausgehende Nachrichten an den entsprechenden Transport gesendet und eingehende Nachrichten mit dem entsprechenden Nachrichtenspeicher übermittelt. Die MAPI-Warteschlange führt diese Aufgaben und seine Aufrufe der Anbieter Transport, wenn Vordergrund Applikationen im Leerlauf befinden. Nachdem optional Dialogfelder anzeigen, wenn der Adressbuchhierarchie zuerst angemeldet, Betrieb Transportanbieter im Hintergrund, wenn vom Client zu leeren senden und Empfangen von Warteschlangen aufgerufen. 
  
Transportanbieter haben folgende Aufgaben in MAPI-messaging-System:
  
- Registrieren Sie die Adresstypen, den, die Sie annehmen können, die MAPI-Warteschlange, damit die MAPI-Warteschlange Nachrichten an die entsprechenden Adressbuchhierarchie je nach die Zieladresse der Nachrichten senden kann. Eine Adressbuchhierarchie kann mehrere Adresstyp registrieren. Transportanbieter können auch bestimmte Empfänger-Adressen mit der MAPI-Warteschlange registrieren. Nachrichten an eine dieser Adressen werden an der Adressbuchhierarchie gesendet werden, die die Adresse für die MAPI-Warteschlange registriert. Weitere Informationen finden Sie unter [Adressbuchhierarchie und MAPI-Warteschlange betriebliche Modell](transport-provider-and-mapi-spooler-operational-model.md).
    
- Übermitteln Sie eingehende Nachrichten an die Warteschlange MAPI. Abhängig von der Art der messaging-System kann ein Transportdienstes entweder direkt benachrichtigt werden, die MAPI-Warteschlange beim Eintreffen einer neuen Nachricht, oder es anfordern kann, dass die MAPI-Warteschlange der Adressbuchhierarchie in regelmäßigen Abständen zu prüfen, ob neue Nachrichten abzufragen.
    
- Konvertieren von MAPI-Eigenschaften zu und von Nachrichteneigenschaften einheitlich in Messagingsystem bereit. Beispielsweise möglicherweise der Adressbuchhierarchie des Senders und des Empfängers Adressen in ausgehenden Nachrichten in ein Format konvertiert, die an die messaging-System akzeptabel ist. Einige Messagingsysteme unterstützen nicht alle Eigenschaften MAPI-Nachricht. Weitere Informationen zum Beibehalten von MAPI-Nachrichteneigenschaften bei der Übermittlung von Nachrichten mit einem Messagingsystem finden Sie unter [Developing eines Transportdienstes TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
    
- Registrieren Sie Nachrichten- und Empfänger Optionen speziell für den Transportdienst.
    
- Führen Sie die Überprüfung von Anmeldeinformationen, die von der messaging-System erforderlich.
    
- Zugriff auf ausgehende Nachrichten mithilfe des Message-Objekts übergeben die MAPI-Warteschlange.
    
- Nachrichtenformat gemäß dem zugrunde liegenden messaging-System zu übersetzen.
    
- Benachrichtigen Sie der MAPI-Warteschlange der Empfänger von ausgehenden Nachrichten der Adressbuchhierarchie Verantwortung für die Behandlung durch Festlegen der **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft für diese Empfänger angenommen hat.
    
- Informieren Sie die MAPI-Warteschlange, wenn eine eingehende Nachricht behandelt werden muss.
    
- Übergeben Sie Daten der eingehenden Nachricht an die MAPI-Warteschlange mithilfe von Message-Objekten.
    
- Alle erforderlichen MAPI Nachrichteneigenschaften für eingehende Nachrichten Werte zuweisen.
    
- Löschen der Nachricht aus dem zugrunde liegenden messaging-System nach der Übermittlung, falls erforderlich.
    
- Bereitzustellen Sie Statusinformationen für den MAPI-Warteschlange und Clientanwendungen.
    
Die folgende Abbildung zeigt eine Adressbuchhierarchie Rolle in Bezug auf die anderen Komponenten der MAPI-Architektur.
  
**Transportanbieterrolle in einem Messaging-System**
  
![Transport-Anbieter-Rolle in einem messaging-system] (media/xp01.gif "Transport-Anbieter-Rolle in einem messaging-system")
  

