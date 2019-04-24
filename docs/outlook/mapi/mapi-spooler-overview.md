---
title: MAPI-Spooler-Übersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309580"
---
# <a name="mapi-spooler-overview"></a>MAPI-Spooler-Übersicht
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Spooler ist eine Funktion des Microsoft Office Outlook-Prozesses, der für das Senden von Nachrichten an und das Empfangen von e-Mails von einem Messagingsystem zuständig ist. MAPI-Spooler spielt eine wichtige Rolle bei Nachrichtenempfang und-Zustellung. Wenn ein Messagingsystem nicht verfügbar ist, werden die Nachrichten von der MAPI-Warteschlange gespeichert und zu einem späteren Zeitpunkt automatisch weitergeleitet. Diese Fähigkeit, Daten bei Bedarf beizubehalten oder zu senden, wird als "Store" und "Forward" bezeichnet, eine wichtige Funktion in Umgebungen, in denen Remoteverbindungen gängig sind und der Netzwerkdatenverkehr hoch ist. MAPI-Spooler wird als Hintergrundthread in Outlook ausgeführt.
  
MAPI-Spooler hat zusätzliche Aufgaben im Zusammenhang mit der Nachrichtenverteilung. Zu diesen zusätzlichen Aufgaben gehört Folgendes:
  
- Nachverfolgen der Empfängertypen, die von bestimmten Transportanbietern verarbeitet werden.
    
- Informieren einer Clientanwendung, wenn eine neue Nachricht zugestellt wurde.
    
- Aufrufen der Nachrichten Vorverarbeitung und nach Verarbeitung.
    
- Generieren von Berichten, die darauf hindeuten, dass die Nachrichtenübermittlung stattgefunden hat.
    
- Verwalten des Status von verarbeiteten Empfängern.
    
Die folgende Abbildung zeigt auf einer hohen Ebene, wie eine Nachricht von einem Client zum Messagingsystem fließt.
  
**Flussdiagramm für ausgehende Nachrichten**
  
![Ablauf der ausgehenden Nachrichten] (media/amapi_46.gif "Ablauf der ausgehenden Nachrichten")
  
Der Benutzer einer Clientanwendung sendet eine Nachricht an einen oder mehrere Empfänger. Der Nachrichtenspeicher Anbieter initiiert den Sendevorgang und formatiert die Nachricht mit zusätzlichen Informationen, die für die Übertragung benötigt werden.
  
MAPI-Spooler empfängt die zu verarbeitende Nachricht, wenn eine der folgenden Bedingungen eintritt:
  
- Der Nachrichtenspeicher Anbieter ist nicht eng mit einem Transportanbieter gekoppelt.
    
- Die Nachricht erfordert die Vorverarbeitung.
    
- Der Nachrichtenspeicher und der Transportanbieter sind eng gekoppelt, können jedoch nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.
    
Wenn die Nachricht vom MAPI-Spooler empfangen wird, wird die erforderliche Vorverarbeitung ausgeführt und die Nachricht an den entsprechenden Transportanbieter übermittelt. Der Transportanbieter übergibt die Nachricht an das Messagingsystem, das Sie an den beabsichtigten Empfänger sendet.
  
Bei eingehenden Nachrichten wird der Fluss umgekehrt. Der Transportanbieter empfängt eine Nachricht von seinem Messagingsystem und benachrichtigt MAPI-Spooler. Spooler führt alle erforderlichen Nachbearbeitung aus und informiert den Nachrichtenspeicher Anbieter darüber, dass eine neue Nachricht eingegangen ist. Diese Benachrichtigung veranlasst den Client, seine Nachrichtenanzeige zu aktualisieren, sodass der Benutzer die neue Nachricht lesen kann.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

