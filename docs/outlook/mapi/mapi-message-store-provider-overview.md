---
title: MAPI-Nachricht Speicher-Anbieter (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5cc8261dfee6803492ffcf62c182930e2ac6d425
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793029"
---
# <a name="mapi-message-store-provider-overview"></a>MAPI-Nachricht Speicher-Anbieter (Übersicht)
  
**Betrifft**: Outlook 
  
Nachricht Anbieter behandeln die Speicherung und den Abruf von Nachrichten und andere Informationen für die Benutzer der Clientanwendungen. Informationen der Nachricht ist mit einer hierarchischen System bekannt als Nachrichtenspeicher organisiert. Nachrichtenspeicher wird in mehreren Ebenen mit namens aufbewahren von Nachrichten mit unterschiedlichen Typen Folders Container implementiert. Es gibt keine Beschränkung der Anzahl der Ebenen in einem Nachrichtenspeicher. Ordner können viele Unterordner enthalten. 
  
Die folgende Abbildung zeigt die Architektur des Nachrichtenspeichers hierarchische.
  
**Architektur des Nachrichtenspeichers**
  
![Architektur des Nachrichtenspeichers] (media/amapi_03.gif "Architektur des Nachrichtenspeichers")
  
Die Abbildung zeigt zwei Ordnern mit einem Unterordner. Client-Anwendungsbenutzer können Zugriff auf eine Zusammenfassungsansicht der Nachrichten, die in jedem Ordner enthalten sind oder einzeln mit einem Formular anzeigen. Ob der Client angezeigt werden, einem Standardformular simulieren, das MAPI bereitstellt oder ein benutzerdefiniertes Formular, das ein Formularentwickler bereitstellt, hängt von den Typ oder der Nachricht-Klasse. Der erste Ordner enthält Hinweis Nachrichten und das MAPI-standard Hinweis Formular verwendet. Der zweite Ordner enthält Inventar Anforderungsnachrichten und einem benutzerdefinierten Inventar Formular verwendet. Die Informationen für beide Formulare stellt die Eigenschaften der Nachricht.
  
Sie können die Nachricht Speicherung von Daten in verschiedene Arten verwenden. Zusätzlich zur Verwendung von Daten für traditionelle e-Mail-Nachrichten, können Sie Ordner als Forum für Öffentliche Diskussion, als Repository für Referenzdokumenten oder als Container für Voicemail, Kalender, Kontakte oder Aufgaben, beispielsweise verwenden. Ein einzelne Nachrichtenspeicher kann viele Arten von Informationen enthalten. Mehrere Clients können den gleichen Nachrichtenspeicher installieren. Dadurch wird die Freigabe von Daten schnell und einfach. 
  
Store Nachrichtenordner aktivieren Sie zum Sortieren und Filtern Nachrichten und zum Anpassen der Anzeige der Nachricht in einer Benutzeroberfläche. Links zu gefilterten Nachrichten werden in Spezialordnern aufgerufen Suchergebnisse Ordner gespeichert. Der Benutzer von einer Clientanwendung gibt Filterkriterien, die MAPI bezieht sich auf als eine Einschränkung, und die Kriterien auf die Nachrichten in einen oder mehrere Ordner angewendet wird. Angenommen, möchten ein Benutzer nur Nachrichten angezeigt, die mit einem bestimmten Thema befassen und hinzukommen Datumsangaben, die aktueller ist als die letzte Woche sind vorhanden. Verweise auf die Nachrichten, die den Kriterien im Suchordner aufgeführt sind, und die echten Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten werden die Daten, die von einem Benutzer oder eine Anwendung an einen anderen Benutzer oder eine Anwendung übertragen werden. Jede Nachricht enthält einige Nachrichtentext mit einfache oder komplexe Formatierung, und die Informationen im Nachrichtenumschlag, die für die Übertragung verwendet wird. Einige Nachrichten enthalten eine oder mehrere Anlagen oder zusätzliche Daten im Zusammenhang mit und transportiert mit einer Nachricht in Form einer Datei, eine andere Nachricht oder ein OLE-Objekt. 
  
Je nach der Nachricht Speicheranbieter, kann ein Benutzer eine neue Nachricht zurzeit außerdem für Nachrichten, die gesendet oder empfangen wurde geschrieben speichern. Nachrichten können kopiert oder verschoben aus einem Ordner in einen anderen mit jedem Exemplar sind somit eine separate Nachricht, die kopiert, gelöscht oder einzeln geändert werden kann. Ein weiteres Feature ist, dass einige Nachrichtenspeicher Anbieter aktivieren die Möglichkeit, eine Nachricht zu ändern, nachdem eingegangen ist und es wieder in dessen Ordner speichern. Ein Benutzer kann dieses Feature für eine Faxnachricht, die eingegangen Kopf drehen nutzen. Der Benutzer kann die richtige Ansicht im Ordner für die Anzeige von später speichern. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und die Architektur](mapi-features-and-architecture.md)

