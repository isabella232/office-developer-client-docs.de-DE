---
title: MAPI-Clientobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412408"
---
# <a name="mapi-client-objects"></a>MAPI-Clientobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Standard-Messaging-Clientanwendungen implementieren nur ein Objekt – eine Ratensenke. Ratgebersenken erben von der [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) und werden von MAPI und Dienstanbietern für ereignisbenachrichtigungen verwendet. Einige Clients implementieren auch Statusobjekte, um die Anzeige von Statusdialogfeldern zu unterstützen. 
  
Komplexere Clients, die benutzerdefinierte Formulare unterstützen, implementieren ein weiteres Advise Sink-Objekt und einige andere Objekte, z. B. das Nachrichtenwebsiteobjekt, das von der [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) erbt, und das Ansichtskontextobjekt, das von der [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) erbt. Das zusätzliche Advise Sink-Objekt erbt von der [IMAPIViewAdviseSink : IUnknown-Schnittstelle.](imapiviewadvisesinkiunknown.md) 
  
In der folgenden Tabelle sind die MAPI-Objekte zusammengefasst, die von Standardnachrichtenclients und von Clients implementiert werden, die die Anzeige benutzerdefinierter Formulare unterstützen.
  
|**Clientobjekt**|**Beschreibung**|
|:-----|:-----|
|Ratensenke  <br/> |Stellt eine Rückruffunktion für Ereignisse im Nachrichtenspeicher, adressbuch oder in der Sitzung zur Verfügung.  <br/> |
|Nachrichtenwebsite  <br/> |Behandelt die Bearbeitung von Formularobjekten.  <br/> |
|Status  <br/> |Zeigt ein Dialogfeld an, um den Fortschritt eines Vorgangs anzuzeigen.  <br/> |
|Anzeigen der Ratensenke  <br/> |Stellt Rückruffunktionen für Ereignisse in einem Formular zur Verfügung.  <br/> |
|Kontext anzeigen  <br/> |Unterstützt Befehle zum Drucken und Speichern von Formularen und zum Navigieren zwischen Formularen.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen diesen verschiedenen Clientobjekten, den Schnittstellen, von denen sie erben, und den MAPI-Komponenten, die sie verwenden. 
  
![Clientobjekte und entsprechende Schnittstellen](media/amapi_65.gif "Clientobjekte und entsprechende Schnittstellen")
  
Clients verwenden viel mehr Objekte als sie implementieren. Alle Clients verwenden ein Sitzungsobjekt, um Zugriff auf eine Vielzahl von Dienstanbieterobjekten und -objekten zu erhalten, die MAPI implementiert. Clients interagieren mit Dienstanbietern entweder indirekt, über die Sitzung, das Adressbuch oder die von MAPI zur Verfügung stellenen Statusobjekte oder direkt über eine Vielzahl von Objekten, die von bestimmten Dienstanbietern implementiert werden. Zum direkten Kontakt mit Adressbuchanbietern verwenden Clients Adressbuchcontainer, Messagingbenutzer und Verteilerlisten. Um direkt auf einen Nachrichtenspeicheranbieter zu zugreifen, verwenden Clients das Nachrichtenspeicherobjekt, Ordner, Nachrichten und Anlagen. Wenn Dienstanbieter ein Statusobjekt unterstützen, können Clients das Statusobjekt verwenden, um den Status des Dienstanbieters zu überwachen.
  
Clients, die die Dienstanbieter- und Nachrichtendienstkonfiguration unterstützen, verwenden drei Objekte, die MAPI implementiert: das Nachrichtendienstverwaltungsobjekt, das Profilverwaltungsobjekt und das Anbieterverwaltungsobjekt. Clients, die benutzerdefinierte Formulare anzeigen, verwenden mehrere Formularobjekte, die von einem Formularbibliotheksanbieter oder einem Formularserver implementiert werden.
  
## <a name="see-also"></a>Siehe auch

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

