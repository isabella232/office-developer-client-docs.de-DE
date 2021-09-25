---
title: Behandeln von MAPI-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 05a1f1b61a8958bc2a32eb31988318cf43a8541b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580167"
---
# <a name="handling-mapi-forms"></a>Behandeln von MAPI-Formularen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht einer bestimmten Klasse. Clients, die es ihren Benutzern ermöglichen, mit Nachrichten zu arbeiten, die zu einer Vielzahl von Nachrichtenklassen gehören, müssen geschrieben werden, um eine Vielzahl von MAPI-Formularen zu verarbeiten. Um mehrere Formulare zu verarbeiten, implementieren Clients eine Komponente, die als Formularanzeige bezeichnet wird und die folgenden drei Objekte enthält:
  
- Ein Nachrichtenwebsiteobjekt, das die [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) unterstützt. 
    
- Eine Ansichts-Empfehlungssenke, die die [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) unterstützt. 
    
- Ein Ansichtskontextobjekt, das die [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) unterstützt. 
    
Jedes dieser Objekte wird von einer Komponente verwendet, die als Formularserver bezeichnet wird, die jedes Formular implementiert, dessen Speicher und die Benachrichtigungen behandeln, die von Clients generiert werden, die die Ansicht behandeln. Eine andere Komponente, der Formularbibliotheksanbieter, implementiert einen Formular-Manager. Der Formular-Manager verwaltet die Formularbibliotheken, in denen ausführbare Dateien des Formularservers gespeichert werden. Diese Verwaltung umfasst das Laden des entsprechenden Formularservers und die Behandlung der anfänglichen Kommunikation zwischen dem Server und dem Client.
  
Das folgende Diagramm zeigt die Beziehung zwischen einem Client und den anderen Teilen der MAPI-Formulararchitektur.
  
## <a name="mapi-form-architecture"></a>Architektur des MAPI-Formulars
  
![Architektur des MAPI-Formulars](media/forms01.gif "Architektur des MAPI-Formulars")
  
Wenn Ihr Client die Verarbeitung von MAPI-Formularen plant, verwenden Sie die [IMAPIFormMgr : IUnknown-Schnittstelle](imapiformmgriunknown.md) des Formular-Managers, um fünf grundlegende Aufgaben auszuführen: 
  
- Starten Sie den entsprechenden MAPI-Formularserver, wenn eine Nachricht geöffnet oder verfasst wird.
    
- Zeigt die Symbole von Formularservern in den Inhaltsverzeichnissen von Ordnern an.
    
- Senden und Empfangen von Formularbenachrichtigungen. Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md)
    
- Benutzern das Installieren oder Entfernen von Formularservern aus Formularbibliotheken gestatten. Weitere Informationen finden Sie unter [Verwalten einer Formularbibliothek.](maintaining-a-form-library.md)
    
- Zulassen, dass Benutzer Formularserver bestimmten Ordnern zuordnen können.
    
Um auf den Formular-Manager zuzugreifen, rufen Sie die [MAPIOpenFormMgr-Funktion](mapiopenformmgr.md) einmal während der Initialisierung auf. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Implementieren einer Formularanzeige:](implementing-a-form-viewer.md)Beschreibt, wie eine Formularanzeige mithilfe einer Ansichts-Empfehlungssenke, einer Nachrichtenwebsite und eines Ansichtskontexts implementiert wird.
    
- [Implementieren von Standardformularverben:](implementing-standard-form-verbs.md)Beschreibt, wie die Verben für Benutzermenü- oder Schaltflächenklicks auf MAPI-Formulare implementiert werden.
    
- [Senden und Empfangen von Formularbenachrichtigungen:](sending-and-receiving-form-notifications.md)Beschreibt, wie Formularbenachrichtigungen gesendet und empfangen werden.
    
- [Verwalten einer Formularbibliothek:](maintaining-a-form-library.md)Beschreibt, wie eine Bibliothek verwaltet wird, die alle wichtigen Informationen zu einem Formular enthält.
    
- [Laden einer Nachricht in ein Formular:](loading-a-message-into-a-form.md)Beschreibt, wie eine Nachricht in ein Formular geladen wird.
    
- [Erstellen einer neuen Nachricht mithilfe eines Formulars:](composing-a-new-message-by-using-a-form.md)Beschreibt, wie eine Nachricht mithilfe eines Formulars erstellt wird.
    
- [Anzeigen von Formularsymbolen:](displaying-form-icons.md)Beschreibt die Schritte zum Anzeigen eines Symbols mit einem Formular.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)
- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

