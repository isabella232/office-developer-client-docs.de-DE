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
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht. Jede Nachricht verfügt über eine Nachrichtenklasse, die das jeweilige Formular bestimmt, das als Viewer verwendet wird. MAPI definiert mehrere Nachrichtenklassen und hat die Formulare zum Anzeigen von Nachrichten dieser Klassen implementiert. Client Softwareentwickler können neue Nachrichtenklassen und benutzerdefinierte Formulare zum Anzeigen von Nachrichten erstellen, die mithilfe der neuen Klassen erstellt wurden.
  
Jedes benutzerdefinierte Formular implementiert eine Reihe von Standardmenü Befehlen wie **Open**, **Create**, **Delete**und **Reply**sowie eine Reihe von Befehlen, die spezifisch für das jeweilige Formular sind. Einige der Formularbefehle sind in die Benutzeroberfläche der Clientanwendung integriert, wenn das Formular aktiv ist. andere Formularbefehle ersetzen die Clientbefehle vollständig. 
  
In der folgenden Abbildung wird die Beziehung zwischen den MAPI-Komponenten dargestellt, die mit Formularen verwendet werden. 
  
**Architektur des MAPI-Formulars**
  
![MAPI-Formulararchitektur] (media/forms01.gif "MAPI-Formulararchitektur")
  
Beachten Sie im Diagramm, dass der Formular-Manager eine Rolle spielt, die anderen MAPI-Dienstanbietern ähnelt, obwohl es sich nicht um einen Dienstanbieter handelt. Der Formular-Manager ist eine austauschbare DLL, die einige der MAPI-Schnittstellen implementiert. Obwohl Entwickler ihren eigenen Formular-Manager implementieren können, verwenden die meisten Umgebungen den von Microsoft bereitgestellten Formular-Manager aufgrund der Komplexität des Formular-Managers.
  
In der folgenden Liste werden die Komponenten im Diagramm und ihre Beziehung zu anderen Komponenten beschrieben:
  
- Messaging Client: eine Anwendung, die Formularobjekte verwenden kann. Der Messaging Client verwendet die MAPI-Formular Schnittstellen für die Kommunikation mit dem Formular-Manager, um Nachrichten in Formularobjekte zu laden.
    
- MAPI-Formular Schnittstellen: ein definierter Standard für die Kommunikation zwischen MAPI-Komponenten, die sich auf Formulare beziehen.
    
- Formular-Manager: die DLL, die Messaging-Clients verwenden, um die Installation von Formularen in Formularbibliotheken, das Laden von Formular Servern und die anfängliche Kommunikation zwischen Messagingclients und Formular Servern zu behandeln.
    
- Formularbibliotheken: permanenter Speicher für die den Formular Servern zugeordneten ausführbaren Dateien.
    
- Formularserver: ausführbare Dateien, die ein Formular implementieren. Formularserver erstellen Formularobjekte und Benutzeroberflächen für die Behandlung bestimmter Nachrichten. Diese ausführbare Datei ist auch ein OLE-Server und entspricht den üblichen OLE-Konventionen.
    
- Formularobjekte: von Formular Servern erstellte Laufzeitobjekte, die bestimmten Nachrichten entsprechen. Formularobjekte werden im gleichen Prozesskontext wie der Formularserver ausgeführt.
    
Weitere Informationen zu MAPI-Formularkomponenten finden Sie unter [MAPI Forms](mapi-forms.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

