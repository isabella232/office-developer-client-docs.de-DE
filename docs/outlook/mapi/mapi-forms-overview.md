---
title: Übersicht über MAPI-Formulare
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c2c47bd25c0ddd05d6a0c518af37763803724e98
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595868"
---
# <a name="mapi-forms-overview"></a>Übersicht über MAPI-Formulare
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht. Jede Nachricht verfügt über eine Nachrichtenklasse, die das bestimmte Formular bestimmt, das als Viewer verwendet wird. MAPI definiert mehrere Nachrichtenklassen und hat die Formulare zum Anzeigen von Nachrichten dieser Klassen implementiert. Clientsoftwareentwickler können neue Nachrichtenklassen und benutzerdefinierte Formulare zum Anzeigen von Nachrichten erstellen, die mithilfe der neuen Klassen erstellt wurden.
  
Jedes benutzerdefinierte Formular implementiert eine Reihe von Standardmenübefehlen wie **"Öffnen",** **"Erstellen",** **"Löschen"** und **"Antworten"** sowie eine Reihe von Befehlen, die für das jeweilige Formular spezifisch sind. Einige der Formularbefehle sind in die Benutzeroberfläche der Clientanwendung integriert, wenn das Formular aktiv ist. Andere Formularbefehle ersetzen die Clientbefehle vollständig. 
  
Die folgende Abbildung zeigt die Beziehung zwischen den MAPI-Komponenten, die an der Verwendung von Formularen beteiligt sind. 
  
**Architektur des MAPI-Formulars**
  
![Architektur des MAPI-Formulars](media/forms01.gif "Architektur des MAPI-Formulars")
  
Beachten Sie im Diagramm, dass der Formular-Manager eine Rolle spielt, die anderen MAPI-Dienstanbietern ähnelt, obwohl er selbst kein Dienstanbieter ist. Der Formular-Manager ist eine austauschbare DLL, die einige der MAPI-Schnittstellen implementiert. Obwohl Entwickler ihren eigenen Formular-Manager implementieren können, verwenden die meisten Umgebungen den von Microsoft bereitgestellten Formular-Manager aufgrund der Komplexität des Formular-Managers.
  
In der folgenden Liste werden die Komponenten im Diagramm und ihre Beziehung zu anderen Komponenten beschrieben:
  
- Messagingclient: Eine Anwendung, die Formularobjekte verwenden kann. Der Messagingclient verwendet die MAPI-Formularschnittstellen, um mit dem Formular-Manager zu kommunizieren, um Nachrichten in Formularobjekte zu laden.
    
- MAPI-Formularschnittstellen: Ein definierter Standard für die Kommunikation zwischen MAPI-Komponenten im Zusammenhang mit Formularen.
    
- Formular-Manager: Die DLL, die Messagingclients verwenden, um die Installation von Formularen in Formularbibliotheken, das Laden von Formularservern und die anfängliche Kommunikation zwischen Messagingclients und Formularservern zu verarbeiten.
    
- Formularbibliotheken: Dauerhafter Speicher für die ausführbaren Dateien, die Formularservern zugeordnet sind.
    
- Formularserver: Ausführbare Dateien, die ein Formular implementieren. Formularserver erstellen Formularobjekte und Benutzeroberflächen für bestimmte Nachrichten. Diese ausführbare Datei ist auch ein OLE-Server und entspricht den üblichen OLE-Konventionen.
    
- Formularobjekte: Laufzeitobjekte, die von Formularservern erstellt wurden, die bestimmten Nachrichten entsprechen. Formularobjekte werden im gleichen Prozesskontext wie ihr Formularserver ausgeführt.
    
Weitere Informationen zu MAPI-Formularkomponenten finden Sie unter [MAPI Forms](mapi-forms.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

