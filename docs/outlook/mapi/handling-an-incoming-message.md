---
title: Behandeln von einer eingehenden Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d6ec40005683cc67c51a63d6b186c042c8e170d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568175"
---
# <a name="handling-an-incoming-message"></a>Behandeln von einer eingehenden Nachricht

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine eingehende Nachricht ist eine Nachricht, die über eine oder mehrere Messagingsystemen gesendet wurde. Es kann nur für Sie oder für viele andere Empfänger gesendet wurden. Eingehende Nachrichten befinden sich in einem Empfangsordner vorgesehen, die Nachrichten von einer bestimmten Klasse enthalten soll. Sie können Einrichten einer anderen Empfangsordner für jede Nachrichtenklasse, dass Sie behandeln oder einen Ordner für alle Klassen.
  
Wenn Sie für neue e-Mail-Benachrichtigungen, mit dem Nachrichtenspeicher registriert haben, werden Sie benachrichtigt, sobald eine Nachricht in einem Empfangsordner platziert wird. Wenn Sie nicht für neue e-Mail-Benachrichtigungen registriert haben, müssen Sie die entsprechende öffnen Empfangsordner regelmäßig, um den Empfang von neuen Nachrichten manuell prüfen.
  
Clients registrieren für neue e-Mail-Benachrichtigungen, indem Sie die Parameter [IMsgStore::Advise](imsgstore-advise.md) wie folgt festlegen: 
  
- _CbEntryID_ auf 0 festgelegt. 
    
- _LpEntryID_ auf NULL festgelegt wurde. 
    
- _UlEventMask_ auf FnevNewMail festgelegt. 
    
Der _LpNotifications_ -Parameter im Aufruf der Methode **IMAPIAdviseSink::OnNotify** verweist auf eine **NEWMAIL\_Benachrichtigung** -Struktur, die Informationen über die eingehende Nachricht, wie deren Nachrichtenklasse den Eintrag enthält Bezeichner, die Eintrags-ID des übergeordneten Ordners und den Inhalt der **PR_MESSAGE_FLAGS** -Eigenschaft ab. Weitere Informationen zum Registrieren für und Behandeln von Benachrichtigungen finden Sie unter [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und [Behandeln von Benachrichtigungen](handling-notifications.md). 
  
Vor dem Anzeigen einer eingehenden Nachricht, die einem Benutzer, bestimmen Sie, ob deren Nachrichtenklasse einer Klasse ist, die der Client unterstützt. Wenn dies nicht der Fall ist, ignorieren Sie die Meldung. Wenn die Klasse, die Sie unterstützen ist, können Sie öffnen und anzeigen die Nachricht mit einem Formular, das für die Nachrichtenklasse der Nachricht geeignet ist. Die Auswahl von Formularen basiert auf Nachrichtenklasse. Nachrichten, die Sie der Klasse IPM gehören verwenden ein Standardformulars MAPI implementiert. Nachrichten, die von Clients definierten benutzerdefinierten Klassen angehören, können spezielle Formen Client definiert oder das Standardformular MAPI verwendet werden.
  
## <a name="open-and-display-an-incoming-message"></a>Öffnen und Anzeigen von einer eingehenden Nachricht
  
1. Rufen Sie **IMsgStore::GetReceiveFolder** zum Abrufen der Eintrags-ID des Ordners für die Nachrichtenklasse der Nachricht empfangen und übergeben Sie dieses Eintrags-ID an **IMsgStore::OpenEntry** zum Öffnen des Ordners. Weitere Informationen finden Sie unter [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)und [einen Speicherordner Nachricht öffnen](opening-a-message-store-folder.md).
    
2. Rufen Sie den Empfangsordner **IMAPIContainer::GetContentsTable** -Methode zum Abrufen der Inhaltstabelle. Weitere Informationen finden Sie unter [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Rufen Sie **die Tabelle QueryRows, um alle Zeilen in der Tabelle abzurufen** . Weitere Informationen finden Sie unter [IMAPITable::QueryRows](imapitable-queryrows.md) und [Inhalt Tabellen](contents-tables.md). Weitere Informationen zum Anzeigen einer Inhaltstabelle finden Sie unter [Tabelle ein Ordner-Inhalt angezeigt](displaying-a-folder-contents-table.md).
    
3. Bei Ihrer Client interaktive erlaubt den Benutzer eine Nachricht aus der Tabelle auswählen, und bestimmen Sie das Formular zum Anzeigen dieser Nachricht verwendet werden soll. Clients können das Standardformular von MAPI oder ein benutzerdefiniertes Formular bereitgestellt wird. Weitere Informationen finden Sie unter [Behandeln von MAPI-Formulare](handling-mapi-forms.md).
    
4. Rufen Sie **IMsgStore::OpenEntry** , um die Nachricht zu öffnen. Weitere Informationen finden Sie unter [Öffnen einer Nachricht](opening-a-message.md).
    
5. Verarbeitet den Nachrichtentext an. Weitere Informationen finden Sie unter [Öffnen des Nachrichtentexts](opening-message-text.md).
    
6. Alle e-Mail-Anlagen zu rendern. Weitere Informationen finden Sie unter [Rendern einer Anlage im Nur-Text](rendering-an-attachment-in-plain-text.md) oder [eine Anlage in RTF-Text rendern](rendering-an-attachment-in-rtf-text.md).
    
7. Öffnen Sie eine Anlage aus, falls gewünscht. Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Öffnen des Nachrichtentexts](opening-message-text.md): Beschreibt, wie Sie den Nachrichtentext zu öffnen.
    
- [Eine Anlage in nur-Text rendern](rendering-an-attachment-in-plain-text.md): Beschreibt, wie Sie eine Anlage in nur-Text zu rendern.
    
- [Rendern einer Anlage im RTF-Text](rendering-an-attachment-in-rtf-text.md): Beschreibt, wie eine Anlage in formatierten Text gerendert werden soll.
    
- [Öffnen einer Anlage](opening-an-attachment.md): Beschreibt, wie eine Anlage geöffnet.
    

