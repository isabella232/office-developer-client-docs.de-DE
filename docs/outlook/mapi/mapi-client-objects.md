---
title: MAPI-Clientobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cea1d2df5d446887bf4ea3d8768a34456a67df98
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579656"
---
# <a name="mapi-client-objects"></a>MAPI-Clientobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Standardmäßige Messaging-Clientanwendungen implementieren nur ein Objekt – eine Empfehlungssenke. Empfehlungssenken erben von der [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) und werden von MAPI und Dienstanbietern für Ereignisbenachrichtigungen verwendet. Einige Clients implementieren außerdem Statusobjekte, um die Anzeige von Statusdialogfeldern zu unterstützen. 
  
Komplexere Clients, die benutzerdefinierte Formulare unterstützen, implementieren ein weiteres Empfehlungssenkenobjekt und einige andere Objekte, z. B. das Nachrichtenwebsiteobjekt, das von der [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) erbt, und das Ansichtskontextobjekt, das von der [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) erbt. Das zusätzliche Advise-Senkenobjekt erbt von der [IMAPIViewAdviseSink : IUnknown-Schnittstelle.](imapiviewadvisesinkiunknown.md) 
  
In der folgenden Tabelle sind die MAPI-Objekte zusammengefasst, die von standardmäßigen Messagingclients und von Clients implementiert werden, die die Anzeige von benutzerdefinierten Formularen unterstützen.
  
|**Client-Objekt**|**Beschreibung**|
|:-----|:-----|
|Empfehlungssenke  <br/> |Stellt eine Rückruffunktion für Ereignisse bereit, die im Nachrichtenspeicher, Adressbuch oder in der Sitzung auftreten.  <br/> |
|Nachrichtenwebsite  <br/> |Behandelt die Manipulation von Formularobjekten.  <br/> |
|Status  <br/> |Zeigt ein Dialogfeld an, in dem der Fortschritt eines Vorgangs angezeigt wird.  <br/> |
|Anzeigen einer Empfehlungssenke  <br/> |Stellt Rückruffunktionen für Ereignisse bereit, die in einem Formular auftreten.  <br/> |
|Kontext anzeigen  <br/> |Unterstützt Befehle zum Drucken und Speichern von Formularen und zum Navigieren zwischen Formularen.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen diesen verschiedenen Clientobjekten, den Schnittstellen, von denen sie erben, und den MAPI-Komponenten, die sie verwenden. 
  
![Clientobjekte und zugehörige Schnittstellen](media/amapi_65.gif "Clientobjekte und zugehörige Schnittstellen")
  
Clients verwenden viel mehr Objekte als sie implementieren. Alle Clients verwenden ein Sitzungsobjekt, um Zugriff auf eine Vielzahl von Dienstanbieterobjekten und Objekten zu erhalten, die mapi implementiert. Clients interagieren mit Dienstanbietern entweder indirekt, über die Sitzung, das Adressbuch oder die von mapi bereitgestellten Statusobjekte oder direkt über eine Vielzahl von Objekten, die von bestimmten Dienstanbietern implementiert werden. Um direkten Kontakt mit Adressbuchanbietern aufzunehmen, verwenden Clients Adressbuchcontainer, Messagingbenutzer und Verteilerlisten. Um direkt auf einen Nachrichtenspeicheranbieter zuzugreifen, verwenden Clients das Nachrichtenspeicherobjekt, Ordner, Nachrichten und Anlagen. Wenn Dienstanbieter ein Statusobjekt unterstützen, können Clients das Statusobjekt verwenden, um den Status des Dienstanbieters zu überwachen.
  
Clients, die die Konfiguration von Dienstanbietern und Nachrichtendiensten unterstützen, verwenden drei Von MAPI implementierte Objekte: das Nachrichtendienst-Verwaltungsobjekt, das Profilverwaltungsobjekt und das Anbieterverwaltungsobjekt. Clients, die benutzerdefinierte Formulare anzeigen, verwenden mehrere Formularobjekte, die von einem Formularbibliotheksanbieter oder einem Formularserver implementiert werden.
  
## <a name="see-also"></a>Siehe auch

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

