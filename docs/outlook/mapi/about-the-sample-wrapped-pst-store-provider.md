---
title: Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 6814244de23d97e6004490bc85b8a3b503d9b8ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551884"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Übersicht über Nachrichtenanbieter Store

Nachrichtenspeicheranbieter verarbeiten das Speichern und Abrufen von Nachrichten und anderen Informationen für die Benutzer von Clientanwendungen. Die Nachrichteninformationen werden mithilfe eines hierarchischen Systems organisiert, das als Nachrichtenspeicher bezeichnet wird. Der Nachrichtenspeicher ist auf mehreren Ebenen implementiert, mit Containern, die als Ordner bezeichnet werden, die Nachrichten unterschiedlicher Typen enthalten. Es gibt keine Beschränkung für die Anzahl der Ebenen in einem Nachrichtenspeicher. Ordner können viele Unterordner enthalten.
  
Nachrichtenspeicherdaten können auf unterschiedliche Weise verwendet werden. Zusätzlich zur typischen E-Mail-Verwendung können Ordner als Forum für öffentliche Diskussionen, als Repository für Referenzdokumente oder als Container für Informationen zu Denkbretts verwendet werden. Ein einzelner Nachrichtenspeicher kann viele Arten von Informationen enthalten, einige sind modifizierbar und andere nicht. Mehrere Clients können denselben Nachrichtenspeicher installieren, sodass Daten einfach und schnell freigegeben werden können.
  
Nachrichtenspeicherordner ermöglichen es Ihnen, Nachrichten zu sortieren und zu filtern und die Ansicht auf einer Benutzeroberfläche anzupassen. Links zu gefilterten Nachrichten werden in speziellen Ordnern gespeichert, die als Suchergebnisordner bezeichnet werden. Der Benutzer einer Clientanwendung gibt Filterkriterien ein, die mapi als Einschränkung bezeichnet, und die Kriterien werden auf die in einem oder mehreren Ordnern gespeicherten Nachrichten angewendet. Ein Benutzer möchte z. B. nur die Nachrichten anzeigen, die sich auf einen bestimmten Betreff beziehen, deren Eintreffen datum aktueller als in der letzten Woche ist. Verweise auf die Nachrichten, die den Kriterien entsprechen, werden im Ordner "Suchergebnisse" aufgeführt, und die tatsächlichen Nachrichten verbleiben in ihren regulären Ordnern.
  
Nachrichten sind die Dateneinheiten, die von einem Benutzer oder einer Anwendung an einen anderen Benutzer oder eine andere Anwendung übertragen werden. Jede Nachricht enthält nachrichtentext- und nachrichtenumschlagsinformationen, die für die Übertragung verwendet werden. Einige Nachrichten enthalten eine oder mehrere Anlagen oder zusätzliche Daten, die sich auf eine Nachricht in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts beziehen und mit dieser übertragen werden.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Das Beispiel für einen umschlossenen PST-Store-Anbieter

Mit der Replikations-API können Sie Elemente aus einem Back-End-Daten-Repository in einen Outlook PST-Speicher replizieren. Verwenden Sie die Replikations-API, um die Daten in einen dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus nachzuverfolgen. Bei diesem Ansatz müssen Sie keinen benutzerdefinierten MAPI-Speicheranbieter einführen, der zum Schreiben und Verwalten komplex ist. Der ANBIETER des PST-Speichers muss jedoch umbrochen werden, um mit der Replikations-API zu arbeiten.
  
Der PsT-Anbieter (Sample Wrapped PST Store) verwendet den Anbieter der persönlichen Ordnerdatei (Personal Folders File, PST) als Back-End zum Speichern von Daten. Der anbieterumschlossene PST-Speicher sollte in Verbindung mit der Replikations-API verwendet werden. Weitere Informationen finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md) Die meisten Funktionen im beispielumschlossenen PST-Store-Anbieter übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Installieren des Beispielanbieters für pst-Store](installing-the-sample-wrapped-pst-store-provider.md)
    
- Erläutert das Herunterladen und Installieren des Beispielanbieters für pst-Store.
    
- [Initialisieren eines Anbieters von umschlossenen PST-Store](initializing-a-wrapped-pst-store-provider.md)
    
- Der erste Schritt bei der Implementierung eines Anbieters für einen umschlossenen PST-Speicher besteht darin, den Anbieter des umschlossenen PST-Speichers zu initialisieren und zu konfigurieren.
    
- [Anmelden bei einem anbieter umschlossenen PST-Store](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Nachdem ein Anbieter für einen umschlossenen PST-Speicher initialisiert wurde, müssen Sie Funktionen implementieren, damit sich MAPI und der MAPI-Spooler beim Anbieter des umschlossenen PST-Speichers anmelden können.
    
- [Verwenden eines Anbieters von umschlossenen PST-Store](using-a-wrapped-pst-store-provider.md)
    
- Um einen Anbieter für einen umschlossenen PST-Speicher zu verwenden, müssen Sie die **[IMAPISupport::IUnknown-Schnittstelle](imapisupportiunknown.md)** umschließen, um allgemeine Aufgaben des Anbieters von umschlossenen PST-Speicheranbietern zu implementieren. 
    
- [Herunterfahren eines Anbieters von umschlossenen PST-Store](shutting-down-a-wrapped-pst-store-provider.md)
    
- Nachdem Sie einen anbieter umschlossenen PST-Speicher verwendet haben, müssen Sie den Anbieter des umschlossenen PST-Speichers ordnungsgemäß herunterfahren.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

