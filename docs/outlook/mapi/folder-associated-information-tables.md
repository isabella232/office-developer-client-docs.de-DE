---
title: Folder-Associated-Informationstabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2710605feba0faafdfdc0ad1f4e3a1e3b19de999
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576282"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated-Informationstabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI definiert das MAPI_ASSOCIATED-Kennzeichen für verschiedene MAPI-Komponenten, die im Umgang mit zugeordneten Informationstabellen verwendet werden sollen. Jedem Ordner in einem Nachrichtenspeicher sollte ein zugeordnetes Inhaltsverzeichnis zusammen mit dem Standardinhaltsverzeichnis zugeordnet sein. Clientanwendungen speichern spezielle Nachrichten im zugeordneten Inhaltsverzeichnis eines Ordners, um Formulare und Ansichten zu speichern. Tatsächlich muss Ihr Nachrichtenspeicheranbieter zugeordnete Inhaltstabellen implementieren, um Formulare und Ansichten zu unterstützen.
  
Um zugeordnete Inhaltstabellen zu implementieren, muss Ihr Speicheranbieter Folgendes tun:
  
- Unterstützen Sie das flag MAPI_ASSOCIATED in der [IMAPIContainer::GetContentsTable-Methode,](imapicontainer-getcontentstable.md) damit Clientanwendungen das zugeordnete Inhaltsverzeichnis des Ordners anstelle des Standardinhaltsverzeichnisses abrufen können. 
    
- Unterstützen Sie die MAPI_ASSOCIATED-Kennzeichnung in der [IMAPIFolder::CreateMessage-Methode,](imapifolder-createmessage.md) damit Clientanwendungen Nachrichten zur zugeordneten Inhaltstabelle eines Ordners hinzufügen können. 
    
- Legen Sie das MAPI_ACCESS_CREATE_ASSOCIATED Bit in der **Eigenschaft PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) für Ordnerobjekte fest.
    
- Unterstützen Sie das flag DEL_ASSOCIATED in der [IMAPIFolder::EmptyFolder-Methode.](imapifolder-emptyfolder.md) 
    
- Legen Sie das MSGFLAG_ASSOCIATED Bit in der **Eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) für Nachrichten im zugeordneten Inhaltsverzeichnis fest.
    
- Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.
    
- Verwalten der **eigenschaft PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) für Ordner.
    
Die **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) enthält kein Bit, um anzugeben, ob Ihr Nachrichtenspeicheranbieter zugeordnete Inhaltstabellen unterstützt. Wenn ihr Nachrichtenspeicheranbieter diese nicht unterstützt, sollte er MAPI_E_NO_SUPPORT zurückgeben, wenn Clientanwendungen eine der oben genannten Methoden mit dem flag MAPI_ASSOCIATED aufrufen.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

