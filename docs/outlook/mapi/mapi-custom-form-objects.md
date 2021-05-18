---
title: BEnutzerdefinierte MAPI-Formularobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318246"
---
# <a name="mapi-custom-form-objects"></a>BEnutzerdefinierte MAPI-Formularobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Objekte für benutzerdefinierte Formulare werden von drei verschiedenen Komponenten implementiert:
  
- Ein Formularserver.
    
- Ein Formularbibliotheksanbieter.
    
- Ein Formularanzeiger.
    
Ein Formularserver ähnelt in der Funktionalität einer OLE-Zusammengesetztdokumentobjektanwendung. Es handelt sich um eine ausführbare Komponente, die das Formular implementiert. Sie steuert die Anzeige und die Vorgänge, die ein Benutzer ausführen kann. MAPI startet einen Formularserver auf Anforderung, wenn ein Benutzer eine Nachricht zusammen mit einer Nachrichtenklasse anzeigen möchte, die mithilfe eines vom Formularserver unterstützten Formulars angezeigt wird. Formularserver implementieren drei Objekte: ein Formular factory-Objekt, das der standardmäßigen OLE-Klassen factory ähnelt, eine Formularsenke zur Behandlung formularspezifischer Ereignisse und das Formular selbst. 
  
Ein Formularbibliotheksanbieter bietet Clients Zugriff auf den Eigenschaftensatz eines Formulars, den Container und das Objekt, das Nachrichten einer bestimmten Klasse mit dem Server verbindet, der das Formular für diese Klasse öffnen kann. Formularbibliotheksanbieter implementieren drei Objekte: ein Formularinformationsobjekt, einen Formularcontainer und einen Formular-Manager zum Binden einer Nachricht an den entsprechenden Formularserver basierend auf der Klasse der Nachricht.
  
Eine Formularanzeige ist eine Komponente, die in Clients enthalten ist, die die Anzeige benutzerdefinierter Formulare in ihren Ordneranzeigen unterstützen. Formularanzeigen sind keine unabhängigen MAPI-Komponenten, ebenso wie Formularbibliotheksanbieter und Formularserver. Formularbetrachter starten Formularserver und stellen kontextbezogene Informationen zur Verfügung. Formularbetrachter implementieren drei Objekte: eine Nachrichtenwebsite, einen Ansichtskontext und eine Ratensenke für die Behandlung von ansichtsspezifischen Ereignissen.
  
In der folgenden Tabelle werden alle benutzerdefinierten Formularobjekte beschrieben. 
  
|**Form-Objekt**|**Beschreibung**|
|:-----|:-----|
|Formular  <br/> |Steuert die Anzeige und den Betrieb eines benutzerdefinierten Formulars zum Anzeigen von Nachrichten einer bestimmten Klasse.  <br/> |
|Formular-Rat-Senke  <br/> |Verarbeitet Benachrichtigungen aus der Formularanzeige.  <br/> |
|Formular factory  <br/> |Erstellt eine Instanz eines Formulars und lässt den Server im Arbeitsspeicher verbleiben.  <br/> |
|Formularcontainer  <br/> |Enthält Formularinformationen.  <br/> |
|Formularinformationen  <br/> |Enthält Nachrichten und andere Nachrichtencontainer.  <br/> |
|Formularmanager  <br/> |Bietet Zugriff auf eine integrierte Ansicht von benutzerdefinierten Formularinformationen, die sich auf alle installierten Formulare bezogen. Entspricht auch Nachrichtenklassen mit entsprechenden Formularklassenbezeichnern.  <br/> |
|Nachrichtenwebsite  <br/> |Behandelt die Bearbeitung von Formularobjekten innerhalb des Clients und bietet Zugriff auf ein Formular-Manager-Objekt.  <br/> |
|Kontext anzeigen  <br/> |Unterstützt Formularbefehle zum Aktivieren nächster und vorheriger Nachrichten sowie zum Speichern oder Drucken.  <br/> |
|Anzeigen der Ratensenke  <br/> |Verarbeitet Benachrichtigungen vom Formularserver.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen benutzerdefinierten Formularkomponenten, den implementierten Objekten und Schnittstellen und den Komponenten, die Benutzer der Objekte sind. Beachten Sie, dass das Formularobjekt im Gegensatz zu den meisten anderen MAPI-Objekten zwei Schnittstellen implementiert, die nicht durch direkte Vererbung verbunden sind. Wenn ein Objekt mehrere unabhängige Schnittstellen verfügbar macht, kann ein Benutzer des Objekts mit einem Zeiger auf eine der Schnittstellen einen Zeiger auf eine der anderen Schnittstellen abrufen. Diese Möglichkeit, zwischen den Schnittstellenimplementierung eines Objekts zu navigieren, ist ein Feature der [IUnknown::QueryInterface-Methode.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) 
  
**Benutzerdefinierte Formularkomponenten**
  
![Benutzerdefinierte Formularkomponenten](media/amapi_67.gif "Benutzerdefinierte Formularkomponenten")
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

