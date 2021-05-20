---
title: Behandeln von eingehenden Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f3fbe34793e3520b26b984f4bd6b14fbcab7a951
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438981"
---
# <a name="handling-an-incoming-message"></a>Behandeln von eingehenden Nachrichten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine eingehende Nachricht ist eine Nachricht, die über ein oder mehrere Messagingsysteme gesendet wurde. Es wurde möglicherweise nur an Sie oder an viele andere Empfänger gesendet. Eingehende Nachrichten werden in einem Empfangsordner platziert, der für Nachrichten einer bestimmten Klasse bestimmt ist. Sie können einen anderen Empfangsordner für jede Nachrichtenklasse einrichten, die Sie verarbeiten oder einen Ordner für alle Klassen verwenden.
  
Wenn Sie sich beim Nachrichtenspeicher für neue E-Mail-Benachrichtigungen registriert haben, werden Sie benachrichtigt, wenn eine Nachricht in einem Empfangsordner platziert wird. Wenn Sie sich nicht für neue E-Mail-Benachrichtigungen registriert haben, müssen Sie den entsprechenden Empfangsordner regelmäßig öffnen, um manuell nach dem Eintreffen neuer Nachrichten zu suchen.
  
Clients registrieren sich für neue E-Mail-Benachrichtigungen, indem sie die Parameter auf [IMsgStore::Advise wie](imsgstore-advise.md) folgt festlegen: 
  
- Legen  _Sie cbEntryID_ auf 0. 
    
- Legen  _Sie lpEntryID auf_ NULL. 
    
- Legen  _Sie ulEventMask auf_ fnevNewMail. 
    
Der _lpNotifications-Parameter_ im Aufruf ihrer **IMAPIAdviseSink::OnNotify-Methode** verweist auf eine **NEWMAIL \_** NOTIFICATION-Struktur, die Informationen zur eingehenden Nachricht enthält, z. B. die Nachrichtenklasse, die Eintrags-ID, die Eintrags-ID des übergeordneten Ordners und den Inhalt der **PR_MESSAGE_FLAGS-Eigenschaft.** Weitere Informationen zum Registrieren und Behandeln von Benachrichtigungen finden Sie unter [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und [Handling Notifications](handling-notifications.md). 
  
Ermitteln Sie vor dem Anzeigen einer eingehenden Nachricht für einen Benutzer, ob es sich bei der Nachrichtenklasse um eine Klasse handelt, die vom Client unterstützt wird. Wenn nicht, ignorieren Sie die Nachricht. Wenn es sich bei der Klasse um eine klasse handelt, die Sie unterstützen, können Sie die Nachricht mit einem Formular öffnen und anzeigen, das für die Nachrichtenklasse der Nachricht geeignet ist. Die Auswahl der Formulare basiert auf der Nachrichtenklasse. Nachrichten, die zur IPM-Klasse gehören, verwenden ein von MAPI implementiertes Standardformular. Nachrichten, die zu benutzerdefinierten Klassen gehören, die von Clients definiert werden, können entweder clientdefinierte spezielle Formulare oder das MAPI-Standardformular verwenden.
  
## <a name="open-and-display-an-incoming-message"></a>Öffnen und Anzeigen einer eingehenden Nachricht
  
1. Rufen **Sie IMsgStore::GetReceiveFolder** auf, um die Eintrags-ID des Empfangsordners für die Nachrichtenklasse der Nachricht abzurufen, und übergeben Sie diesen Eintragsbezeichner an **IMsgStore::OpenEntry,** um den Ordner zu öffnen. Weitere Informationen finden Sie unter [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)und [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
2. Rufen Sie die **IMAPIContainer::GetContentsTable-Methode** des Empfangsordners auf, um die Inhaltstabelle abzurufen. Weitere Informationen finden Sie unter [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Rufen Sie die **IMAPITable::QueryRows-Methode** der Tabelle auf, um alle Zeilen in der Tabelle abzurufen. Weitere Informationen finden Sie unter [IMAPITable::QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md). Weitere Informationen zum Anzeigen einer Inhaltstabelle finden Sie unter [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).
    
3. Wenn Ihr Client interaktiv ist, können Sie dem Benutzer erlauben, eine Nachricht aus der Tabelle auszuwählen und das Formular zu bestimmen, das zum Anzeigen dieser Nachricht verwendet werden soll. Clients können das von MAPI oder einem benutzerdefinierten Formular bereitgestellte Standardformular verwenden. Weitere Informationen finden Sie unter [Handling MAPI Forms](handling-mapi-forms.md).
    
4. Rufen **Sie IMsgStore::OpenEntry auf,** um die Nachricht zu öffnen. Weitere Informationen finden Sie unter [Öffnen einer Nachricht](opening-a-message.md).
    
5. Verarbeiten des Nachrichtentexts. Weitere Informationen finden Sie unter [Opening Message Text](opening-message-text.md).
    
6. Rendern Sie jede der Nachrichtenanlagen. Weitere Informationen finden Sie unter [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md) oder Rendering an Attachment in [RTF Text](rendering-an-attachment-in-rtf-text.md).
    
7. Öffnen Sie bei Bedarf eine Anlage. Weitere Informationen finden Sie [unter Öffnen einer Anlage](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Öffnen von Nachrichtentext](opening-message-text.md): Beschreibt, wie der Nachrichtentext geöffnet wird.
    
- [Rendern einer Anlage in Nur-Text:](rendering-an-attachment-in-plain-text.md)Beschreibt, wie eine Anlage in Nur-Text gerendert wird.
    
- [Rendern einer Anlage in RTF Text](rendering-an-attachment-in-rtf-text.md): Beschreibt, wie eine Anlage in formatierten Text gerendert wird.
    
- [Öffnen einer Anlage](opening-an-attachment.md): Beschreibt das Öffnen einer Anlage.
    

