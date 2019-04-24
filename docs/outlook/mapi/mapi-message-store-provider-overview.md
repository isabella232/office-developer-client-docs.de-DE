---
title: Übersicht über den MAPI-Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d4ef074523cd654c3db2d686494d9a4f864e7cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345875"
---
# <a name="mapi-message-store-provider-overview"></a>Übersicht über den MAPI-Nachrichtenspeicher Anbieter
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicher Anbieter behandeln das Speichern und Abrufen von Nachrichten und anderen Informationen für die Benutzer von Clientanwendungen. Die Nachrichten Informationen werden mithilfe eines hierarchischen Systems organisiert, das als Nachrichtenspeicher bezeichnet wird. Der Nachrichtenspeicher wird auf mehreren Ebenen implementiert, wobei Container als Ordner mit Nachrichten unterschiedlicher Typen bezeichnet werden. Es gibt keine Begrenzung für die Anzahl der Ebenen in einem Nachrichtenspeicher; Ordner können viele Unterordner enthalten. 
  
Die folgende Abbildung zeigt die hierarchische Nachrichtenspeicher Architektur.
  
**Architektur des Nachrichtenspeichers**
  
![Nachrichtenspeicher Architektur] (media/amapi_03.gif "Nachrichtenspeicher Architektur")
  
Die Abbildung zeigt zwei Ordner, eine mit einem Unterordner. Client Anwendungsbenutzer können auf eine Zusammenfassungsansicht der Nachrichten in den einzelnen Ordnern zugreifen oder diese einzeln mit einem Formular anzeigen. Ob der Client ein Standardformular anzeigt, das von MAPI bereitgestellt wird, oder ein benutzerdefiniertes Formular, das ein Entwickler bereitstellt, hängt vom Typ oder der Klasse der Nachricht ab. Der erste Ordner enthält Notiz Nachrichten und verwendet das MAPI-Standard Noten Formular. Der zweite Ordner enthält Inventar Anforderungsnachrichten und verwendet ein benutzerdefiniertes Inventar Formular. Die Informationen in beiden Formularen sind die Eigenschaften der Nachricht.
  
Sie können Nachrichtenspeicher Daten auf verschiedene Arten verwenden. Neben der Verwendung von Daten für herkömmliche elektronische e-Mails können Sie Ordner auch als Forum für öffentliche Diskussionen, als Repository für Referenzdokumente oder als Container für Voicemail, Kalender, Kontakte oder Aufgaben verwenden. Ein einzelner Nachrichtenspeicher kann viele Arten von Informationen enthalten. Mehrere Clients können denselben Nachrichtenspeicher installieren. Dadurch wird die Freigabe von Daten einfach und schnell. 
  
Mit Nachrichtenspeicher Ordnern können Sie Nachrichten sortieren und Filtern und die Nachrichtenanzeige auf einer Benutzeroberfläche anpassen. Links zu gefilterten Nachrichten werden in speziellen Ordnern mit dem Namen Suchergebnisordner gespeichert. Der Benutzer einer Clientanwendung gibt Filterkriterien ein, auf die MAPI als Einschränkung verweist, und die Kriterien werden auf die Nachrichten angewendet, die in einem oder mehreren Ordnern gespeichert sind. Beispielsweise kann ein Benutzer nur die Nachrichten anzeigen, die mit einem bestimmten Betreff befassen und über die aktuelle Ankunftszeit verfügen. Verweise auf die Nachrichten, die den Kriterien entsprechen, werden im Suchordner aufgeführt, und die tatsächlichen Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten sind die Dateneinheiten, die von einem Benutzer oder einer Anwendung an einen anderen Benutzer oder eine andere Anwendung übertragen werden. Jede Nachricht enthält einen Text mit einfacher oder komplexer Formatierung und Nachrichtenumschlag Informationen, die für die Übertragung verwendet werden. Einige Nachrichten verfügen über eine oder mehrere Anhänge oder zusätzliche Daten im Zusammenhang mit einer Nachricht in Form einer Datei, einer anderen Nachricht oder einem OLE-Objekt. 
  
Je nach Nachrichtenspeicher Anbieter kann ein Benutzer zusätzlich zu gesendeten oder empfangenen Nachrichten eine neue Nachricht speichern. Nachrichten können kopiert oder von einem Ordner in einen anderen verschoben werden, wobei jede Kopie eine separate Nachricht wird, die einzeln kopiert, gelöscht oder geändert werden kann. Ein weiteres Feature, das einige Nachrichtenspeicher Anbieter aktivieren, ist die Möglichkeit, eine Nachricht zu ändern, nachdem Sie empfangen wurde, und Sie wieder im Ordner zu speichern. Ein Benutzer kann diese Funktion nutzen, um eine auf dem Kopf stehende Faxnachricht zu drehen. Der Benutzer kann die richtige Ansicht im Ordner zur späteren Anzeige speichern. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

