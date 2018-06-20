---
title: Behandeln von MAPI-Formulare
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b0e54f78257eb6890e8afbb7941dc625dc79be0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791818"
---
# <a name="handling-mapi-forms"></a>Behandeln von MAPI-Formulare

**Betrifft**: Outlook 
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht einer bestimmten Klasse. Clients, mit denen die Benutzer zum Arbeiten mit Nachrichten, die mit einer Vielzahl von Nachrichtenklassen gehören müssen, eine Vielzahl von MAPI-Formulare behandeln geschrieben werden. Behandeln von mehreren Formularen implementieren Clients eine Komponente bekannt als Formular Viewer, der die folgenden drei Objekte enthält:
  
- Ein Meldungsobjekt Website, die unterstützt die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) Schnittstelle. 
    
- Eine Ansicht advise-Empfänger, die unterstützt die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) Schnittstelle. 
    
- Ein View-Kontext-Objekt, das unterstützt die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) Schnittstelle. 
    
Jedes dieser Objekte wird durch eine Komponente mit dem Namen des Formular-Servers, der jedes Formular, Verarbeitung der Speicherung und die Benachrichtigungen von Clients, die Verarbeitung der Ansicht generierte implementiert. Eine weitere Komponente, der Formular-Bibliothek-Anbieter implementiert wird, einen Formular-Manager. Der Formular-Manager verwaltet die Formularbibliotheken, die in der Form Server ausführbare Dateien speichern. Diese Verwaltung umfasst, laden den entsprechende Formular Server und zur Handhabung der ersten Kommunikation zwischen dem Server und dem Client.
  
Das folgende Diagramm zeigt die Beziehung zwischen einem Client und anderen Teilen der MAPI-Formular-Architektur.
  
## <a name="mapi-form-architecture"></a>Architektur des MAPI-Formulars
  
![MAPI-Formular-Architektur] (media/forms01.gif "MAPI-Formular-Architektur")
  
Wenn der Client plant, MAPI-Formulare zu behandeln, verwenden Sie des Formular-Managers [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) Schnittstelle fünf grundlegende Aufgaben ausführen: 
  
- Starten Sie den entsprechenden Server der MAPI-Formular aus, wenn eine Nachricht geöffnet oder erstellt wird.
    
- Formular-Servern Symbole in den Tabellen Inhalt von Ordnern anzeigen.
    
- Senden und Empfangen von Benachrichtigungen Formular. Weitere Informationen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
    
- Ermöglicht es Benutzern, die zum Installieren oder Entfernen von Servern Formular von Formularbibliotheken. Weitere Informationen finden Sie unter [Verwalten einer Formularbibliothek](maintaining-a-form-library.md).
    
- Ermöglicht es Benutzern, die bestimmte Ordner Formular Server zugeordnet.
    
Rufen Sie die [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion einmal während der Initialisierung, Zugriff auf den Formular-Manager. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Implementieren Sie ein Formular Viewer](implementing-a-form-viewer.md): Beschreibt, wie Sie einen Formular Viewer implementieren, indem Sie eine Ansicht advise-Empfänger einer Nachricht-Website und ein Ansichtskontext.
    
- [Implementieren von standardmäßigen Formular Verben](implementing-standard-form-verbs.md): Beschreibt, wie die Verben für Benutzer im Menü oder Schaltfläche klickt auf MAPI-Formularen zu implementieren.
    
- [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md): Beschreibt, wie Sie senden und Empfangen von Benachrichtigungen Formular.
    
- [Verwalten einer Formularbibliothek](maintaining-a-form-library.md): Beschreibt, wie Sie eine Dokumentbibliothek zu verwalten, die alle wichtige Informationen zu einem Formular enthält.
    
- [Laden Sie eine Nachricht in ein Formular](loading-a-message-into-a-form.md): Beschreibt, wie Sie eine Nachricht in einem Formular zu laden.
    
- [Verfassen einer neuen Nachricht mithilfe eines Formulars](composing-a-new-message-by-using-a-form.md): Beschreibt, wie Sie eine Nachricht mit einem Formular zum Verfassen.
    
- [Anzeigen von Form von Symbolen](displaying-form-icons.md): Beschreibt die Schritte zum Anzeigen eines Symbols mit einem Formular.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)
- [Entwickeln von MAPI-Formular-Servern](developing-mapi-form-servers.md)

