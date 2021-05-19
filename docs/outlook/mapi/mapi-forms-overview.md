---
title: Übersicht über MAPI-Formulare
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432520"
---
# <a name="mapi-forms-overview"></a>Übersicht über MAPI-Formulare
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht. Jede Nachricht verfügt über eine Nachrichtenklasse, die das bestimmte Formular bestimmt, das als Viewer verwendet wird. MAPI definiert mehrere Nachrichtenklassen und hat die Formulare zum Anzeigen von Nachrichten dieser Klassen implementiert. Clientsoftwareentwickler können neue Nachrichtenklassen und benutzerdefinierte Formulare zum Anzeigen von Nachrichten erstellen, die mithilfe der neuen Klassen erstellt wurden.
  
Jedes benutzerdefinierte Formular implementiert eine Reihe von Standardmenübefehlen, z. B. **Öffnen**, **Erstellen**, **Löschen** und **Antworten**, und eine Reihe von Befehlen, die für das bestimmte Formular spezifisch sind. Einige der Formularbefehle sind in die Benutzeroberfläche der Clientanwendung integriert, wenn das Formular aktiv ist. Andere Formularbefehle ersetzen die Clientbefehle vollständig. 
  
Die folgende Abbildung zeigt die Beziehung zwischen den MAPI-Komponenten, die an der Verwendung von Formularen beteiligt sind. 
  
**Architektur des MAPI-Formulars**
  
![MAPI-Formulararchitektur](media/forms01.gif "MAPI-Formulararchitektur")
  
Beachten Sie im Diagramm, dass der Formular-Manager eine Rolle spielt, die anderen MAPI-Dienstanbietern ähnelt, obwohl er selbst kein Dienstanbieter ist. Der Formular-Manager ist eine austauschbare DLL, die einige der MAPI-Schnittstellen implementiert. Obwohl Entwickler einen eigenen Formular-Manager implementieren können, verwenden die meisten Umgebungen aufgrund der Komplexität des Formular-Managers den von Microsoft bereitgestellten Formular-Manager.
  
In der folgenden Liste werden die Komponenten im Diagramm und deren Beziehung zu anderen Komponenten beschrieben:
  
- Messagingclient: Eine Anwendung, die Formularobjekte verwenden kann. Der Messagingclient verwendet die MAPI-Formularschnittstellen, um mit dem Formular-Manager zu kommunizieren, um Nachrichten in Formularobjekte zu laden.
    
- MAPI-Formularschnittstellen: Ein definierter Standard für die Kommunikation zwischen MAPI-Komponenten, die sich auf Formulare bezogen haben.
    
- Formular-Manager: Die DLL, mit der Messagingclients die Installation von Formularen in Formularbibliotheken, das Laden von Formularservern und die anfängliche Kommunikation zwischen Messagingclients und Formularservern verarbeiten.
    
- Formularbibliotheken: Permanenter Speicher für die ausführbaren Dateien, die Formularservern zugeordnet sind.
    
- Formularserver: Ausführbare Dateien, die ein Formular implementieren. Formularserver erstellen Formularobjekte und Benutzeroberflächen für den Umgang mit bestimmten Nachrichten. Diese ausführbare Datei ist auch ein OLE-Server und hält die üblichen OLE-Konventionen ein.
    
- Form-Objekte: Laufzeitobjekte, die von Formularservern erstellt werden, die bestimmten Nachrichten entsprechen. Formularobjekte werden im gleichen Prozesskontext wie ihr Formularserver ausgeführt.
    
Weitere Informationen zu MAPI-Formularkomponenten finden Sie unter [MAPI Forms](mapi-forms.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

