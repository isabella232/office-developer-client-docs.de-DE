---
title: Informationen über das Beispiel für einen Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: 399c86d189cfc4160d151f417a6dd20364e60ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563828"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Informationen über das Beispiel für einen Anbieter von umschlossenem PST-Speicher

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Übersicht über die Nachrichtenspeicher-Anbieter

Nachricht Anbieter behandeln die Speicherung und den Abruf von Nachrichten und andere Informationen für die Benutzer der Clientanwendungen. Informationen der Nachricht ist mit einer hierarchischen System bekannt als Nachrichtenspeicher organisiert. Nachrichtenspeicher implementiert ist in mehreren Ebenen mit Containern aufgerufen, Ordner, die Nachrichten von unterschiedlichen Elementtypen enthalten. Es gibt keine Beschränkung der Anzahl der Ebenen in einem Nachrichtenspeicher. Ordner können viele Unterordner enthalten.
  
Nachricht Speichern von Daten können auf verschiedene Weise verwendet werden. Zusätzlich zu den normalen e-Mail-Nutzung können Ordner als Forum für Öffentliche Diskussion, als Repository für Referenzdokumenten oder als Container für Bulletin Board-Informationen verwendet werden. Ein einzelnen Nachrichtenspeicher kann viele Arten von Informationen, einige änderbare und andere nicht enthalten. Mehrere Clients können den gleichen Nachrichtenspeicher installieren leicht, einfach und schnell zum Freigeben von Daten.
  
Nachricht Speicherordner zum Sortieren und Filtern können Sie Nachrichten und zum Anpassen der Ansicht in der Anzeige einer Benutzer-Benutzeroberfläche (UI). Links zu gefilterten Nachrichten werden in Spezialordnern aufgerufen Suchergebnisse Ordner gespeichert. Der Benutzer von einer Clientanwendung gibt Filterkriterien, die MAPI bezieht sich auf als eine Einschränkung, und die Kriterien auf die Nachrichten in einen oder mehrere Ordner angewendet wird. Beispielsweise kann ein Benutzer anzeigen möchten nur Nachrichten Umgang mit einem bestimmten Thema mit hinzukommen Datumsangaben, die aktueller ist als die letzte Woche liegen. Verweise auf die Nachrichten, die den Kriterien im Suchergebnisse Ordner aufgeführt sind, und die echten Nachrichten in ihren regulären Ordnern verbleiben.
  
Nachrichten werden die Daten von einem Benutzer oder eine Anwendung an einen anderen Benutzer oder eine Anwendung übertragen. Jede Nachricht enthält einige Nachrichtentext und Informationen im Nachrichtenumschlag, die für die Übertragung verwendet wird. Einige Nachrichten enthalten eine oder mehrere Anlagen oder zusätzliche Daten im Zusammenhang mit und transportiert mit einer Nachricht in Form einer Datei, eine andere Nachricht oder ein OLE-Objekt.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Im Beispiel umgebrochen PST-Anbieter

Replikation der API können Sie Elemente in einer Outlook-PST-Speicher aus einem Back-End-Daten-Repository repliziert werden. Sie verwenden die Replikation-API zum Replizieren von Daten in einer dedizierten PST-Speicher und verfolgen an den Synchronisierungsstatus. Dieser Ansatz erfordert keinen Sie einen benutzerdefinierten MAPI-Speicher-Anbieter einführen, der schreiben und Verwalten komplexer ist. Der PST-Speicher-Anbieter müssen jedoch umbrochen werden, damit die Replikation API entwickelt.
  
Der umbrochen PST Store Beispielanbieter verwendet den Persönliche Ordner-Datei (PST) Anbieter als Back-End zum Speichern von Daten. Der gepackten PST-Speicheranbieter sollte in Verbindung mit der API für die Replikation verwendet werden. Weitere Informationen finden Sie unter [Informationen zu Replikation API](about-the-replication-api.md). Die meisten Funktionen in der umbrochen PST Store Beispielanbieter übergeben ihre Argumente direkt an dem zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern besondere Implementierung und werden in den folgenden Themen beschrieben.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Installieren des Beispiel für einen Anbieter von umschlossenem PST-Speicher](installing-the-sample-wrapped-pst-store-provider.md)
    
- Erläutert das Herunterladen und Installieren der umbrochen PST Store Beispielanbieter.
    
- [Initialisieren eines Anbieters von umschlossenem PST-Speicher](initializing-a-wrapped-pst-store-provider.md)
    
- Der erste Schritt beim Implementieren von eines gepackten PST-Anbieters wird initialisiert und Konfigurieren des gepackten PST-Anbieters.
    
- [Anmelden bei einem Anbieter von umschlossenem PST-Speicher](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Nach ein gepackten PST-Anbieter initialisiert wird, müssen Sie Funktionen implementieren, sodass MAPI- und die MAPI-Warteschlange auf dem gepackten PST-Anbieter anmelden können.
    
- [Verwenden eines Anbieters von umschlossenem PST-Speicher](using-a-wrapped-pst-store-provider.md)
    
- Zum Verwenden einer gepackten PST-Speichers umgebrochen Anbieter die **[IMAPISupport::IUnknown](imapisupportiunknown.md)** -Schnittstelle zum Implementieren von allgemeinen Text fließt um müssen PST-Speicher-Anbieter Aufgaben. 
    
- [Herunterfahren eines Anbieters von umschlossenem PST-Speicher](shutting-down-a-wrapped-pst-store-provider.md)
    
- Nach Abschluss der mit einem gepackten PST-Anbieter, müssen Sie die gepackten PST-Speicheranbieter ordnungsgemäß herunterfahren.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

