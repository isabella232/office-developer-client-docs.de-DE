---
title: Schreiben von Formularservercode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 463193b55dab0839c756367db16d02aae5980a77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578122"
---
# <a name="writing-form-server-code"></a>Schreiben von Formularservercode

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Sie können ein Formular Server wie folgt vorstellen: 
  
- Ein Win32-Programm, zeigt eine Benutzeroberfläche und Windows-Nachrichten über die standardmäßigen Windows Nachricht Pumpe Mechanismen behandelt.
    
- Ein Objekt, das OLE-Klassenfactory, die registriert und von OLE-Automatisierungsmethoden aktiviert ist.
    
- Ein MAPI-Objekt, das den MAPI-Regeln für Interaktionen mit anderen Komponenten MAPI entspricht.
    
 Der Code enthält, gleichzeitig alle drei diese umfassenden Anforderungen zu behandeln. 
  
Siehe Abschnitt COM und ActiveX-Objektdienste im Windows SDK Weitere Informationen zum Registrieren von Ihrem Formular Konferenzserver-Klasse. Behandeln von Windows-Nachrichten und Anzeigen einer Schnittstelle sind standard Windows Programmiertechniken, die nicht über die speziellen Anforderungen in Bezug auf MAPI-Formulare verfügen. Windows SDK auch hier Details zu Windows-Programmierung hat. Dieses Dokument enthält, was Sie wissen, dass die erforderlichen und optionalen MAPI Formular Schnittstellen implementieren, sodass sie die MAPI-Regeln für Interaktionen mit anderen Komponenten MAPI einhalten müssen – in erster Linie die MAPI-Manager und messaging-Clientanwendungen zu bilden.
  
Alle Schnittstellen, die Sie verwenden können, wenn Sie Formular Servern implementieren abgeleitet werden – entweder direkt oder indirekt – aus dem OLE Basisklasse [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx). Dies bedeutet, dass alle die Implementierung dieser Schnittstellen **QueryInterface**, **AddRef**und **Release** Methoden verfügen müssen. Sie können sich eine Menge Arbeit sparen, wenn Sie mehrere Vererbung verwenden, um alle erforderlichen Schnittstellen in eine neue Klasse von eigenen, implementieren, sodass die Schnittstellen, die Sie verwenden eine einzelne Implementierung der erforderlichen **IUnknown** -Methoden freigeben können. Weitere Informationen finden Sie unter [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)und [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methoden. Es gibt keine besondere Aspekte im Hinblick auf die MAPI-Formulars Servern für diese Methoden. 
  
Nicht alle MAPI-Formulars Schnittstellen für alle Formular Server erforderlich sind, sind die Methoden in einer bestimmten Schnittstelle obligatorisch. Wenn Sie eine bestimmte Schnittstelle implementieren auswählen, müssen Sie alle Methoden d. h., in der Schnittstelle implementieren. Dies unterscheidet sich von der Situation mit einige andere MAPI-Komponenten, beispielsweise Nachricht Transporten. Zum Glück sind die Methoden in der MAPI-Formulars Schnittstellen relativ einfach, und implementieren alle diese keine hervorragende Belastung auf Entwickler eingefügt.
  
Die MAPI-Formulars Schnittstellen sind unabhängig von den Typ des Entwicklungstool verwendet, um einen Server Formular zu erstellen. Dadurch können Formulare mit anderen Entwicklungstools erstellt werden soll. Die einzige Anforderung ist, dass alle Formular Server die erforderlichen MAPI Formular Schnittstellen unterstützen müssen.
  
Nicht alle der MAPI-Schnittstellen, die auf Formularen beziehen werden alle Formular Server erforderlich. Die optionalen Schnittstellen können Sie einige Funktionen, die erweiterte Formular zu implementieren, die nicht von den meisten Formular-Servern erforderlich sind. Die folgende Tabelle enthält die Schnittstellen, was für sind und gibt an, ob Sie sie implementieren müssen.
  
|**Schnittstelle**|**Beschreibung**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |Die primäre Schnittstelle, die Clients zu Servern Formular geladen und Verben Formular ausführen Formular Server herunterfahren, verwenden. Dies ist auch die Schnittstelle abgeleitet OLE **IUnknown** , die mit anderen Komponenten OLE, über welche Schnittstellen zu informieren, die ein Form-Objekt implementiert wird.  <br/> |Erforderlich  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Beim Laden von Nachrichten in und Speichern von Nachrichten von Formular-Objekte verwendet.  <br/> |Erforderlich  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Von Formular-Objekte verwendet, um messaging Clientstatus an, und um zu ermitteln, ob das Form-Objekt zum Anzeigen der nächsten oder der vorherigen Nachricht in einem Ordner ist.  <br/> |Optional  <br/> |
|[IClassFactory](http://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |Die OLE-Klasse Factory-Schnittstelle von Formularobjekten für die Einhaltung der OLE-Klasse Factory Mechanismus verwendet.  <br/> |Erforderlich  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Wird verwendet, wenn Ihr Formular Server mehr als ein Formulartyps unterstützt. In diesem Fall kann die Schnittstelle **IMAPIFormFactory** -Clientanwendungen, die mehrere **IClassFactory** -Schnittstellen (eine pro Formulartyp, der Ihrem Formular Server unterstützt) Zugriff auf Ihrem Formular Server muss auch implementieren.  <br/> |Optional  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

