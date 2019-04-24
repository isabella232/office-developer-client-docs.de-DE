---
title: Schreiben von Formular Server Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325794"
---
# <a name="writing-form-server-code"></a>Schreiben von Formular Server Code

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können sich einen Formularserver wie folgt vorstellen: 
  
- Ein Win32-Programm, das eine Schnittstelle anzeigt und Windows-Nachrichten mithilfe der standardmäßigen Windows Message Pump-Mechanismen behandelt.
    
- Ein Objekt, das seine Klassen Factory mit OLE registriert und von OLE-Automatisierungsmethoden aktiviert wird.
    
- Ein MAPI-Objekt, das den MAPI-Regeln für Interaktionen mit anderen MAPI-Komponenten folgt.
    
 Ihr Code muss alle drei dieser allgemeinen Anforderungen gleichzeitig verarbeiten. 
  
Weitere Informationen zum Registrieren der Klassen Factory Ihres Formular Servers finden Sie im Abschnitt COM-und ActiveX-Objektdienste im Windows SDK. Die Behandlung von Windows-Nachrichten und das Anzeigen einer Schnittstelle sind standardmäßige Windows-Programmiertechniken, die keine speziellen Anforderungen in Bezug auf MAPI-Formulare aufweisen. Auch hier enthält das Windows SDK Details zur Windows-Programmierung. Dieses Dokument enthält Informationen, die Sie benötigen, um die erforderlichen und optionalen MAPI-Formular Schnittstellen zu implementieren, damit Sie den MAPI-Regeln für Interaktionen mit anderen MAPI-Komponenten folgen, vor allem dem MAPI-Formular-Manager und den Messaging-Clientanwendungen.
  
Alle Schnittstellen, die Sie beim Implementieren von Formular Servern verwenden können, werden direkt oder indirekt aus der OLE-Basisklasse [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)abgeleitet. Dies führt dazu, dass alle Ihre Implementierungen dieser Schnittstellen die **QueryInterface**-, **AddRef**-und **Release** -Methoden aufweisen müssen. Sie können sich selbst eine Menge Arbeit sparen, wenn Sie mehrere Vererbung verwenden, um alle erforderlichen Schnittstellen in einer neuen Klasse zu implementieren, sodass alle verwendeten Schnittstellen eine einzelne Implementierung der erforderlichen **IUnknown** -Methoden freigeben können. Weitere Informationen finden Sie unter den Methoden [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)und [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) . Für diese Methoden gibt es keine besonderen Überlegungen hinsichtlich der MAPI-Formularserver. 
  
Obwohl nicht alle MAPI-Formular Schnittstellen für alle Formularserver obligatorisch sind, sind die Methoden in einer bestimmten Schnittstelle obligatorisch. Wenn Sie also eine bestimmte Schnittstelle implementieren möchten, müssen Sie alle Methoden in der Schnittstelle implementieren. Dies unterscheidet sich von der Situation mit einigen anderen MAPI-Komponenten wie Nachrichtenverkehr. Glücklicherweise sind die Methoden in den MAPI-Formular Schnittstellen relativ einfach, sodass Entwickler durch deren Implementierung nicht besonders belastet werden.
  
Die MAPI-Formular Schnittstellen sind unabhängig vom Typ des Entwicklungstools, das zum Erstellen eines Formular Servers verwendet wird. Dadurch können Formulare mit verschiedenen Entwicklungstools erstellt werden. Die einzige Voraussetzung ist, dass alle Formularserver die erforderlichen MAPI-Formular Schnittstellen unterstützen müssen.
  
Nicht alle MAPI-Schnittstellen, die sich auf Formulare beziehen, sind für alle Formularserver erforderlich. Mit den optionalen Schnittstellen können Sie einige erweiterte Formularfunktionen implementieren, die von den meisten Formular Servern nicht benötigt werden. In der folgenden Tabelle sind die Schnittstellen, deren Zweck und die Implementierung aufgeführt.
  
|**Schnittstelle**|**Beschreibung**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |Die primäre Schnittstelle, über die Clients Formularserver laden, Formular Verben ausführen und Formularserver Herunterfahren. Dies ist auch die Schnittstelle, die vom OLE **IUnknown** abgeleitet wird und andere OLE-Komponenten darüber informiert, welche Schnittstellen ein Form-Objekt implementiert.  <br/> |Erforderlich  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Wird beim Laden von Nachrichten und Speichern von Nachrichten aus Formularobjekten verwendet.  <br/> |Erforderlich  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Wird von Formularobjekten verwendet, um den Status des Messagingclients nachzuverfolgen und herauszufinden, ob das Formularobjekt die nächste oder vorherige Nachricht in einem Ordner anzeigen kann.  <br/> |Optional  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |Die von Form-Objekten verwendete OLE-Klassenfactory-Schnittstelle für die Einhaltung des OLE-Klassenfactory-Mechanismus.  <br/> |Erforderlich  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Wird verwendet, wenn der Formularserver mehr als einen Formulartyp unterstützt. In diesem Fall ermöglicht die **IMAPIFormFactory** -Schnittstelle Clientanwendungen den Zugriff auf mehrere **IClassFactory** -Schnittstellen (eine pro Formulartyp, die von Ihrem Formularserver unterstützt werden), die der Formularserver auch implementieren muss.  <br/> |Optional  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

