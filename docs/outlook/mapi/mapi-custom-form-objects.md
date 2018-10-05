---
title: MAPI-benutzerdefiniertes Formularobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396323"
---
# <a name="mapi-custom-form-objects"></a>MAPI-benutzerdefiniertes Formularobjekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Objekte für benutzerdefinierte Formulare werden durch drei Komponenten implementiert:
  
- Ein Formular Server.
    
- Ein Formular Bibliotheksanbieter.
    
- Ein Formular Viewer.
    
Ein Formular Server ist Funktionalität ähnelt einer OLE zusammengesetzter Document-Objekt-Anwendung. Es ist eine ausführbare Komponente, die das Formular implementiert wird. Sie steuert die Anzeige und die Vorgänge, die ein Benutzer ausführen können. MAPI wird ein Formular Server auf Anfrage, wenn ein Benutzer möchte, eine Nachricht zusammen mit einer Nachrichtenklasse anzuzeigen, die angezeigt wird, mithilfe eines Formulars, die vom Formular Server unterstützt. Implementieren Sie Formular drei Objekte: ein Form-Factory-Objekt, das das standardmäßige OLE ähnelt class Factory, ein Formular advise-Empfänger für die Verarbeitung von Formular-Ereignisse und das Formular selbst. 
  
Ein Formular Bibliotheksanbieter stellt Zugriff für Clients, die auf einem Formular zugrunde Eigenschaftensatz, mit seinem Container und auf das Objekt, das Nachrichten von einer bestimmten Klasse mit dem Server verknüpft, die das Formular für diese Klasse öffnen können. Formular Bibliothek Anbieter implementieren drei Objekte: ein Form-Informationsobjekt, ein Formular Container und ein Formular-Manager zum Binden einer Nachricht an den entsprechenden Formular Server basierend auf der Message-Klasse.
  
Ein Formular Viewer ist eine Komponente, die in Clients enthalten ist, die die Anzeige von benutzerdefinierten Formularen in ihren Ordner Viewer unterstützen. Formular Viewer sind nicht unabhängig MAPI-Komponenten wie Formular Bibliothek Anbieter und Formular Server sind. Formular Viewer Formular Servern starten und Kontext für diese bereitzustellen. Formular Viewer drei Objekte implementieren: eine Nachricht-Website, ein Ansichtskontext und einer Advise-Empfänger für die Ereignisbehandlung ansichtsspezifische.
  
Die folgende Tabelle beschreibt alle benutzerdefinierten Formularobjekte. 
  
|**Form-Objekt**|**Beschreibung**|
|:-----|:-----|
|Formular  <br/> |Steuert die Anzeige und den Betrieb von einem benutzerdefinierten Formular zum Anzeigen von Nachrichten von einer bestimmten Klasse.  <br/> |
|Formular advise-Empfänger  <br/> |Benachrichtigungen über den Formular-Viewer behandelt.  <br/> |
|Formularbereichsfactory  <br/> |Erstellt eine Instanz eines Formulars und ermöglicht, dass den Server im Speicher verbleiben.  <br/> |
|Formular container  <br/> |Enthält Informationen für das Formular.  <br/> |
|Formularinformationen  <br/> |Nachrichten und andere Container Nachricht enthält.  <br/> |
|Formular-manager  <br/> |Bietet Zugriff auf eine integrierte Ansicht der benutzerdefinierten Formularinformationen, die alle installierten Formulare zugeordnet ist. Entspricht auch Nachrichtenklassen mit entsprechenden Formularklasse-Bezeichner.  <br/> |
|Nachricht-Website  <br/> |Ist für die Bearbeitung des Formular-Objekte innerhalb des Clients, und bietet Zugriff auf ein Formular-Manager-Objekt.  <br/> |
|Ansichtskontext  <br/> |Unterstützt bilden Befehle für die Aktivierung von vorherigen und nächsten Nachrichten und zum Speichern oder drucken.  <br/> |
|Ansicht advise-Empfänger  <br/> |Benachrichtigungen aus dem Formular Server behandelt.  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen benutzerdefinierte Formularkomponenten, die Objekte und Schnittstellen, die sie implementieren und die Komponenten, die Benutzer der Objekte sind. Beachten Sie, dass im Gegensatz zu den meisten anderen MAPI-Objekten, das Form-Objekt zwei Schnittstellen implementiert, die nicht über die direkte Vererbung verknüpft sind. Ein Objekt mehrere unabhängige Schnittstellen verfügbar macht, kann ein Benutzer, der das Objekt, das einen Zeiger auf eine der Schnittstellen hat einen Zeiger auf einer anderen Schnittstelle abrufen. Diese Möglichkeit zum Navigieren zwischen schnittstellenimplementierungen ein Objekt ist ein Feature von die [QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode. 
  
**Benutzerdefinierte Formularkomponenten**
  
![Benutzerdefinierte Formularkomponenten] (media/amapi_67.gif "Benutzerdefinierte Formularkomponenten")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

