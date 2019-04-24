---
title: MAPI-benutzerdefinierte Formularobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318246"
---
# <a name="mapi-custom-form-objects"></a>MAPI-benutzerdefinierte Formularobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Objekte für benutzerdefinierte Formulare werden von drei verschiedenen Komponenten implementiert:
  
- Ein Formularserver.
    
- Ein Anbieter für Formularbibliotheken.
    
- Ein Formular-Viewer.
    
Ein Formularserver ähnelt der Funktionalität einer OLE-Verbund-Dokumentobjekt Anwendung. Es handelt sich um eine ausführbare Komponente, die das Formular implementiert; Sie steuert die Anzeige und die Vorgänge, die ein Benutzer ausführen kann. MAPI startet einen Formularserver auf Anforderung, wenn ein Benutzer eine Nachricht zusammen mit einer Nachrichtenklasse anzeigen möchte, die mithilfe eines vom Formularserver unterstützten Formulars angezeigt wird. Formularserver implementieren drei Objekte: ein Form Factory-Objekt, das der standardmäßigen OLE-Klassen Factory ähnelt, eine Form Advise-Senke zur Behandlung von formularspezifischen Ereignissen und das Formular selbst. 
  
Ein Formularbibliothek Anbieter stellt den Zugriff für Clients auf den Eigenschaftensatz eines Formulars, seinen Container und das Objekt bereit, das Nachrichten einer bestimmten Klasse mit dem Server verknüpft, der das Formular für diese Klasse öffnen kann. Formular Bibliotheks Anbieter implementieren drei Objekte: ein Formular Informationsobjekt, einen Formular Container und einen Formular-Manager zum Binden einer Nachricht an den entsprechenden Formularserver auf der Grundlage der Nachrichtenklasse.
  
Ein Formular Betrachter ist eine Komponente, die in Clients enthalten ist, die die Anzeige von benutzerdefinierten Formularen in Ihren Ordner Viewern unterstützen. Formular Betrachter sind keine unabhängigen MAPI-Komponenten, ebenso wie Formular Bibliotheks Anbieter und Formularserver. Formular Betrachter starten Formularserver und bieten Kontext für diese. Formular Betrachter implementieren drei Objekte: eine Nachrichtenwebsite, einen Ansichtskontext und eine Advise-Senke für die Verarbeitung von ansichtsspezifischen Ereignissen.
  
In der folgenden Tabelle werden alle benutzerdefinierten Formularobjekte beschrieben. 
  
|**Form-Objekt**|**Beschreibung**|
|:-----|:-----|
|Formular  <br/> |Steuert die Anzeige und den Betrieb eines benutzerdefinierten Formulars zum Anzeigen von Nachrichten einer bestimmten Klasse.  <br/> |
|Formular Advise-Senke  <br/> |Behandelt Benachrichtigungen im Formular-Viewer.  <br/> |
|Formular Factory  <br/> |Erstellt eine Instanz eines Formulars und ermöglicht, dass der Server im Arbeitsspeicher verbleibt.  <br/> |
|Formular Container  <br/> |Enthält Formular Informationen.  <br/> |
|Formular Informationen  <br/> |Enthält Nachrichten und andere Nachrichtencontainer.  <br/> |
|Formularmanager  <br/> |Ermöglicht den Zugriff auf eine integrierte Ansicht von benutzerdefinierten Formular Informationen, die sich auf alle installierten Formulare beziehen. Vergleicht auch Nachrichtenklassen mit entsprechenden Formularklassen Bezeichnern.  <br/> |
|Nachrichtenwebsite  <br/> |Behandelt die Bearbeitung von Formularobjekten innerhalb des Clients und ermöglicht den Zugriff auf ein Formular-Manager-Objekt.  <br/> |
|Ansichtskontext  <br/> |Unterstützt Formularbefehle zum Aktivieren von nächsten und vorherigen Nachrichten sowie zum Speichern oder drucken.  <br/> |
|Anzeigen der Advise-Senke  <br/> |Behandelt Benachrichtigungen vom Formularserver.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen benutzerdefinierten Formularkomponenten, die Objekte und Schnittstellen, die Sie implementieren, und die Komponenten, die Benutzer der Objekte sind. Beachten Sie, dass im Gegensatz zu den meisten anderen MAPI-Objekten das Form-Objekt zwei Schnittstellen implementiert, die nicht durch direkte Vererbung verbunden sind. Wenn ein Objekt mehrere unabhängige Schnittstellen verfügbar macht, kann ein Benutzer des Objekts, das über einen Zeiger auf eine der Schnittstellen verfügt, einen Zeiger auf eine beliebige andere Schnittstelle abrufen. Diese Fähigkeit, zwischen den Schnittstellenimplementierungen eines Objekts zu navigieren, ist ein Feature der [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode. 
  
**Benutzerdefinierte Formularkomponenten**
  
![Benutzerdefinierte Formularkomponenten] (media/amapi_67.gif "Benutzerdefinierte Formularkomponenten")
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

