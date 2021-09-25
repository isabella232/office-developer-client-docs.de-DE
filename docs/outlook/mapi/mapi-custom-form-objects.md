---
title: Benutzerdefinierte MAPI-Formularobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff73842326134c0e9a7a3e5a98bd0cee9a4c042c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595882"
---
# <a name="mapi-custom-form-objects"></a>Benutzerdefinierte MAPI-Formularobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Objekte für benutzerdefinierte Formulare werden von drei verschiedenen Komponenten implementiert:
  
- Ein Formularserver.
    
- Ein Formularbibliotheksanbieter.
    
- Eine Formularanzeige.
    
Ein Formularserver ähnelt in seiner Funktionalität einer OLE-Verbunddokumentobjektanwendung. Es handelt sich um eine ausführbare Komponente, die das Formular implementiert. Es steuert die Anzeige und die Vorgänge, die ein Benutzer ausführen kann. MAPI startet einen Formularserver auf Anforderung, wenn ein Benutzer eine Nachricht zusammen mit einer Nachrichtenklasse anzeigen möchte, die mithilfe eines vom Formularserver unterstützten Formulars angezeigt wird. Formularserver implementieren drei Objekte: ein Formularfactoryobjekt, das der Standardfactory der OLE-Klasse ähnelt, eine Formular-Empfehlungssenke für die Behandlung formularspezifischer Ereignisse und das Formular selbst. 
  
Ein Formularbibliotheksanbieter stellt Clients Zugriff auf den Eigenschaftensatz eines Formulars, seinen Container und das Objekt bereit, das Nachrichten einer bestimmten Klasse mit dem Server verknüpft, der das Formular für diese Klasse öffnen kann. Formularbibliotheksanbieter implementieren drei Objekte: ein Formularinformationsobjekt, einen Formularcontainer und einen Formular-Manager zum Binden einer Nachricht an den entsprechenden Formularserver basierend auf der Klasse der Nachricht.
  
Eine Formularanzeige ist eine Komponente, die in Clients enthalten ist, die die Anzeige von benutzerdefinierten Formularen in ihren Ordneranzeigen unterstützen. Formularviewer sind keine unabhängigen MAPI-Komponenten, ebenso wie Formularbibliotheksanbieter und Formularserver. Formularviewer starten Formularserver und stellen Kontext für sie bereit. Formularviewer implementieren drei Objekte: eine Nachrichtenwebsite, einen Ansichtskontext und eine Empfehlungssenke für die Behandlung ansichtsspezifischer Ereignisse.
  
In der folgenden Tabelle werden alle benutzerdefinierten Formularobjekte beschrieben. 
  
|**Form-Objekt**|**Beschreibung**|
|:-----|:-----|
|Formular  <br/> |Steuert die Anzeige und den Betrieb eines benutzerdefinierten Formulars zum Anzeigen von Nachrichten einer bestimmten Klasse.  <br/> |
|Formular-Empfehlungssenke  <br/> |Behandelt Benachrichtigungen aus der Formularanzeige.  <br/> |
|Formularfactory  <br/> |Erstellt eine Instanz eines Formulars und lässt zu, dass der Server im Arbeitsspeicher bleibt.  <br/> |
|Formularcontainer  <br/> |Enthält Formularinformationen.  <br/> |
|Formularinformationen  <br/> |Enthält Nachrichten und andere Nachrichtencontainer.  <br/> |
|Formularmanager  <br/> |Bietet Zugriff auf eine integrierte Ansicht von benutzerdefinierten Formularinformationen, die sich auf alle installierten Formulare beziehen. Gleicht nachrichtenklassen auch mit den entsprechenden Formularklassenbezeichnern ab.  <br/> |
|Nachrichtenwebsite  <br/> |Behandelt die Bearbeitung von Formularobjekten innerhalb des Clients und ermöglicht den Zugriff auf ein Formular-Manager-Objekt.  <br/> |
|Kontext anzeigen  <br/> |Unterstützt Formularbefehle zum Aktivieren von nächsten und vorherigen Nachrichten und zum Speichern oder Drucken.  <br/> |
|Anzeigen einer Empfehlungssenke  <br/> |Behandelt Benachrichtigungen vom Formularserver.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen benutzerdefinierten Formularkomponenten, den von ihnen implementierten Objekten und Schnittstellen und den Komponenten, die Benutzer der Objekte sind. Beachten Sie, dass das Formularobjekt im Gegensatz zu den meisten anderen MAPI-Objekten zwei Schnittstellen implementiert, die nicht mit der direkten Vererbung zusammenhängen. Wenn ein Objekt mehrere unabhängige Schnittstellen verfügbar macht, kann ein Benutzer des Objekts, das über einen Zeiger auf eine der Schnittstellen verfügt, einen Zeiger auf eine der anderen Schnittstellen abrufen. Diese Möglichkeit zum Navigieren zwischen den Schnittstellenimplementierungen eines Objekts ist ein Feature der [IUnknown::QueryInterface-Methode.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) 
  
**Benutzerdefinierte Formularkomponenten**
  
![Benutzerdefinierte Formularkomponenten](media/amapi_67.gif "Benutzerdefinierte Formularkomponenten")
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

