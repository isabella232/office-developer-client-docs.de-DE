---
title: Schreiben eines Remote-Viewers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325662"
---
# <a name="writing-a-remote-viewer"></a>Schreiben eines Remote-Viewers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einem Remote Viewer handelt es sich um ein Fenster in einer Clientanwendung, das den Zugriff auf Nachrichten kontrolliert, die auf einem anderen Computer gespeichert sind. Dieser kontrollierte Zugriff kann auf eine langsame Kommunikationsverbindung angewendet werden. Statt eine vollständige Auswahl der verfügbaren Nachrichten immer dann abzurufen, wenn ein Benutzer einen Ordner öffnet, werden zunächst nur die Kopfzeilen angezeigt. Der Benutzer wählt dann aus den Kopfzeilen aus, welche der Nachrichten vollständig angezeigt werden sollen. Remote Viewer-Clients können Benutzern das Löschen von Nachrichten ermöglichen, bevor Sie heruntergeladen werden. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>So rufen Sie die Kopfzeilen von Nachrichten ab, die Remote gespeichert werden
  
1. Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen. 
    
2. Rufen Sie [IMAPITable:: Restrict](imapitable-restrict.md) auf, um die Statustabelle auf die Zeilen einzuschränken, deren **PR\_-\_Ressourcentyp** ([pidtagresourcetype (](pidtagresourcetype-canonical-property.md))\_auf\_MAPI-Transport Anbieter festgelegt ist. 
    
3. Rufen Sie [IMAPITable::](imapitable-setcolumns.md) SetColumns auf, um die folgenden Spalten in die Statustabelle einzuschließen: 
   - **PR\_** -Eintrags-Nr. ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR\_-\_Ressourcen Methoden** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))
   - **PR\_-\_Ressourcentyp**, **\_PR\_-Anbieter Anzeige** ([pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))
   - **PR\_-\_Status Code** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md)).
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen in der Statustabelle abzurufen. 
    
5. Führen Sie den Eintragsbezeichner für jede Zeile in der Tabelle in einem Aufruf von [IMAPISession:: OpenEntry](imapisession-openentry.md)aus. Da diese Schnittstelle vom Prozesskontext des MAPI-Spoolers zum Prozesskontext des Clients gemarshallt wird – im Gegensatz zu Schnittstellen, die normalerweise von Adressbuch-oder Nachrichtenspeicher Anbietern abgerufen werden – sind Probleme im Zusammenhang mit Multithreading von größerer Bedeutung. 
    
6. Rufen Sie die [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) -Methode des Status-Objekts auf, übergeben Sie IID_IMAPIFolder als Schnittstellenbezeichner, um den Remoteordner abzurufen. Der Remoteordner ist keine vollständige Ordner Implementierung; Es unterstützt nur eine Teilmenge der Folder-Methoden und-Eigenschaften. Eine der erforderlichen Methoden, [IMAPIProp::](imapiprop-getprops.md)GetProps, unterstützt das Abrufen der folgenden Eigenschaften:
    
    |||
    |:-----|:-----|
    |**PR\_-Zugriff** ([pidtagaccess (](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([Pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([Pidtagassociatedcontentcount (](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([Pidtagfoldertype (](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR\_** -Unterordner ([pidtagsubfolders (](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Remote Ordner müssen außerdem die Methoden [IMAPIProp::](imapiprop-getproplist.md)getproplist, [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontentable und [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) unterstützen. Inhaltstabellen für Remote Ordner unterstützen in der Regel die folgenden Spalten: 
        
    |||
    |:-----|:-----|
    |**PR\_-\_Anzeige an** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR\_-Eintrags-Nr.** <br/> |
    |**PR\_-HASATTACH** ([pidtaghasattachments (](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_-MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_-MESSAGE_DOWNLOAD_TIME** ([pidtagmessagedownloadtime (](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([Pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_-SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Rufen Sie die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode des Transportanbieters zum ersten Mal auf, wenn eine der Übertragungsoptionen ausgewählt wird. Entweder das REFRESH_XP_HEADER_CACHE-oder das PROCESS_XP_HEADER_CACHE-Prozess Kennzeichen sollte ebenso festgelegt werden wie das SHOW_XP_SSESSION_UI-Flag, damit die Benutzeroberfläche angezeigt wird. 
    
   > [!NOTE]
   > Um einen bestimmten Nachrichtenkopf zum Herunterladen oder löschen zu markieren, Ruft ein Client [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) auf und legt das MSGSTATUS_REMOTE_DOWNLOAD-oder MSGSTATUS_REMOTE_DELETE-Flag fest. 
  

