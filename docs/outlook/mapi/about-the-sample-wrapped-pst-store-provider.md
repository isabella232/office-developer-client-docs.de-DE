---
title: Informationen zum Beispiel umschlossenen STORE Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Letzte Änderung: 03. Juli 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432723"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Informationen zum Beispiel umschlossenen STORE Anbieter

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Übersicht über nachrichten Store Anbieter

Nachrichtenspeicheranbieter verarbeiten das Speichern und Abrufen von Nachrichten und anderen Informationen für die Benutzer von Clientanwendungen. Die Nachrichteninformationen werden mithilfe eines hierarchischen Systems organisiert, das als Nachrichtenspeicher bezeichnet wird. Der Nachrichtenspeicher ist auf mehreren Ebenen implementiert, mit Containern, die als Ordner bezeichnet werden und Nachrichten unterschiedlicher Typen enthalten. Die Anzahl der Ebenen in einem Nachrichtenspeicher ist nicht begrenzt. Ordner können viele Unterordner enthalten.
  
Nachrichtenspeicherdaten können auf unterschiedliche Weise verwendet werden. Zusätzlich zur typischen E-Mail-Verwendung können Ordner als Forum für öffentliche Diskussionen, als Repository für Referenzdokumente oder als Container für Bulletin Board-Informationen verwendet werden. Ein einzelner Nachrichtenspeicher kann viele Arten von Informationen enthalten, einige sind änderbar und andere nicht. Mehrere Clients können denselben Nachrichtenspeicher installieren, wodurch die Freigabe von Daten einfach und schnell ist.
  
Mit Nachrichtenspeicherordnern können Sie Nachrichten sortieren und filtern und die Ansicht in einer Benutzeroberflächenanzeige anpassen. Links zu gefilterten Nachrichten werden in speziellen Ordnern gespeichert, die als Suchergebnisordner bezeichnet werden. Der Benutzer einer Clientanwendung gibt Filterkriterien ein, die MAPI als Einschränkung bezeichnet, und die Kriterien werden auf die Nachrichten angewendet, die in einem oder mehreren Ordnern gespeichert sind. Ein Benutzer kann beispielsweise nur nachrichten anzeigen, die sich mit einem bestimmten Betreff mit Denkdaten, die aktueller als letzte Woche sind, handelt. Verweise auf nachrichten, die den Kriterien entsprechen, werden im Suchergebnisordner aufgeführt, und die tatsächlichen Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten sind die Einheiten von Daten, die von einem Benutzer oder einer Anwendung an einen anderen Benutzer oder eine andere Anwendung übertragen werden. Jede Nachricht enthält einige Nachrichtentext- und Nachrichtenumschlaginformationen, die für die Übertragung verwendet werden. Einige Nachrichten enthalten eine oder mehrere Anlagen oder zusätzliche Daten im Zusammenhang mit einer Nachricht in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Der Beispielanbieter für umschlossene Store PST

Die Replikations-API ermöglicht das Replizieren von Elementen aus einem Back-End-Datenrepository in Outlook PST-Speicher. Sie verwenden die Replikations-API, um die Daten in einen dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus zu verfolgen. Für diesen Ansatz ist es nicht erforderlich, einen benutzerdefinierten MAPI-Speicheranbieter einzuführen, der komplex zu schreiben und zu warten ist. Der Anbieter des PST-Speichers muss jedoch umschlossen werden, um mit der Replikations-API zu arbeiten.
  
Der Beispielanbieter für Store PST verwendet den Anbieter für persönliche Ordner als Back-End zum Speichern von Daten. Der umschlossene PST-Speicheranbieter sollte in Verbindung mit der Replikations-API verwendet werden. Weitere Informationen finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md). Die meisten Funktionen im Beispielanbieter für umschlossene STORE übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Installieren des Umschlossenen Store -Beispielanbieters](installing-the-sample-wrapped-pst-store-provider.md)
    
- Erläutert, wie Sie den Beispielanbieter für umbrochene PST Store installieren.
    
- [Initialisieren eines umschlossenen STORE Anbieters](initializing-a-wrapped-pst-store-provider.md)
    
- Der erste Schritt bei der Implementierung eines umschlossenen PST Store-Anbieters besteht in der Initialisierung und Konfiguration des umschlossenen PST Store-Anbieters.
    
- [Anmelden bei einem umschlossenen STORE Anbieter](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Nachdem ein umschlossener PST Store-Anbieter initialisiert wurde, müssen Sie Funktionen implementieren, damit sich MAPI und der MAPI-Spooler beim umschlossenen ANBIETER für den PST Store anmelden können.
    
- [Verwenden eines umschlossenen STORE Anbieters](using-a-wrapped-pst-store-provider.md)
    
- Um einen umschlossenen ANBIETER für den PST Store zu verwenden, müssen Sie die **[IMAPISupport::IUnknown-Schnittstelle](imapisupportiunknown.md)** umschließen, um allgemeine Aufgaben des umschlossenen PST Store-Anbieters zu implementieren. 
    
- [Herunterfahren eines umschlossenen STORE Anbieters](shutting-down-a-wrapped-pst-store-provider.md)
    
- Nachdem Sie die Verwendung eines umschlossenen PST Store-Anbieters abgeschlossen haben, müssen Sie den umschlossenen ANBIETER für den PST Store ordnungsgemäß herunterfahren.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

