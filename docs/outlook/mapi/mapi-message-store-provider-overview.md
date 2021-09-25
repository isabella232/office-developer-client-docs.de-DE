---
title: Übersicht über den MAPI-Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dce839bdeb067abb3702919faad9782a53ebde18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556168"
---
# <a name="mapi-message-store-provider-overview"></a>Übersicht über den MAPI-Nachrichtenspeicheranbieter
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter verarbeiten das Speichern und Abrufen von Nachrichten und anderen Informationen für die Benutzer von Clientanwendungen. Die Nachrichteninformationen werden mithilfe eines hierarchischen Systems organisiert, das als Nachrichtenspeicher bezeichnet wird. Der Nachrichtenspeicher wird auf mehreren Ebenen implementiert, wobei Container als Ordner bezeichnet werden, die Nachrichten unterschiedlicher Typen enthalten. Es gibt keine Beschränkung für die Anzahl der Ebenen in einem Nachrichtenspeicher. Ordner können viele Unterordner enthalten. 
  
Die folgende Abbildung zeigt die hierarchische Architektur des Nachrichtenspeichers.
  
**Architektur des Nachrichtenspeichers**
  
![Architektur des Nachrichtenspeichers](media/amapi_03.gif "Architektur des Nachrichtenspeichers")
  
Die Abbildung zeigt zwei Ordner, einen mit einem Unterordner. Clientanwendungsbenutzer können auf eine Zusammenfassungsansicht der in den einzelnen Ordnern enthaltenen Nachrichten zugreifen oder sie einzeln mit einem Formular anzeigen. Ob der Client ein standardformular anzeigt, das MAPI bereitstellt, oder ein benutzerdefiniertes Formular, das ein Formularentwickler bereitstellt, hängt vom Typ oder der Klasse der Nachricht ab. Der erste Ordner enthält Notizmeldungen und verwendet das MAPI-Standardnotizformular. Der zweite Ordner enthält Bestandsanforderungsnachrichten und verwendet ein benutzerdefiniertes Bestandsformular. Die Informationen in beiden Formularen stellen die Eigenschaften der Nachricht dar.
  
Sie können Nachrichtenspeicherdaten auf verschiedene Arten verwenden. Zusätzlich zur Verwendung von Daten für herkömmliche E-Mails können Sie Ordner als Forum für öffentliche Diskussionen, als Repository für Referenzdokumente oder als Container für Voicemail, Kalender, Kontakte oder Aufgaben verwenden, z. B. Ein einzelner Nachrichtenspeicher kann viele Arten von Informationen enthalten. Mehrere Clients können denselben Nachrichtenspeicher installieren. Dadurch wird die Freigabe von Daten einfach und schnell. 
  
Mit Nachrichtenspeicherordnern können Sie Nachrichten sortieren und filtern und die Meldungsanzeige auf einer Benutzeroberfläche anpassen. Links zu gefilterten Nachrichten werden in speziellen Ordnern gespeichert, die als Suchergebnisordner bezeichnet werden. Der Benutzer einer Clientanwendung gibt Filterkriterien ein, die mapi als Einschränkung bezeichnet, und die Kriterien werden auf die in einem oder mehreren Ordnern gespeicherten Nachrichten angewendet. Ein Benutzer möchte z. B. nur die Nachrichten anzeigen, die sich auf einen bestimmten Betreff beziehen und über Eintreffen von Datumsangaben verfügen, die aktueller als letzte Woche sind. Verweise auf die Nachrichten, die den Kriterien entsprechen, werden im Suchordner aufgelistet, und die tatsächlichen Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten sind die Dateneinheiten, die von einem Benutzer oder einer Anwendung an einen anderen Benutzer oder eine andere Anwendung übertragen werden. Jede Nachricht enthält Nachrichtentext mit einfacher oder komplexer Formatierung und Nachrichtenumschlaginformationen, die für die Übertragung verwendet werden. Einige Nachrichten enthalten eine oder mehrere Anlagen oder zusätzliche Daten, die sich auf eine Nachricht in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts beziehen und mit dieser übertragen werden. 
  
Abhängig vom Nachrichtenspeicheranbieter kann ein Benutzer zusätzlich zu den nachrichten, die gesendet oder empfangen wurden, eine neue Nachricht speichern, die gerade geschrieben wird. Nachrichten können von einem Ordner in einen anderen kopiert oder verschoben werden, wobei jede Kopie zu einer separaten Nachricht wird, die einzeln kopiert, gelöscht oder geändert werden kann. Ein weiteres Feature, das einige Nachrichtenspeicheranbieter aktivieren, ist die Möglichkeit, eine Nachricht zu ändern, nachdem sie empfangen wurde, und sie wieder in ihrem Ordner zu speichern. Ein Benutzer kann diese Funktion nutzen, um eine Faxnachricht zu drehen, die auf den Kopf gelangt ist. Der Benutzer kann die richtige Ansicht im Ordner für die spätere Anzeige speichern. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

