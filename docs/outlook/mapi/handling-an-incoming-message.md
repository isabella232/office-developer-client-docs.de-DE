---
title: Behandeln von eingehenden Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 643e55871a94d5d4ef9707e1971f89b282ceec2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580160"
---
# <a name="handling-an-incoming-message"></a>Behandeln von eingehenden Nachrichten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einer eingehenden Nachricht handelt es sich um eine Nachricht, die über ein oder mehrere Messagingsysteme gesendet wurde. Er wurde möglicherweise nur an Sie oder an viele andere Empfänger gesendet. Eingehende Nachrichten werden in einem Empfangsordner platziert, der nachrichten einer bestimmten Klasse enthalten soll. Sie können für jede Nachrichtenklasse, die Sie behandeln, einen anderen Empfangsordner einrichten oder einen Ordner für alle Klassen verwenden.
  
Wenn Sie sich für neue E-Mail-Benachrichtigungen beim Nachrichtenspeicher registriert haben, werden Sie benachrichtigt, wenn sich eine Nachricht in einem Empfangsordner befindet. Wenn Sie sich nicht für neue E-Mail-Benachrichtigungen registriert haben, müssen Sie den entsprechenden Empfangsordner regelmäßig öffnen, um manuell nach dem Eintreffen neuer Nachrichten zu suchen.
  
Clients registrieren sich für neue E-Mail-Benachrichtigungen, indem sie die Parameter auf ["IMsgStore::Advise"](imsgstore-advise.md) wie folgt festlegen: 
  
- Legen Sie  _cbEntryID_ auf 0 fest. 
    
- Legen Sie  _lpEntryID_ auf NULL fest. 
    
- Legen Sie  _"ulEventMask"_ auf "fnevNewMail" fest. 
    
Der _LpNotifications-Parameter_ im Aufruf der **IMAPIAdviseSink::OnNotify-Methode** verweist auf eine **NEWMAIL \_ NOTIFICATION-Struktur,** die Informationen über die eingehende Nachricht enthält, z. B. die Nachrichtenklasse, den Eintragsbezeichner, den Eintragsbezeichner des übergeordneten Ordners und den Inhalt der **PR_MESSAGE_FLAGS-Eigenschaft.** Weitere Informationen zum Registrieren und Behandeln von Benachrichtigungen finden Sie unter [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und [Handling Notifications](handling-notifications.md). 
  
Ermitteln Sie vor dem Anzeigen einer eingehenden Nachricht für einen Benutzer, ob es sich bei der Nachrichtenklasse um eine Vom Client unterstützte Klasse handelt. Wenn nicht, ignorieren Sie die Nachricht. Wenn die Klasse von Ihnen unterstützt wird, können Sie die Nachricht mit einem Formular öffnen und anzeigen, das für die Nachrichtenklasse der Nachricht geeignet ist. Die Auswahl von Formularen basiert auf der Nachrichtenklasse. Nachrichten, die zur IPM-Klasse gehören, verwenden ein Standardformular, das von der MAPI implementiert wird. Nachrichten, die zu von Clients definierten benutzerdefinierten Klassen gehören, können entweder clientdefinierte spezielle Formulare oder das MAPI-Standardformular verwenden.
  
## <a name="open-and-display-an-incoming-message"></a>Öffnen und Anzeigen einer eingehenden Nachricht
  
1. Rufen **Sie IMsgStore::GetReceiveFolder** auf, um den Eintragsbezeichner des Empfangsordners für die Nachrichtenklasse der Nachricht abzurufen, und übergeben Sie diesen Eintragsbezeichner an **IMsgStore::OpenEntry,** um den Ordner zu öffnen. Weitere Informationen finden Sie unter ["IMsgStore::GetReceiveFolder",](imsgstore-getreceivefolder.md) ["IMsgStore::OpenEntry"](imsgstore-openentry.md)und ["Opening a Message Store Folder".](opening-a-message-store-folder.md)
    
2. Rufen Sie die **IMAPIContainer::GetContentsTable-Methode** des Empfangsordners auf, um das Inhaltsverzeichnis abzurufen. Weitere Informationen finden Sie unter [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Rufen Sie die **IMAPITable::QueryRows-Methode** der Tabelle auf, um alle Zeilen in der Tabelle abzurufen. Weitere Informationen finden Sie unter [IMAPITable::QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md). Weitere Informationen zum Anzeigen eines Inhaltsverzeichnisses finden Sie unter [Anzeigen eines Ordnerinhaltsverzeichnisses.](displaying-a-folder-contents-table.md)
    
3. Wenn Ihr Client interaktiv ist, ermöglichen Sie es dem Benutzer, eine Nachricht aus der Tabelle auszuwählen und das Formular zu bestimmen, das zum Anzeigen dieser Nachricht verwendet werden soll. Clients können das standardformular verwenden, das von MAPI oder einem benutzerdefinierten Formular bereitgestellt wird. Weitere Informationen finden Sie unter [Behandeln von MAPI-Formularen.](handling-mapi-forms.md)
    
4. Rufen **Sie IMsgStore::OpenEntry** auf, um die Nachricht zu öffnen. Weitere Informationen finden Sie unter [Öffnen einer Nachricht.](opening-a-message.md)
    
5. Verarbeiten des Nachrichtentexts. Weitere Informationen finden Sie unter Öffnen von [Nachrichtentext.](opening-message-text.md)
    
6. Rendern sie alle Nachrichtenanlagen. Weitere Informationen finden Sie unter [Rendern einer Anlage in Nur-Text](rendering-an-attachment-in-plain-text.md) oder [Rendern einer Anlage in RTF-Text.](rendering-an-attachment-in-rtf-text.md)
    
7. Öffnen Sie bei Bedarf eine Anlage. Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Öffnen von Nachrichtentext:](opening-message-text.md)Beschreibt, wie der Nachrichtentext geöffnet wird.
    
- [Rendern einer Anlage in Nur-Text:](rendering-an-attachment-in-plain-text.md)Beschreibt, wie eine Anlage in Nur-Text gerendert wird.
    
- [Rendern einer Anlage in RTF-Text:](rendering-an-attachment-in-rtf-text.md)Beschreibt, wie eine Anlage in formatiertem Text gerendert wird.
    
- [Öffnen einer Anlage:](opening-an-attachment.md)Beschreibt, wie eine Anlage geöffnet wird.
    

