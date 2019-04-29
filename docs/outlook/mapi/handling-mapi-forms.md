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
  
Ein MAPI-Formular ist ein Viewer für eine Nachricht einer bestimmten Klasse. Clients, die es Ihren Benutzern ermöglichen, mit Nachrichten zu arbeiten, die zu einer Vielzahl von Nachrichtenklassen gehören, müssen geschrieben werden, um eine Vielzahl von MAPI-Formularen zu behandeln. Für die Verarbeitung mehrerer Formulare implementieren Clients eine Komponente, die als Formularanzeige bezeichnet wird und die folgenden drei Objekte enthält:
  
- Ein Nachrichten Site-Objekt, das die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle unterstützt. 
    
- Eine View Advise-Senke, die die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle unterstützt. 
    
- Ein View-Kontextobjekt, das die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) -Schnittstelle unterstützt. 
    
Jedes dieser Objekte wird von einer Komponente mit dem Namen "Form Server" verwendet, die jedes Formular implementiert, dessen Speicherung und die von Clients, die die Ansicht verarbeiten, generierten Benachrichtigungen. Eine andere Komponente, der Formularbibliothek Anbieter, implementiert einen Formular-Manager. Der Formular-Manager verwaltet die Formularbibliotheken, in denen ausführbare Formularserver Dateien gespeichert werden. Diese Verwaltung umfasst das Laden des entsprechenden Formular Servers und die Verarbeitung der anfänglichen Kommunikation zwischen dem Server und dem Client.
  
Das folgende Diagramm zeigt die Beziehung zwischen einem Client und den anderen Teilen der MAPI-Formulararchitektur.
  
## <a name="mapi-form-architecture"></a>Architektur des MAPI-Formulars
  
![MAPI-Formulararchitektur] (media/forms01.gif "MAPI-Formulararchitektur")
  
Wenn Ihr Client MAPI-Formulare verarbeiten möchte, verwenden Sie die [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) -Schnittstelle des Formular-Managers, um fünf grundlegende Aufgaben auszuführen: 
  
- Starten Sie den entsprechenden MAPI-Formularserver, wenn eine Nachricht geöffnet oder zusammengesetzt wird.
    
- Anzeigen der Symbole von Formular Servern in den Inhaltsverzeichnis Tabellen.
    
- Senden und empfangen von Formular Benachrichtigungen. Weitere Informationen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
    
- Ermöglicht Benutzern das Installieren oder Entfernen von Formular Servern aus Formularbibliotheken. Weitere Informationen finden Sie unter [Verwalten einer Formularbibliothek](maintaining-a-form-library.md).
    
- Zulassen, dass Benutzerformular Server bestimmten Ordnern zuordnen.
    
Um auf den Formular-Manager zuzugreifen, rufen Sie die [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion einmal während der Initialisierung auf. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Implementieren eines Formular](implementing-a-form-viewer.md)-Viewers: Beschreibt, wie ein Formular-Viewer mithilfe einer Ansicht Advise-Senke, einer Nachrichtenwebsite und eines Ansichts Kontexts implementiert wird.
    
- [Implementieren von Standard Verben für Formulare](implementing-standard-form-verbs.md): Beschreibt, wie Sie die Verben für Benutzermenü-oder Schaltflächenklicks auf MAPI-Formulare implementieren.
    
- [Senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md): Beschreibt das Senden und empfangen von Formular Benachrichtigungen.
    
- [Verwalten einer Formularbibliothek](maintaining-a-form-library.md): Beschreibt, wie Sie eine Bibliothek mit allen wichtigen Informationen zu einem Formular verwalten.
    
- [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md): Beschreibt, wie Sie eine Nachricht in ein Formular laden.
    
- [Verfassen einer neuen Nachricht mithilfe eines Formulars](composing-a-new-message-by-using-a-form.md): Beschreibt, wie Sie eine Nachricht mithilfe eines Formulars verfassen.
    
- [Anzeigen von Formular Symbolen](displaying-form-icons.md): Beschreibt die Schritte zum Anzeigen eines Symbols mit einem Formular.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)
- [Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

