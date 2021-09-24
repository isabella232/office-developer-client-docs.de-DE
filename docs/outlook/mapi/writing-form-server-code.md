---
title: Schreiben von Formularservercode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: daade632a10b48e6db88ece286f53db4ae95a804
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549763"
---
# <a name="writing-form-server-code"></a>Schreiben von Formularservercode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können sich einen Formularserver wie folgt vorstellen: 
  
- Ein Win32-Programm, das eine Schnittstelle anzeigt und Windows-Nachrichten mithilfe der standardmäßigen Windows Nachrichtenmechanismen verarbeitet.
    
- Ein Objekt, das seine Klassenfactory bei OLE registriert und durch OLE-Automatisierungsmethoden aktiviert wird.
    
- Ein MAPI-Objekt, das den MAPI-Regeln für Interaktionen mit anderen MAPI-Komponenten folgt.
    
 Ihr Code muss alle drei dieser allgemeinen Anforderungen gleichzeitig verarbeiten. 
  
Weitere Informationen zum Registrieren der Klassenfactory Ihres Formularservers finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK. Die Behandlung von Windows-Nachrichten und das Anzeigen einer Schnittstelle sind Standardmäßige Windows Programmiertechniken, die keine besonderen Anforderungen in Bezug auf MAPI-Formulare haben. Auch hier enthält das Windows SDK Details zum programmieren Windows. Dieses Dokument enthält das, was Sie wissen müssen, um die erforderlichen und optionalen MAPI-Formularschnittstellen zu implementieren, damit diese den MAPI-Regeln für Interaktionen mit anderen MAPI-Komponenten folgen – in erster Linie dem MAPI-Formular-Manager und Denkclientanwendungen.
  
Alle Schnittstellen, die Sie beim Implementieren von Formularservern verwenden können, werden – entweder direkt oder indirekt – von der OLE-Basisklasse [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)abgeleitet. Dies bedeutet, dass alle Implementierungen dieser Schnittstellen über **QueryInterface-,** **AddRef-** und **Release-Methoden** verfügen müssen. Sie können sich viel Arbeit ersparen, wenn Sie mehrere Vererbung verwenden, um alle erforderlichen Schnittstellen in einer neuen Klasse zu implementieren, sodass alle verwendeten Schnittstellen eine einzige Implementierung der erforderlichen **IUnknown-Methoden** gemeinsam nutzen können. Weitere Informationen finden Sie unter den Methoden [IUnknown::AddRef,](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)und [IUnknown::Release.](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) Es gibt keine besonderen Überlegungen in Bezug auf MAPI-Formularserver für diese Methoden. 
  
Obwohl nicht alle MAPI-Formularschnittstellen für alle Formularserver obligatorisch sind, sind die Methoden in einer bestimmten Schnittstelle obligatorisch. Wenn Sie also eine bestimmte Schnittstelle implementieren möchten, müssen Sie alle Methoden in der Schnittstelle implementieren. Dies unterscheidet sich von der Situation bei einigen anderen MAPI-Komponenten, z. B. Nachrichtentransporten. Glücklicherweise sind die Methoden in den MAPI-Formularschnittstellen relativ einfach, sodass die Implementierung aller Methoden entwickler nicht sehr belastend ist.
  
Die MAPI-Formularschnittstellen sind unabhängig vom Typ des Entwicklungstools, das zum Erstellen eines Formularservers verwendet wird. Auf diese Weise können Formulare mit unterschiedlichen Entwicklungstools erstellt werden. Die einzige Anforderung besteht darin, dass alle Formularserver die erforderlichen MAPI-Formularschnittstellen unterstützen müssen.
  
Nicht alle MAPI-Schnittstellen, die sich auf Formulare beziehen, sind für alle Formularserver erforderlich. Mit den optionalen Schnittstellen können Sie einige erweiterte Formularfunktionen implementieren, die von den meisten Formularservern nicht benötigt werden. In der folgenden Tabelle sind die Schnittstellen, deren Zweck und ihre Implementierung aufgeführt.
  
|**Schnittstelle**|**Beschreibung**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |Die primäre Schnittstelle, die Clients zum Laden von Formularservern, Ausführen von Formularverben und Herunterfahren von Formularservern verwenden. Dies ist auch die von OLE **IUnknown** abgeleitete Schnittstelle, die verwendet wird, um andere OLE-Komponenten darüber zu informieren, welche Schnittstellen ein Formularobjekt implementiert.  <br/> |Erforderlich  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Wird beim Laden von Nachrichten in und Speichern von Nachrichten aus Formularobjekten verwendet.  <br/> |Erforderlich  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Wird von Formularobjekten verwendet, um den Status des Messagingclients nachzuverfolgen und herauszufinden, ob das Formularobjekt die nächste oder vorherige Nachricht in einem Ordner anzeigen kann.  <br/> |Optional  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |Die von Formularobjekten verwendete OLE-Klassenfactoryschnittstelle für die Kompatibilität mit dem Mechanismus der OLE-Klassenfactory.  <br/> |Erforderlich  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Wird verwendet, wenn der Formularserver mehrere Formulartypen unterstützt. In diesem Fall ermöglicht die **IMAPIFormFactory-Schnittstelle** Clientanwendungen den Zugriff auf die mehreren **IClassFactory-Schnittstellen** (eine pro Formulartyp, den der Formularserver unterstützt), die der Formularserver ebenfalls implementieren muss.  <br/> |Optional  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

