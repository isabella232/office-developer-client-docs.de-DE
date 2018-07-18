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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792131"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Betrifft**: Outlook 
  
Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Folder-Objekten  <br/> |
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
   
|**Erforderliche Eigenschaften**|**Zugriff**|
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

