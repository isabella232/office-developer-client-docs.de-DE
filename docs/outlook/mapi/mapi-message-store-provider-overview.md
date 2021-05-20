---
title: Übersicht über den MAPI-Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d4ef074523cd654c3db2d686494d9a4f864e7cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429313"
---
# <a name="mapi-message-store-provider-overview"></a>Übersicht über den MAPI-Nachrichtenspeicheranbieter
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter verarbeiten das Speichern und Abrufen von Nachrichten und anderen Informationen für die Benutzer von Clientanwendungen. Die Nachrichteninformationen werden mithilfe eines hierarchischen Systems organisiert, das als Nachrichtenspeicher bezeichnet wird. Der Nachrichtenspeicher ist auf mehreren Ebenen implementiert, mit Containern, die als Ordner bezeichnet werden und Nachrichten unterschiedlicher Typen enthalten. Die Anzahl der Ebenen in einem Nachrichtenspeicher ist nicht begrenzt. Ordner können viele Unterordner enthalten. 
  
Die folgende Abbildung zeigt die hierarchische Nachrichtenspeicherarchitektur.
  
**Architektur des Nachrichtenspeichers**
  
![Architektur des Nachrichtenspeichers](media/amapi_03.gif "Nachrichtenspeicherarchitektur")
  
Die Abbildung zeigt zwei Ordner, einen mit einem Unterordner. Clientanwendungsbenutzer können auf eine Zusammenfassungsansicht der nachrichten zugreifen, die in den einzelnen Ordnern enthalten sind, oder sie einzeln mit einem Formular anzeigen. Ob der Client ein von MAPI zur Verfügung stelltes Standardformular oder ein benutzerdefiniertes Formular anzeigt, das von einem Formularentwickler zur Verfügung stellt, hängt vom Typ oder der Klasse der Nachricht ab. Der erste Ordner enthält Notiznachrichten und verwendet das MAPI-Standardnotizformular. Der zweite Ordner enthält Bestandsanforderungsnachrichten und verwendet ein benutzerdefiniertes Bestandsformular. Die Informationen in beiden Formularen stellen die Eigenschaften der Nachricht dar.
  
Sie können Nachrichtenspeicherdaten auf unterschiedliche Weise verwenden. Zusätzlich zur Verwendung von Daten für herkömmliche elektronische E-Mails können Sie Ordner als Forum für öffentliche Diskussionen, als Repository für Referenzdokumente oder als Container für Voicemail, Kalender, Kontakte oder Aufgaben verwenden. Ein einzelner Nachrichtenspeicher kann viele Arten von Informationen enthalten. Mehrere Clients können denselben Nachrichtenspeicher installieren. Dies macht die Freigabe von Daten einfach und schnell. 
  
Mit Nachrichtenspeicherordnern können Sie Nachrichten sortieren und filtern und die Nachrichtenanzeige auf einer Benutzeroberfläche anpassen. Links zu gefilterten Nachrichten werden in speziellen Ordnern gespeichert, die als Suchergebnisordner bezeichnet werden. Der Benutzer einer Clientanwendung gibt Filterkriterien ein, die MAPI als Einschränkung bezeichnet, und die Kriterien werden auf die Nachrichten angewendet, die in einem oder mehreren Ordnern gespeichert sind. Beispielsweise kann ein Benutzer nur nachrichten anzeigen möchten, die sich mit einem bestimmten Betreff befassen und über aktuellere Ankunftsdaten als letzte Woche verfügen. Verweise auf nachrichten, die den Kriterien entsprechen, werden im Suchordner aufgeführt, und die tatsächlichen Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten sind die Dateneinheiten, die von einem Benutzer oder einer Anwendung an einen anderen Benutzer oder eine andere Anwendung übertragen werden. Jede Nachricht enthält einige Nachrichtentexte mit einfacher oder komplexer Formatierung sowie Nachrichtenumschlaginformationen, die für die Übertragung verwendet werden. Einige Nachrichten enthalten eine oder mehrere Anlagen oder zusätzliche Daten im Zusammenhang mit einer Nachricht in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts. 
  
Je nach Anbieter des Nachrichtenspeichers kann ein Benutzer zusätzlich zu den gesendeten oder empfangenen Nachrichten eine neue Nachricht speichern, die gerade geschrieben wird. Nachrichten können von einem Ordner in einen anderen kopiert oder verschoben werden, und jede Kopie wird zu einer separaten Nachricht, die einzeln kopiert, gelöscht oder geändert werden kann. Ein weiteres Feature, das einige Nachrichtenspeicheranbieter aktivieren, ist die Möglichkeit, eine Nachricht nach dem Empfangen zu ändern und sie wieder in ihrem Ordner zu speichern. Ein Benutzer nutzt dieses Feature möglicherweise zum Drehen einer Faxnachricht, die auf den Kopf gestellt wurde. Der Benutzer kann die richtige Ansicht für die spätere Anzeige im Ordner speichern. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

