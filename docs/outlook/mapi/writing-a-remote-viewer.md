---
title: Schreiben eines remote-Viewers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391605"
---
# <a name="writing-a-remote-viewer"></a>Schreiben eines remote-Viewers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein remote-Viewer ist ein Fenster in einer anderen Clientanwendung den gesteuerten Zugriff auf Nachrichten, die auf einem anderen Computer gespeichert. Diese gesteuerte Zugriff kann auf eine langsame Verbindung ausgeführt werden. Statt eine umfassende Auswahl an verfügbaren Nachrichten abzurufen, jedes Mal, wenn ein Benutzer einen Ordner öffnet, wird im remote Viewer zunächst nur die Kopfzeilen. Der Benutzer wählt dann aus die Kopfzeilen der Nachrichten vollständig angezeigt. Remote-Viewer-Clients können ihre Benutzer Nachrichten löschen, bevor sie jemals heruntergeladen werden dürfen. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Die Kopfzeilen der Nachrichten remote gespeicherten abrufen
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle. 
    
2. Rufen Sie die [Methode IMAPITable:: Restrict](imapitable-restrict.md) , um nur die Zeilen der Statustabelle zu begrenzen, haben ihre **PR\_Ressource\_Typ** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) Spalte festlegen MAPI\_TRANSPORT\_PROVIDER. 
    
3. Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Einschließen von der folgenden Spalten in der Tabelle "Status": 
   - **Kurs\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Kurs\_Ressource\_Methoden** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **Kurs\_Ressource\_Typ**, **PR\_PROVIDER\_Anzeige** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **Kurs\_STATUS\_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) , um alle Zeilen in der Tabelle "Status" abzurufen. 
    
5. Übergeben Sie die Eintrags-ID für jede Zeile in der Tabelle in einem Aufruf von [IMAPISession::OpenEntry](imapisession-openentry.md). Da diese Schnittstelle aus Prozess-Kontext die MAPI-Warteschlange auf dem Client Prozesskontext gemarshallt wird – im Gegensatz zu Schnittstellen, die in der Regel von Adressbuch oder einer Nachricht erhalten speichern-Anbieter – Probleme bezüglich multithreading werden weitere Wichtigkeitsstufe. 
    
6. Rufen Sie den Status des Objekts [QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) -Methode übergeben IID_IMAPIFolder als Schnittstellenbezeichner, um remote-Ordners abzurufen. Der remote-Ordner ist keine vollständige Ordner Implementierung. unterstützt nur eine Teilmenge der Ordner Methoden und Eigenschaften. Einer der erforderlichen Methoden, [IMAPIProp::GetProps](imapiprop-getprops.md), unterstützt das Abrufen der folgenden Eigenschaften:
    
    |||
    |:-----|:-----|
    |**Kurs\_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**Kurs\_UNTERORDNER** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Remote-Ordner müssen auch die Methoden [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)und [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) unterstützen. Remote-Ordner Inhalt Tabellen unterstützen in der Regel die folgenden Spalten: 
        
    |||
    |:-----|:-----|
    |**Kurs\_Anzeige\_an** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**Kurs\_ENTRYID** <br/> |
    |**Kurs\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**Kurs\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**Kurs\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**Kurs\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Aufrufen der Adressbuchhierarchie [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode die erste Zeit, die eine der Übertragungsoptionen ausgewählt ist. Die REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE Prozess Flag sollte die Benutzeroberfläche angezeigt werden können sowie das Flag SHOW_XP_SSESSION_UI festgelegt werden. 
    
   > [!NOTE]
   > Um ein bestimmtes Nachrichtenkopf zum Herunterladen oder löschen zu markieren, ein Client ruft [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) und die MSGSTATUS_REMOTE_DOWNLOAD oder MSGSTATUS_REMOTE_DELETE gekennzeichnet. 
  

