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
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325794"
---
# <a name="writing-form-server-code"></a>Schreiben von Formularservercode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können sich einen Formularserver wie folgt denken: 
  
- Ein Win32-Programm, das eine Schnittstelle anzeigt und Windows-Nachrichten über die standardmäßigen Nachrichtenpumpmechanismen Windows verarbeitet.
    
- Ein Objekt, das seine Klassen factory bei OLE registriert und durch OLE-Automatisierungsmethoden aktiviert wird.
    
- Ein MAPI-Objekt, das den MAPI-Regeln für Interaktionen mit anderen MAPI-Komponenten folgt.
    
 Ihr Code muss alle drei dieser umfassenden Anforderungen gleichzeitig verarbeiten. 
  
Weitere Informationen zum Registrieren der Klassen factory ihres Formularservers finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK. Die Verarbeitung von Windows-Nachrichten und das Anzeigen einer Schnittstelle sind Windows Programmiertechniken, die keine besonderen Anforderungen an MAPI-Formulare haben. Auch hier enthält das Windows SDK Details zur Windows Programmierung. Dieses Dokument enthält das, was Sie wissen müssen, um die erforderlichen und optionalen MAPI-Formularschnittstellen zu implementieren, damit sie die MAPI-Regeln für Interaktionen mit anderen MAPI-Komponenten befolgen – in erster Linie den MAPI-Formular-Manager und Messagingclientanwendungen.
  
Alle Schnittstellen, die Sie beim Implementieren von Formularservern verwenden können, werden direkt oder indirekt von der OLE-Basisklasse [IUnknown abgeleitet.](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) Dies bedeutet, dass alle Implementierungen dieser Schnittstellen **die Methoden QueryInterface,** **AddRef** und **Release benötigen.** Sie können sich viel Arbeit sparen, wenn Sie mehrere Vererbungen verwenden, um alle erforderlichen Schnittstellen in einer eigenen neuen Klasse zu implementieren, sodass alle verwendeten Schnittstellen eine einzige Implementierung der erforderlichen **IUnknown-Methoden** gemeinsam nutzen können. Weitere Informationen finden Sie unter [den Methoden IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)und [IUnknown::Release.](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) Für diese Methoden gibt es keine besonderen Überlegungen in Bezug auf MAPI-Formularserver. 
  
Obwohl nicht alle MAPI-Formularschnittstellen für alle Formularserver obligatorisch sind, sind die Methoden in einer bestimmten Schnittstelle obligatorisch. Wenn Sie also eine bestimmte Schnittstelle implementieren möchten, müssen Sie alle Methoden in der Schnittstelle implementieren. Dies ist anders als bei einigen anderen MAPI-Komponenten, z. B. Nachrichtentransporten. Glücklicherweise sind die Methoden in den MAPI-Formularschnittstellen relativ einfach, sodass die Implementierung aller Methoden keine große Belastung für Entwickler bedeutet.
  
Die MAPI-Formularschnittstellen sind unabhängig vom Typ des Entwicklungstools, das zum Erstellen eines Formularservers verwendet wird. Dadurch können Formulare mithilfe verschiedener Entwicklungstools erstellt werden. Die einzige Anforderung ist, dass alle Formularserver die erforderlichen MAPI-Formularschnittstellen unterstützen müssen.
  
Nicht alle MAPI-Schnittstellen, die sich auf Formulare beziehen, sind von allen Formularservern erforderlich. Mit den optionalen Schnittstellen können Sie einige erweiterte Formularfunktionen implementieren, die von den meisten Formularservern nicht benötigt werden. In der folgenden Tabelle sind die Schnittstellen aufgeführt, wofür sie stehen und ob Sie sie implementieren müssen.
  
|**Schnittstelle**|**Beschreibung**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |Die primäre Schnittstelle, die Clients zum Laden von Formularservern, Ausführen von Formularverben und Herunterfahren von Formularservern verwenden. Dies ist auch die vom OLE **IUnknown** abgeleitete Schnittstelle, die verwendet wird, um andere OLE-Komponenten darüber zu informieren, welche Schnittstellen ein Formularobjekt implementiert.  <br/> |Erforderlich  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Wird beim Laden von Nachrichten in und Speichern von Nachrichten aus Formularobjekten verwendet.  <br/> |Erforderlich  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Wird von Formularobjekten verwendet, um den Status des Messagingclients nachverfolgt und herauszufinden, ob das Formularobjekt die nächste oder vorherige Nachricht in einem Ordner anzeigen kann.  <br/> |Optional.  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |Die von Formularobjekten verwendete Factoryschnittstelle der OLE-Klasse zur Einhaltung des OLE-Klasse-Factorymechanismus.  <br/> |Erforderlich  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Wird verwendet, wenn der Formularserver mehrere Formulartypen unterstützt. In diesem Fall ermöglicht die **IMAPIFormFactory-Schnittstelle** Clientanwendungen den Zugriff auf die **mehreren IClassFactory-Schnittstellen** (eine pro Formulartyp, die ihr Formularserver unterstützt), die ihr Formularserver ebenfalls implementieren muss.  <br/> |Optional.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

