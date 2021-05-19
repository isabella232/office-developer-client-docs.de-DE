---
title: Folder-Associated Informationstabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426415"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated Informationstabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert das MAPI_ASSOCIATED für verschiedene MAPI-Komponenten, die beim Umgang mit zugeordneten Informationstabellen verwendet werden. Jeder Ordner in einem Nachrichtenspeicher sollte eine zugeordnete Inhaltstabelle zusammen mit seiner Standardinhaltstabelle haben. Clientanwendungen speichern spezielle Nachrichten in der zugeordneten Inhaltstabelle eines Ordners, um Formulare und Ansichten zu speichern. Um Formulare und Ansichten zu unterstützen, muss ihr Nachrichtenspeicheranbieter verknüpfte Inhaltstabellen implementieren.
  
Um zugeordnete Inhaltstabellen zu implementieren, muss Ihr Speicheranbieter die folgenden Schritte unternehmen:
  
- Unterstützen Sie MAPI_ASSOCIATED-Flag in der [IMAPIContainer::GetContentsTable-Methode,](imapicontainer-getcontentstable.md) damit Clientanwendungen die zugeordnete Inhaltstabelle des Ordners anstelle der Standardinhaltstabelle erhalten können. 
    
- Unterstützen Sie MAPI_ASSOCIATED-Flag in der [IMAPIFolder::CreateMessage-Methode,](imapifolder-createmessage.md) damit Clientanwendungen Nachrichten zur zugeordneten Inhaltstabelle eines Ordners hinzufügen können. 
    
- Legen Sie MAPI_ACCESS_CREATE_ASSOCIATED -Bit in **der PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) -Eigenschaft für Ordnerobjekte.
    
- Unterstützt das DEL_ASSOCIATED in der [IMAPIFolder::EmptyFolder-Methode.](imapifolder-emptyfolder.md) 
    
- Legen Sie MSGFLAG_ASSOCIATED bit in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft für Nachrichten in der zugeordneten Inhaltstabelle.
    
- Expose and respond to **the PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.
    
- Verwalten sie **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) -Eigenschaft in Ordnern.
    
Die Eigenschaft PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) enthält kein Bit, um anzugeben, ob ihr Nachrichtenspeicheranbieter verknüpfte Inhaltstabellen unterstützt. Wenn der Nachrichtenspeicheranbieter sie nicht unterstützt, sollte MAPI_E_NO_SUPPORT, wenn Clientanwendungen eine der oben genannten Methoden mit dem MAPI_ASSOCIATED aufrufen.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

