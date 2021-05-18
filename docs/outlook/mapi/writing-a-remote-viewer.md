---
title: Schreiben eines Remote-Viewers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325662"
---
# <a name="writing-a-remote-viewer"></a>Schreiben eines Remote-Viewers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Remoteanzeiger ist ein Fenster in einer Clientanwendung, das kontrollierten Zugriff auf Nachrichten bietet, die auf einem anderen Computer gespeichert sind. Dieser kontrollierte Zugriff funktioniert möglicherweise über eine langsame Kommunikationsverbindung. Anstatt bei jedem Öffnen eines Ordners eine vollständige Auswahl verfügbarer Nachrichten abzurufen, zeigt der Remoteanzeige zunächst nur die Kopfzeilen an. Der Benutzer wählt dann aus den Kopfzeilen aus, welche der Nachrichten vollständig angezeigt werden sollen. Remote-Viewer-Clients können benutzern das Löschen von Nachrichten ermöglichen, bevor sie heruntergeladen werden. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>So rufen Sie die Kopfzeilen von Remotenachrichten ab
  
1. Rufen [Sie IMAPISession::GetStatusTable auf,](imapisession-getstatustable.md) um auf die Statustabelle zu zugreifen. 
    
2. Rufen [Sie IMAPITable::Restrict](imapitable-restrict.md) auf, um die Statustabelle auf die Zeilen zu beschränken, für die die **Spalte PR RESOURCE \_ \_ TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) auf MAPI \_ TRANSPORT PROVIDER festgelegt \_ ist. 
    
3. Rufen [Sie IMAPITable::SetColumns auf,](imapitable-setcolumns.md) um die folgenden Spalten in die Statustabelle zu setzen: 
   - **PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR \_ RESOURCE \_ METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR \_ \_RESSOURCENTYP**, **\_ PR-ANBIETERANZEIGE \_** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR \_ \_STATUSCODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md) um alle Zeilen in der Statustabelle abzurufen. 
    
5. Übergeben Sie den Eintragsbezeichner für jede Zeile in der Tabelle in einem Aufruf von [IMAPISession::OpenEntry](imapisession-openentry.md). Da diese Schnittstelle aus dem Prozesskontext des MAPI-Spoolers in den Prozesskontext des Clients ge marshallt wird – im Gegensatz zu Schnittstellen, die normalerweise von Adressbuch- oder Nachrichtenspeicheranbietern erhalten werden – sind Probleme im Zusammenhang mit multithreading wichtiger. 
    
6. Rufen Sie die [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) des Statusobjekts auf und übergeben IID_IMAPIFolder als Schnittstellenbezeichner, um den Remoteordner abzurufen. Der Remoteordner ist keine vollständige Ordnerimplementierung. Es unterstützt nur eine Teilmenge der Ordnermethoden und -eigenschaften. Eine der erforderlichen Methoden, [IMAPIProp::GetProps](imapiprop-getprops.md), unterstützt das Abrufen der folgenden Eigenschaften:
    
    |||
    |:-----|:-----|
    |**PR \_ ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR \_ SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Remoteordner müssen auch die [Methoden IMAPIProp::GetPropList,](imapiprop-getproplist.md) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)und [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) unterstützen. Inhaltstabellen für Remoteordner unterstützen in der Regel die folgenden Spalten: 
        
    |||
    |:-----|:-----|
    |**PR \_ DISPLAY \_ TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR \_ ENTRYID** <br/> |
    |**PR \_ HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR \_ MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR \_ MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Rufen Sie die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Transportanbieters auf, wenn eine der Übertragungsoptionen zum ersten Mal ausgewählt wird. Entweder das REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE-Prozessflag sowie das SHOW_XP_SSESSION_UI festgelegt werden, damit die Benutzeroberfläche angezeigt werden kann. 
    
   > [!NOTE]
   > Um einen bestimmten Nachrichtenheader zum Herunterladen oder Löschen zu markieren, ruft ein Client [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) auf und legt entweder das MSGSTATUS_REMOTE_DOWNLOAD- oder MSGSTATUS_REMOTE_DELETE fest. 
  

