---
title: MAPI-Warteschlange (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e4bd4f6038db3dbb33ec3511d953448fea7a6c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793091"
---
# <a name="mapi-spooler-overview"></a>MAPI-Warteschlange (Übersicht)
  
**Betrifft**: Outlook 
  
MAPI-Warteschlange ergibt sich aus der Microsoft Office Outlook-Prozess, der für das Senden von Nachrichten an und Empfangen von Nachrichten aus einem messaging-System verantwortlich ist. MAPI-Warteschlange spielt eine wichtige Rolle in der Nachricht und die Zustellung. Bei einem messaging-System nicht verfügbar ist, MAPI-Warteschlange werden die Nachrichten gespeichert und automatisch zu einem späteren Zeitpunkt weiterleitet. Die Möglichkeit, halten Sie sich oder Senden von Daten bei Bedarf wird als speichern und weiterleiten, ein wichtiges Feature in Umgebungen, in denen Remoteverbindungen sind häufige und Netzwerkdatenverkehr ist hoch, bezeichnet. MAPI-Warteschlange in Outlook als Hintergrundthread ausgeführt wird.
  
MAPI-Warteschlange verfügt über zusätzliche Aufgaben im Zusammenhang mit der Verteilung von Nachrichten. Diese zusätzlichen Aufgaben umfassen Folgendes:
  
- Verfolgen von die Empfängertypen, die vom Anbieter von spezifischen Transport verarbeitet werden.
    
- Eine Clientanwendung informiert, wenn eine neue Nachricht übermittelt wurde.
    
- Nachricht der vorverarbeitung und Traditionsgemäß aufrufen.
    
- Generieren von Berichten, die angeben, Nachrichtenübermittlung ist aufgetreten.
    
- Verwalten von Status auf verarbeiteten Empfänger.
    
Die folgende Abbildung zeigt auf allgemeiner Ebene, wie eine Nachricht von einem Client an die messaging-System fließt.
  
**Flussdiagramm für ausgehende Nachrichten**
  
![Ausgehende Nachrichtenfluss] (media/amapi_46.gif "Ausgehende Nachrichtenfluss")
  
Der Benutzer von einer Clientanwendung sendet eine Nachricht an einen oder mehrere Empfänger an. Die Nachricht speichern Anbieter initiiert im Sendevorgang Formatierung der Nachricht mit zusätzlichen Informationen für die Übertragung benötigt.
  
MAPI-Warteschlange empfängt die Meldung verarbeiten, wenn einer der folgenden Situationen auftreten:
  
- Der Nachricht Speicheranbieter ist nicht eng mit eines Transportdienstes verknüpft.
    
- Die Nachricht muss der vorverarbeitung.
    
- Die Nachrichtenspeicher und Transport Anbieter eng verknüpft sind, aber sie können nicht alle Empfänger, an die Nachricht adressiert ist, behandeln.
    
Wenn MAPI-Warteschlange die Nachricht empfängt, führt der erforderlichen vorverarbeitung und übermittelt die Nachricht an den entsprechenden Adressbuchhierarchie. Der Adressbuchhierarchie bietet die Nachricht an die messaging-System, an den Empfänger sendet.
  
Mit eingehenden Nachrichten wird der Ablauf umgekehrt. Der Transportdienst empfängt eine Nachricht von messaging-System und MAPI-Warteschlange benachrichtigt. Warteschlange führt alle erforderlichen Nachbearbeitung und dem Speicheranbieter Nachricht informiert werden, dass eine neue Nachricht empfangen hat. Diese Benachrichtigung wird vom Client zum Aktualisieren der Nachricht-Display, dem der Benutzer die neue Nachricht lesen.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und die Architektur](mapi-features-and-architecture.md)

