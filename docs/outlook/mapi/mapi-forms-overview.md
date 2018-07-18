---
title: MAPI-Workflowformulare (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91bc0641723a92d8dc86bf3d1037d8e9936930ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793001"
---
# <a name="mapi-forms-overview"></a>MAPI-Workflowformulare (Übersicht)
  
**Betrifft**: Outlook 
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht. Jede Nachricht weist eine Nachrichtenklasse, die bestimmte Form durch die bestimmt, die als Viewer verwendet wird. MAPI definiert verschiedene Nachrichtenklassen und die Formulare für die Anzeige von Nachrichten dieser Klassen wurde implementiert. Client-Software-Entwicklern können neue Nachrichtenklassen und benutzerdefinierte Formulare für die Anzeige von Nachrichten mithilfe der neuen Klassen erstellt erstellen.
  
Jedes benutzerdefiniertes Formular implementiert eine Reihe von standard Menübefehle, z. B. **Open**, **Erstellen**, **Löschen**und **Antwort**, und eine Reihe von Befehlen, die auf das Formular spezifisch sind. Einige der Formularbefehle sind mit der Benutzeroberfläche der Client-Anwendung integriert, wenn das Formular aktiv ist. andere Formularbefehle ersetzt vollständig die Clientbefehle. 
  
Die folgende Abbildung zeigt die Beziehung zwischen den MAPI-Komponenten für die Verwendung von Formularen. 
  
**Architektur des MAPI-Formulars**
  
![MAPI-Formular-Architektur] (media/forms01.gif "MAPI-Formular-Architektur")
  
Beachten Sie, dass der Formular-Manager eine Rolle, die andere MAPI-Dienstanbieter ähnlich ist spielt, obwohl es keinem Dienstanbieter selbst ist, in das Diagramm. Der Formular-Manager ist eine austauschbare DLL, die einige MAPI-Schnittstellen implementiert. Obwohl Entwickler ihre eigenen Formular-Manager implementieren können, werden die meisten Umgebungen aufgrund der Komplexität der Formular-Manager von Microsoft bereitgestellten Formular-Manager verwenden.
  
Die folgende Liste beschreibt die Komponenten im Diagramm und deren Beziehung zu anderen Komponenten:
  
- Messaging-Client: eine Anwendung, die Formular-Objekte verwenden kann. Der messaging-Client verwendet die MAPI-Formular-Schnittstellen zur Kommunikation mit der Formular-Manager Nachrichten in Formularobjekte zu laden.
    
- MAPI-Formulars Schnittstellen: ein definierter Standard für die Kommunikation zwischen MAPI-Komponenten, die im Zusammenhang mit Formularen.
    
- Formular-Manager: der DLL, die messaging-Clients verwenden, um die Installation von Formularen in Formularbibliotheken, Laden des Formulars Servern und erste Kommunikation zwischen messaging-Clients und Servern Formular zu behandeln.
    
- Formular Bibliotheken: permanenten Speicher für die ausführbaren Dateien Formular Server zugeordnet.
    
- Server bilden: ausführbare Dateien, die einem Formular zu implementieren. Formular Servern Formular-Objekte und -Benutzeroberflächen für den Umgang mit bestimmter Nachrichten erstellen. Diese ausführbare Datei ist auch ein OLE-Server und den üblichen OLE-Konventionen befolgt.
    
- Objekte bilden: Laufzeitobjekte erstelltes Formular Server, die bestimmte Nachrichten entsprechen. Formular-Objekte werden in demselben Prozesskontext als Formular Server ausführen.
    
Weitere Informationen zu MAPI-Formularkomponenten finden Sie unter [MAPI-Formulare](mapi-forms.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und die Architektur](mapi-features-and-architecture.md)

