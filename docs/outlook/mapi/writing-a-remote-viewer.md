---
title: Schreiben eines Remote-Viewers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0a4f5f186c97e3f8cfc0d3e73695e6dfa96a85c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566185"
---
# <a name="writing-a-remote-viewer"></a>Schreiben eines Remote-Viewers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Remoteviewer ist ein Fenster in einer Clientanwendung, das kontrollierten Zugriff auf Nachrichten bereitstellt, die auf einem anderen Computer gespeichert sind. Dieser kontrollierte Zugriff funktioniert möglicherweise über eine langsame Kommunikationsverbindung. Anstatt jedes Mal, wenn ein Benutzer einen Ordner öffnet, eine vollständige Auswahl der verfügbaren Nachrichten abzurufen, zeigt der Remoteviewer zuerst nur die Kopfzeilen an. Der Benutzer wählt dann aus den Kopfzeilen aus, welche der Nachrichten vollständig angezeigt werden soll. Remoteviewer-Clients können ihren Benutzern erlauben, Nachrichten zu löschen, bevor sie heruntergeladen werden. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>So rufen Sie die Kopfzeilen von remote gespeicherten Nachrichten ab
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zuzugreifen. 
    
2. Call [IMAPITable::Restrict](imapitable-restrict.md) to limit the status table to only those rows that have their **PR \_ RESOURCE \_ TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI \_ TRANSPORT \_ PROVIDER. 
    
3. Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) auf, um die folgenden Spalten in die Statustabelle einzuschließen: 
   - **PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR \_ RESOURCE \_ METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR \_ \_RESSOURCENTYP**, **PR PROVIDER \_ \_ DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR \_ STATUS \_ CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen in der Statustabelle abzurufen. 
    
5. Übergeben Sie den Eintragsbezeichner für jede Zeile in der Tabelle in einem Aufruf von [IMAPISession::OpenEntry](imapisession-openentry.md). Da diese Schnittstelle vom Prozesskontext des MAPI-Spoolers zum Prozesskontext des Clients gemarshallt wird – im Gegensatz zu Schnittstellen, die normalerweise von Adressbuch- oder Nachrichtenspeicheranbietern abgerufen werden – sind Probleme im Zusammenhang mit Multithreading wichtiger. 
    
6. Rufen Sie die [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) des Statusobjekts auf, und übergeben Sie IID_IMAPIFolder als Schnittstellenbezeichner, um den Remoteordner abzurufen. Der Remoteordner ist keine vollständige Ordnerimplementierungen. unterstützt nur eine Teilmenge der Ordnermethoden und -eigenschaften. Eine der erforderlichen Methoden, [IMAPIProp::GetProps,](imapiprop-getprops.md)unterstützt den Abruf der folgenden Eigenschaften:
    
    |||
    |:-----|:-----|
    |**PR \_ ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR \_ SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Remoteordner müssen auch die Methoden [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)und [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) unterstützen. Inhaltsverzeichnisse für Remoteordner unterstützen in der Regel die folgenden Spalten: 
        
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
   
7. Rufen Sie die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Transportanbieters auf, wenn eine der Übertragungsoptionen zum ersten Mal ausgewählt wird. Es sollten entweder das REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE Prozess-Flag sowie das SHOW_XP_SSESSION_UI-Flag festgelegt werden, damit die Benutzeroberfläche angezeigt werden kann. 
    
   > [!NOTE]
   > Um einen bestimmten Nachrichtenkopf zum Herunterladen oder Löschen zu markieren, ruft ein Client [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) auf und legt entweder das MSGSTATUS_REMOTE_DOWNLOAD oder MSGSTATUS_REMOTE_DELETE Flag fest. 
  

