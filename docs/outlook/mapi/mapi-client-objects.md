---
title: MAPI-Clientobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319289"
---
# <a name="mapi-client-objects"></a>MAPI-Clientobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Standard-Messaging-Clientanwendungen implementieren nur ein Objekt – eine Advise-Senke. Advise-Senken erben von der [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle und werden von MAPI und Dienstanbietern für Ereignisbenachrichtigungen verwendet. Einige Clients implementieren auch Progress-Objekte zur Unterstützung der Anzeige von Fortschritts Dialogfeldern. 
  
Komplexere Clients, die benutzerdefinierte Formulare unterstützen, implementieren ein weiteres Advise-Senke-Objekt und einige andere Objekte, wie das Nachrichten Site Objekt, das von der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle erbt, und das View-Kontextobjekt, das von der [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) -Schnittstelle. Das zusätzliche Advise-Senke-Objekt erbt von der [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle. 
  
In der folgenden Tabelle werden die MAPI-Objekte zusammengefasst, die von Standard-Messaging-Clients und von Clients implementiert werden, die die Anzeige benutzerdefinierter Formulare unterstützen.
  
|**Client Objekt**|**Beschreibung**|
|:-----|:-----|
|Advise-Senke  <br/> |Stellt eine Rückruffunktion für Ereignisse bereit, die im Nachrichtenspeicher, im Adressbuch oder in der Sitzung auftreten.  <br/> |
|Nachrichtenwebsite  <br/> |Behandelt die Bearbeitung von Formularobjekten.  <br/> |
|Status  <br/> |Zeigt ein Dialogfeld an, in dem der Fortschritt eines Vorgangs angezeigt wird.  <br/> |
|Anzeigen der Advise-Senke  <br/> |Stellt Rückruffunktionen für Ereignisse bereit, die in einem Formular auftreten.  <br/> |
|Ansichtskontext  <br/> |Unterstützt Befehle zum Drucken und Speichern von Formularen und zum Navigieren zwischen Formularen.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen diesen verschiedenen Clientobjekten, die Schnittstellen, von denen Sie erben, und die MAPI-Komponenten, die Sie verwenden. 
  
![Client Objekte und entsprechende Schnittstellen] (media/amapi_65.gif "Client Objekte und entsprechende Schnittstellen")
  
Clients verwenden viel mehr Objekte als implementiert. Alle Clients verwenden ein Session-Objekt, um Zugriff auf eine Vielzahl von Dienstanbieter Objekten und Objekten zu erhalten, die von MAPI implementiert werden. Clients interagieren mit Dienstanbietern entweder indirekt, über die Sitzung, das Adressbuch oder die von MAPI bereitgestellten Statusobjekte oder direkt über eine Vielzahl von Objekten, die bestimmte Dienstanbieter implementieren. Um direkten Kontakt mit Adressbuch Anbietern herzustellen, verwenden Clients Adressbuchcontainer, Messagingbenutzer und Verteilerlisten. Für den direkten Zugriff auf einen Nachrichtenspeicher Anbieter verwenden Clients das Nachrichtenspeicherobjekt, Ordner, Nachrichten und Anlagen. Wenn Dienstanbieter ein Status-Objekt unterstützen, können Clients das Status-Objekt verwenden, um den Status des Dienstanbieters zu überwachen.
  
Clients, die die Konfiguration des Dienstanbieters und des Nachrichtendiensts unterstützen, verwenden drei Objekte, die von MAPI implementiert werden: das Nachrichtendienst-Verwaltungsobjekt, das Profilverwaltungsobjekt und das Anbieter Verwaltungsobjekt. Clients, die benutzerdefinierte Formulare anzeigen, verwenden mehrere Formularobjekte, die von einem Formularbibliothek Anbieter oder einem Formularserver implementiert werden.
  
## <a name="see-also"></a>Siehe auch

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

