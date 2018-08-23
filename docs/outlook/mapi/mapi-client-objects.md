---
title: MAPI-Client-Objekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4242e466b0e784bb260d0525db0e253f1c1f37f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568770"
---
# <a name="mapi-client-objects"></a>MAPI-Client-Objekte
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Standard-Client-Messaginganwendungen implementieren nur ein Objekt – Advise-Empfänger. Advise-Senken von erben die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle und werden von MAPI verwendet und Dienstanbieter für ereignisbenachrichtigung. Einige Clients implementieren auch Fortschritt-Objekte, die die Anzeige von Dialogfeldern Fortschritt zu unterstützen. 
  
Komplexere-Clients, die Unterstützung für benutzerdefinierte Formulare auf einer anderen Advise implementieren Auffangen-Objekt und einige andere Objekte, wie das Objekt "Message" Website, die von erbt die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle und die Ansicht Context-Objekt, das von erbt die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) Schnittstelle. Das Empfängerobjekt zusätzliche Advise erbt von der [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) Schnittstelle. 
  
In der folgenden Tabelle werden die MAPI-Objekte, die von standard-messaging-Clients implementiert und von Clients, die das Anzeigen von benutzerdefinierten Formularen unterstützen zusammengefasst.
  
|**Clientobjekt**|**Beschreibung**|
|:-----|:-----|
|Advise-Empfänger  <br/> |Stellt eine Rückruffunktion für Ereignisse, die in den Nachrichtenspeicher, Adressbuch oder die Sitzung auftreten.  <br/> |
|Nachricht-Website  <br/> |Verarbeitet die Bearbeitung der Formularobjekte.  <br/> |
|Progress  <br/> |Zeigt ein Dialogfeld, um den Fortschritt eines Vorgangs anzuzeigen.  <br/> |
|Ansicht advise-Empfänger  <br/> |Enthält Rückruffunktionen für Ereignisse, die in einem Formular auftreten.  <br/> |
|Ansichtskontext  <br/> |Unterstützt die Befehle zum Drucken und Speichern von Formularen und zum Navigieren zwischen Formularen.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen diesen verschiedene Client-Objekte, die Schnittstellen, von denen sie erben, und die MAPI-Komponenten, die sie verwenden. 
  
![Clientobjekte und entsprechende Schnittstellen] (media/amapi_65.gif "Clientobjekte und entsprechende Schnittstellen")
  
Clients verwenden viele weitere-Objekte, als sie implementieren. Alle Clients verwenden ein Session-Objekt, auf einer Vielzahl von dienstanbieterobjekten und, die von MAPI implementierte Objekte zuzugreifen. Clients interagieren mit-Dienstanbietern indirekt über die Sitzung, das Adressbuch oder die Status-Objekte, die MAPI bereitstellt oder direkt über eine Vielzahl von Objekten, die bestimmten Dienstanbieter implementieren. Zum direkten Kontakt mit adressbuchanbietern implementierte vornehmen möchten, verwenden Clients Address Book-Containern und messaging-Benutzer und Verteilerlisten. Zugriff auf eine Nachricht Speicheranbieter verwenden Clients direkt über das Objekt "Message" Store, Ordner, Nachrichten und Anlagen. Wenn der Dienstanbieter ein Status-Objekt unterstützen, können Clients das Statusobjekt zum Überwachen des Status des Dienstanbieters verwenden.
  
Clients, die Dienstanbieter und Nachricht Dienstkonfiguration unterstützen drei von MAPI implementierte Objekte verwenden: die Message Service Administration-Objekt sowie die Profilverwaltungsobjekt und Verwaltungsobjekt Anbieter. Clients, die benutzerdefinierte Formulare anzeigen verwenden Sie verschiedene Formularobjekte, die einem Formular Bibliotheksanbieter oder einem Formular Server implementiert wird.
  
## <a name="see-also"></a>Siehe auch

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

