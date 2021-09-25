---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 162e31574cc182c93ffcda5f9d38f045f7e7e152
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551401"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner aus.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Folder-Objekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFolder  <br/> |
|Zeigertyp:  <br/> |LPMAPIFOLDER  <br/> |
|Transaktionsmodell:  <br/> |Nicht übersetzt  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Createmessage](imapifolder-createmessage.md) <br/> |Erstellt eine neue Nachricht.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Kopiert oder verschiebt eine oder mehrere Nachrichten.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Löscht eine oder mehrere Nachrichten.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Erstellt einen neuen Unterordner.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Kopiert oder verschiebt einen Unterordner.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Löscht einen Unterordner.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Legt das MSGFLAG_READ Flag in der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) einer oder mehrerer Nachrichten des Ordners fest oder löscht es und verwaltet das Senden von Leseberichten.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Ruft den Status ab, der einer Nachricht in einem bestimmten Ordner zugeordnet ist.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Legt den Status fest, der einer Nachricht zugeordnet ist.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Legt die Standardsortierreihenfolge für das Inhaltsverzeichnis eines Ordners fest.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst zu löschen.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

