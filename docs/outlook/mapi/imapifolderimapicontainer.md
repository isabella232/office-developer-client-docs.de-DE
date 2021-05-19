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
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424238"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner aus.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Folder-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter von Nachrichtenspeichern  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFolder  <br/> |
|Zeigertyp:  <br/> |LPMAPIFOLDER  <br/> |
|Transaktionsmodell:  <br/> |Nichttransaktioniert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Erstellt eine neue Nachricht.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Kopiert oder verschiebt eine oder mehrere Nachrichten.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Löscht eine oder mehrere Nachrichten.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Erstellt einen neuen Unterordner.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Kopiert oder verschiebt einen Unterordner.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Löscht einen Unterordner.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Legt das flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer oder mehreren Nachrichten des Ordners fest oder entfernt es und verwaltet das Senden von Leseberichten.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Ruft den Status ab, der einer Nachricht in einem bestimmten Ordner zugeordnet ist.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Legt den Status fest, der einer Nachricht zugeordnet ist.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Legt die Standardsortreihenfolge für die Inhaltstabelle eines Ordners fest.  <br/> |
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

