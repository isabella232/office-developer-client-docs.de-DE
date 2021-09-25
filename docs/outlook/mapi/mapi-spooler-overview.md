---
title: MAPI-Spooler-Übersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f92d7a579c2ccd8c945cdbb820bd97b66d6fa2c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592123"
---
# <a name="mapi-spooler-overview"></a>MAPI-Spooler-Übersicht
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Spooler ist eine Funktion des Microsoft Office Outlook Prozesses, der für das Senden von Nachrichten an und empfangen von Nachrichten von einem Messagingsystem verantwortlich ist. DER MAPI-Spooler spielt eine wichtige Rolle bei der Nachrichtenbestätigung und -zustellung. Wenn ein Messagingsystem nicht verfügbar ist, speichert der MAPI-Spooler die Nachrichten und leitet sie zu einem späteren Zeitpunkt automatisch weiter. Diese Möglichkeit, Daten bei Bedarf zu speichern oder zu senden, wird als "Speichern und Weiterleiten" bezeichnet, ein wichtiges Feature in Umgebungen, in denen Remoteverbindungen häufig sind und der Netzwerkdatenverkehr hoch ist. MAPI-Spooler wird als Hintergrundthread innerhalb Outlook ausgeführt.
  
Der MAPI-Spooler hat zusätzliche Zuständigkeiten im Zusammenhang mit der Nachrichtenverteilung. Diese zusätzlichen Aufgaben umfassen Folgendes:
  
- Nachverfolgen der Empfängertypen, die von bestimmten Transportanbietern verarbeitet werden.
    
- Informieren einer Clientanwendung, wenn eine neue Nachricht zugestellt wurde.
    
- Aufrufen der Vor- und Nachverarbeitung von Nachrichten.
    
- Generieren von Berichten, die angeben, dass die Nachrichtenübermittlung erfolgt ist.
    
- Verwalten des Status für verarbeitete Empfänger.
    
Die folgende Abbildung zeigt auf hoher Ebene, wie eine Nachricht von einem Client zum Messagingsystem fließt.
  
**Flussdiagramm für ausgehende Nachrichten**
  
![Flussdiagramm für ausgehende Nachrichten](media/amapi_46.gif "Flussdiagramm für ausgehende Nachrichten")
  
Der Benutzer einer Clientanwendung sendet eine Nachricht an einen oder mehrere Empfänger. Der Nachrichtenspeicheranbieter initiiert den Sendevorgang und formatiert die Nachricht mit zusätzlichen Informationen, die für die Übertragung erforderlich sind.
  
Der MAPI-Spooler empfängt die zu verarbeitende Nachricht, wenn eine der folgenden Bedingungen auftritt:
  
- Der Nachrichtenspeicheranbieter ist nicht eng mit einem Transportanbieter verbunden.
    
- Die Nachricht muss vorverarbeitet werden.
    
- Der Nachrichtenspeicher und der Transportanbieter sind eng miteinander verbunden, können jedoch nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.
    
Wenn der MAPI-Spooler die Nachricht empfängt, führt er alle erforderlichen Vorverarbeitungen durch und übermittelt die Nachricht an den entsprechenden Transportanbieter. Der Transportanbieter gibt die Nachricht an sein Messagingsystem weiter, das sie an den gewünschten Empfänger sendet.
  
Bei eingehenden Nachrichten wird der Fluss umgekehrt. Der Transportanbieter empfängt eine Nachricht von seinem Messagingsystem und benachrichtigt den MAPI-Spooler. Spooler führt alle erforderlichen Nachverarbeitungen durch und informiert den Nachrichtenspeicheranbieter darüber, dass eine neue Nachricht eingetroffen ist. Diese Benachrichtigung bewirkt, dass der Client seine Nachrichtenanzeige aktualisiert, sodass der Benutzer die neue Nachricht lesen kann.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

