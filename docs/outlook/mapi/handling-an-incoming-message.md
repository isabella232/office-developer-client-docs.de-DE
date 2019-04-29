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
  
Eine eingehende Nachricht ist eine Nachricht, die über ein oder mehrere Messagingsysteme gesendet wurde. Sie wurde möglicherweise nur an Sie oder an viele andere Empfänger gesendet. Eingehende Nachrichten werden in einem Empfangsordner gespeichert, der zum Speichern von Nachrichten einer bestimmten Klasse bestimmt ist. Sie können für jede Nachrichtenklasse, die Sie behandeln, oder einen Ordner für alle Klassen verwenden, einen anderen Empfangsordner einrichten.
  
Wenn Sie sich mit dem Nachrichtenspeicher für neue e-Mail-Benachrichtigungen registriert haben, werden Sie benachrichtigt, wenn eine Nachricht in einem Empfangsordner gespeichert wird. Wenn Sie sich noch nicht für neue e-Mail-Benachrichtigungen registriert haben, müssen Sie den entsprechenden Empfangsordner regelmäßig öffnen, um manuell nach der Ankunft neuer Nachrichten zu suchen.
  
Clients registrieren für neue e-Mail-Benachrichtigungen, indem Sie die Parameter auf [IMsgStore:: Advise](imsgstore-advise.md) wie folgt festlegen: 
  
- Legen Sie _cbEntryID_ auf 0 fest. 
    
- Legen Sie _lpEntryID_ auf NULL fest. 
    
- Legen Sie _ulEventMask_ auf uleventmaskfnevnewmail. 
    
Der _lpNotifications_ -Parameter im Aufruf Ihrer **IMAPIAdviseSink:: OnNotify** -Methode verweist auf eine **NEWMAIL\_** -Benachrichtigungsstruktur, die Informationen über die eingehende Nachricht enthält, beispielsweise Ihre Nachrichtenklasse, Ihren Eintrag Bezeichner, die Eintrags-ID des übergeordneten Ordners und der Inhalt seiner **PR_MESSAGE_FLAGS** -Eigenschaft. Weitere Informationen zum Registrieren und behandeln von Benachrichtigungen finden Sie unter [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und [Handling Notifications](handling-notifications.md). 
  
Bevor Sie einem Benutzer eine eingehende Nachricht anzeigen, bestimmen Sie, ob es sich bei der Nachrichtenklasse um eine vom Client unterstützte Klasse handelt. Wenn dies nicht der Fall ist, ignorieren Sie die Nachricht. Wenn die Klasse unterstützt wird, können Sie die Nachricht mit einem für die Nachrichtenklasse der Nachricht geeigneten Formular öffnen und anzeigen. Die Auswahl der Formulare basiert auf der Nachrichtenklasse. Nachrichten, die zur IPM-Klasse gehören, verwenden ein Standardformular, das von MAPI implementiert wird. Nachrichten, die zu benutzerdefinierten Klassen gehören, die von Clients definiert werden, können entweder Client definierte spezialisierte Formulare oder das MAPI-Standardformular verwenden.
  
## <a name="open-and-display-an-incoming-message"></a>Öffnen und Anzeigen einer eingehenden Nachricht
  
1. Rufen Sie **IMsgStore:: GetReceiveFolder** auf, um den Eintragsbezeichner des Empfänger Ordners für die Nachrichtenklasse der Nachricht abzurufen, und führen Sie diese Eintrags-ID an **IMsgStore:: OpenEntry** , um den Ordner zu öffnen. Weitere Informationen finden Sie unter [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md)und [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).
    
2. Rufen Sie die **IMAPIContainer::** getContents-Methode des empfangen-Ordners auf, um die Inhaltstabelle abzurufen. Weitere Informationen finden Sie unter [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontentable. Rufen Sie die **IMAPITable:: QueryRows** -Methode der Tabelle auf, um alle Zeilen in der Tabelle abzurufen. Weitere Informationen finden Sie unter [IMAPITable:: QueryRows](imapitable-queryrows.md) -und [Inhaltstabellen](contents-tables.md). Weitere Informationen zum Anzeigen einer Inhaltstabelle finden Sie unter [Anzeigen einer Ordnerinhaltstabelle](displaying-a-folder-contents-table.md).
    
3. Wenn Ihr Client interaktiv ist, lassen Sie den Benutzer eine Nachricht aus der Tabelle auswählen und bestimmen, welches Formular zum Anzeigen dieser Nachricht verwendet werden soll. Clients können das von MAPI bereitgestellte Standardformular oder ein benutzerdefiniertes Formular verwenden. Weitere Informationen finden Sie unter [Behandeln von MAPI-Formularen](handling-mapi-forms.md).
    
4. Rufen Sie **IMsgStore:: OpenEntry** auf, um die Nachricht zu öffnen. Weitere Informationen finden Sie unter [Öffnen einer Nachricht](opening-a-message.md).
    
5. Verarbeiten Sie den Nachrichtentext. Weitere Informationen finden Sie unter [Öffnen von Nachrichten Text](opening-message-text.md).
    
6. Rendern Sie die einzelnen Nachrichtenanlagen. Weitere Informationen finden Sie unter [Rendern einer Anlage im nur-Text](rendering-an-attachment-in-plain-text.md) -Format oder [Rendern einer Anlage in RTF-Text](rendering-an-attachment-in-rtf-text.md).
    
7. Öffnen Sie eine Anlage, falls gewünscht. Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Öffnen des Nachrichtentexts](opening-message-text.md): Beschreibt, wie der Nachrichtentext geöffnet wird.
    
- [Rendern einer Anlage im Klartext](rendering-an-attachment-in-plain-text.md): Beschreibt, wie eine Anlage im nur-Text-Format gerendert wird.
    
- [Rendern einer Anlage in RTF-Text](rendering-an-attachment-in-rtf-text.md): Beschreibt, wie eine Anlage in formatiertem Text gerendert wird.
    
- [Öffnen einer Anlage](opening-an-attachment.md): Beschreibt, wie Sie eine Anlage öffnen.
    

