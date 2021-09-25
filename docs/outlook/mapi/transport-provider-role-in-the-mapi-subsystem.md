---
title: Transportanbieterrolle im MAPI-Subsystem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0cfc1fd71e70fbc3555e63551cb3e48c708b98bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609278"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Transportanbieterrolle im MAPI-Subsystem
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transport provider dynamic-link libraries (DLLs) provide the interface between the MAPI spooler and the part of a messaging system responsible for message sending and receiving. Der MAPI-Spooler und der Transportanbieter arbeiten zusammen, um die Verantwortlichkeiten für das Senden einer Nachricht oder das Empfangen einer Nachricht zu übernehmen. Der MAPI-Spooler lädt die Transportanbieter-DLL bei der ersten Verwendung und gibt sie frei, wenn sie nicht mehr benötigt wird. Auf demselben System können mehrere Transportanbieter installiert werden, die MAPI stellt jedoch den erforderlichen Spooler bereit.
  
Clientanwendungen kommunizieren in der Regel nicht direkt mit dem Transportanbieter. Clients senden stattdessen Nachrichten über einen Speicheranbieter, und der MAPI-Spooler sendet ausgehende Nachrichten an den entsprechenden Transportanbieter und übermittelt eingehende Nachrichten an den entsprechenden Nachrichtenspeicher. Der MAPI-Spooler führt seine Arbeit aus und ruft Transportanbieter auf, wenn sich Vordergrundanwendungen im Leerlauf befinden. Nach dem optionalen Anzeigen von Dialogfeldern, wenn der Transportanbieter zum ersten Mal angemeldet ist, arbeiten Transportanbieter im Hintergrund, es sei denn, sie werden vom Client aufgerufen, um Sende- und Empfangswarteschlangen zu leeren. 
  
Transportanbieter haben die folgenden Zuständigkeiten in einem MAPI-Messagingsystem:
  
- Registrieren Sie die Adresstypen, die sie für den MAPI-Spooler akzeptieren können, damit der MAPI-Spooler Nachrichten je nach Zieladresse der Nachrichten an den entsprechenden Transportanbieter senden kann. Ein Transportanbieter kann mehrere Adresstypen registrieren. Transportanbieter können auch bestimmte Empfängeradressen beim MAPI-Spooler registrieren. Nachrichten, die an eine dieser Adressen adressiert sind, werden an den Transportanbieter gesendet, der die Adresse beim MAPI-Spooler registriert hat. Weitere Informationen finden Sie unter [Transport provider and MAPI Spooler Operational Model.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Übermitteln eingehender Nachrichten an den MAPI-Spooler. Je nach Art des Messagingsystems kann ein Transportanbieter den MAPI-Spooler entweder direkt benachrichtigen, wenn eine neue Nachricht eintrifft, oder er kann anfordern, dass der MAPI-Spooler den Transportanbieter regelmäßig abruft, um nach neuen Nachrichten zu suchen.
    
- Konvertieren von MAPI-Nachrichteneigenschaften in und von systemeigenen Nachrichteneigenschaften in das Messagingsystem. Beispielsweise muss der Transportanbieter möglicherweise die Adressen des Absenders und des Empfängers in einer ausgehenden Nachricht in ein Formular konvertieren, das für das Messagingsystem akzeptabel ist. Einige Messagingsysteme unterstützen nicht alle MAPI-Nachrichteneigenschaften. Weitere Informationen zum Beibehalten von MAPI-Nachrichteneigenschaften beim Übermitteln von Nachrichten an ein Messagingsystem finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
    
- Registrieren Sie nachrichten- und empfängerspezifische Optionen für den Transportanbieter.
    
- Führen Sie alle vom Messagingsystem erforderlichen Überprüfungen der Anmeldeinformationen durch.
    
- Zugreifen auf ausgehende Nachrichten mithilfe des Nachrichtenobjekts, das vom MAPI-Spooler an sie übergeben wird.
    
- Übersetzen Sie das Nachrichtenformat nach Bedarf des zugrunde liegenden Messagingsystems.
    
- Benachrichtigen Sie den MAPI-Spooler, welche Empfänger einer ausgehenden Nachricht der Transportanbieter für die Verarbeitung zuständig ist, indem Sie die Eigenschaft **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) für diese Empfänger festlegen.
    
- Informieren Sie den MAPI-Spooler, wenn eine eingehende Nachricht verarbeitet werden muss.
    
- Übergeben Sie eingehende Nachrichtendaten mithilfe von Nachrichtenobjekten an den MAPI-Spooler.
    
- Weisen Sie allen erforderlichen MAPI-Nachrichteneigenschaften für eingehende Nachrichten Werte zu.
    
- Löschen Sie die Nachricht aus dem zugrunde liegenden Messagingsystem nach der Zustellung, falls erforderlich.
    
- Bereitstellen von Statusinformationen für die MAPI-Spooler- und Clientanwendungen.
    
Die folgende Abbildung zeigt die Rolle eines Transportanbieters im Hinblick auf die anderen Komponenten der MAPI-Architektur.
  
**Transportanbieterrolle in einem Messaging-System**
  
![Transportanbieterrolle in einem Messaging-System](media/xp01.gif "Transportanbieterrolle in einem Messaging-System")
  

