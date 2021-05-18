---
title: Behandeln von MAPI-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91347f0c34b8d7b76e4e456397a1faa061f3b2c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423055"
---
# <a name="handling-mapi-forms"></a>Behandeln von MAPI-Formularen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht einer bestimmten Klasse. Clients, die benutzern die Arbeit mit Nachrichten ermöglichen, die zu einer Vielzahl von Nachrichtenklassen gehören, müssen für die Verarbeitung einer Vielzahl von MAPI-Formularen geschrieben werden. Um mehrere Formulare zu verarbeiten, implementieren Clients eine Komponente, die als Formularanzeige bekannt ist und die die folgenden drei Objekte enthält:
  
- Ein Nachrichtenwebsiteobjekt, das die [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) unterstützt. 
    
- Eine Ansichtssenke, die die [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) unterstützt. 
    
- Ein Ansichtskontextobjekt, das die [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) unterstützt. 
    
Jedes dieser Objekte wird von einer Komponente namens Formularserver verwendet, die jedes Formular implementiert, dessen Speicher und die von Clients generierten Benachrichtigungen behandeln, die die Ansicht behandeln. Eine andere Komponente, der Formularbibliotheksanbieter, implementiert einen Formular-Manager. Der Formular-Manager verwaltet die Formularbibliotheken, in denen ausführbare Dateien des Formularservers gespeichert werden. Diese Verwaltung umfasst das Laden des entsprechenden Formularservers und die Verarbeitung der anfänglichen Kommunikation zwischen dem Server und dem Client.
  
Das folgende Diagramm zeigt die Beziehung zwischen einem Client und den anderen Teilen der MAPI-Formulararchitektur.
  
## <a name="mapi-form-architecture"></a>Architektur des MAPI-Formulars
  
![MAPI-Formulararchitektur](media/forms01.gif "MAPI-Formulararchitektur")
  
Wenn Ihr Client die Verarbeitung von MAPI-Formularen plant, verwenden Sie die [IMAPIFormMgr : IUnknown-Schnittstelle](imapiformmgriunknown.md) des Formular-Managers, um fünf grundlegende Aufgaben auszuführen: 
  
- Starten Sie den entsprechenden MAPI-Formularserver, wenn eine Nachricht geöffnet oder zusammengesetzt wird.
    
- Zeigen Sie die Symbole von Formularservern in den Inhaltsverzeichnissen von Ordnern an.
    
- Senden und Empfangen von Formularbenachrichtigungen. Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).
    
- Zulassen, dass Benutzer Formularserver aus Formularbibliotheken installieren oder entfernen. Weitere Informationen finden Sie unter [Verwalten einer Formularbibliothek](maintaining-a-form-library.md).
    
- Zulassen, dass Benutzer Formularserver bestimmten Ordnern zuordnen.
    
Rufen Sie die [MAPIOpenFormMgr-Funktion einmal](mapiopenformmgr.md) während der Initialisierung auf, um auf den Formular-Manager zu zugreifen. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Implementieren einer Formularanzeige:](implementing-a-form-viewer.md)Beschreibt, wie Sie eine Formularanzeige mithilfe einer Ansichtssenke, einer Nachrichtenwebsite und einem Ansichtskontext implementieren.
    
- [Implementieren von Standardformularverben:](implementing-standard-form-verbs.md)Beschreibt die Implementierung der Verben für Benutzermenü- oder Schaltflächenklicks auf MAPI-Formulare.
    
- [Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md): Beschreibt das Senden und Empfangen von Formularbenachrichtigungen.
    
- [Verwalten einer Formularbibliothek:](maintaining-a-form-library.md)Beschreibt, wie Sie eine Bibliothek verwalten, die alle wichtigen Informationen zu einem Formular enthält.
    
- [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md): Beschreibt, wie eine Nachricht in ein Formular geladen wird.
    
- [Verfassen einer neuen Nachricht mithilfe eines Formulars](composing-a-new-message-by-using-a-form.md): Beschreibt, wie eine Nachricht mithilfe eines Formulars verfasst wird.
    
- [Anzeigen von Formularsymbolen:](displaying-form-icons.md)Beschreibt die Schritte zum Anzeigen eines Symbols mit einem Formular.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)
- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

