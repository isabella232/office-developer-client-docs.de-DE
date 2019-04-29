---
title: Informationen zum einGebundenen PST-Speicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432723"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Informationen zum einGebundenen PST-Speicheranbieter

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Übersicht über Nachrichtenspeicher Anbieter

Nachrichtenspeicher Anbieter behandeln das Speichern und Abrufen von Nachrichten und anderen Informationen für die Benutzer von Clientanwendungen. Die Nachrichten Informationen werden mithilfe eines hierarchischen Systems organisiert, das als Nachrichtenspeicher bezeichnet wird. Der Nachrichtenspeicher wird auf mehreren Ebenen implementiert, wobei Container als Ordner bezeichnet werden, die Nachrichten unterschiedlicher Typen enthalten. Es gibt keine Begrenzung für die Anzahl der Ebenen in einem Nachrichtenspeicher; Ordner können viele Unterordner enthalten.
  
Nachrichtenspeicher Daten können auf unterschiedliche Weise verwendet werden. Neben der typischen e-Mail-Verwendung können Ordner als Forum für öffentliche Diskussionen, als Repository für Referenzdokumente oder als Container für Bulletin Board-Informationen verwendet werden. Ein einzelner Nachrichtenspeicher kann viele Arten von Informationen enthalten, einige änderbar und andere nicht. Mehrere Clients können denselben Nachrichtenspeicher installieren, sodass Daten problemlos und schnell freigegeben werden.
  
Mit dem Nachrichtenspeicher Ordner können Sie Nachrichten sortieren und Filtern und die Ansicht in einer Benutzeroberfläche (UI) anpassen. Links zu gefilterten Nachrichten werden in speziellen Ordnern mit dem Namen Suchergebnisordner gespeichert. Der Benutzer einer Clientanwendung gibt Filterkriterien ein, auf die MAPI als Einschränkung verweist, und die Kriterien werden auf die Nachrichten angewendet, die in einem oder mehreren Ordnern gespeichert sind. Beispielsweise kann ein Benutzer nur die Nachrichten anzeigen, die sich auf einen bestimmten Betreff beziehen, und zwar mit Anreise Terminen, die jünger sind als letzte Woche. Verweise auf die Nachrichten, die den Kriterien entsprechen, werden im Ordner Suchergebnisse aufgeführt, und die tatsächlichen Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten sind die Dateneinheiten, die von einem Benutzer oder einer Anwendung an einen anderen Benutzer oder eine andere Anwendung übertragen werden. Jede Nachricht enthält einige Nachrichtentext-und Nachrichtenumschlag Informationen, die für die Übertragung verwendet werden. Einige Nachrichten verfügen über eine oder mehrere Anhänge oder zusätzliche Daten im Zusammenhang mit einer Nachricht in Form einer Datei, einer anderen Nachricht oder einem OLE-Objekt.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Der beispielhafte PST-Speicheranbieter

Mit der Replikations-API können Sie Elemente aus einem Back-End-Daten-Repository in einen Outlook-PST-Speicher replizieren. Sie verwenden die Replikations-API, um die Daten in einem dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus nachzuverfolgen. Dieser Ansatz erfordert nicht, dass Sie einen benutzerdefinierten MAPI-Speicheranbieter einführen, der Komplex ist, um zu schreiben und zu warten. Der PST-Speicheranbieter muss jedoch für die Zusammenarbeit mit der Replikations-API verpackt werden.
  
Der Beispiel-Wrapped-PST-Speicheranbieter verwendet den PST-Anbieter als Back-End zum Speichern von Daten. Der verpackte PST-Speicheranbieter sollte in Verbindung mit der Replikations-API verwendet werden. Weitere Informationen finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md). Die meisten Funktionen im beispielhaften PST-Speicheranbieter übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Installieren des eingeWickelten Beispiel-PST-Speicheranbieters](installing-the-sample-wrapped-pst-store-provider.md)
    
- Erläutert das herunterladen und Installieren des Beispiels Wrapped-PST-Speicheranbieters.
    
- [Initialisieren eines einGebundenen PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md)
    
- Der erste Schritt bei der Implementierung eines eingebundenen PST-Speicheranbieters besteht in der Initialisierung und Konfiguration des eingebundenen PST-Speicheranbieters.
    
- [Anmelden bei einem einGebundenen PST-Speicheranbieter](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Nachdem ein eingebundener PST-Speicheranbieter initialisiert wurde, müssen Sie Funktionen implementieren, damit MAPI und der MAPI-Spooler sich beim eingebundenen PST-Speicheranbieter anmelden können.
    
- [Verwenden eines einGebundenen PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md)
    
- Um einen eingebundenen PST-Speicheranbieter verwenden zu können, müssen Sie die **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** -Schnittstelle einschließen, um häufig eingebundene PST-Speicheranbieter Aufgaben zu implementieren. 
    
- [Herunterfahren eines einGebundenen PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md)
    
- Nachdem Sie einen eingebundenen PST-Speicheranbieter abgeschlossen haben, müssen Sie den eingebundenen PST-Speicheranbieter ordnungsgemäß herunterfahren.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

