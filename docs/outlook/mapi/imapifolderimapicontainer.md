---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1886987515f3cafe38418960baa4b6fd89e3b6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590799"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verfügbar gemacht von:  <br/> |Folder-Objekten  <br/> |
|Implementiert von:  <br/> |Nachricht-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFolder  <br/> |
|Zeigertyp:  <br/> |LPMAPIFOLDER  <br/> |
|Transaktionsmodell:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Erstellt eine neue Nachricht an.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Kopiert oder verschiebt eine oder mehrere Nachrichten.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Löscht eine oder mehrere Nachrichten.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Erstellt einen neuen Unterordner.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Kopiert oder Verschiebt einen Unterordner.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Löscht einen Unterordner.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Legt fest oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) von einem oder mehreren der Nachrichten, die den Ordner und das Senden von lesen Berichte verwaltet.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Ruft den Status einer Nachricht in einem bestimmten Ordner an.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Setzt den Status einer Nachricht.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Legt die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle fest.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst löschen.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

