---
title: Informationstabellen, die Ordnern zugeordnet sind
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9c9c75d0ae4b9fe060d6717dfa11ad418cbb715b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564647"
---
# <a name="folder-associated-information-tables"></a>Informationstabellen, die Ordnern zugeordnet sind

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI definiert das MAPI_ASSOCIATED-Flag für verschiedene MAPI-Komponenten beim Umgang mit zugehörigen Informationstabellen verwendet werden. Jeden Ordner in einem Nachrichtenspeicher sollte eine zugeordnete Inhaltstabelle zusammen mit dessen standard-Inhaltstabelle. Clientanwendungen speichern spezielle Nachrichten in einen Ordner zugeordneten Inhaltstabelle, Formulare und Ansichten enthalten soll. Zur Unterstützung der Formulare und Ansichten muss Ihre Nachricht Speicheranbieter tatsächlich zugeordneten Inhalt Tabellen implementieren.
  
Um zugeordneten Inhalt Tabellen zu implementieren, muss ein Speicheranbieter Folgendes ausführen:
  
- Das Flag MAPI_ASSOCIATED in der [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode unterstützt, damit Clientanwendungen den Ordner zugeordneten Inhaltstabelle anstelle der standard Inhaltstabelle abrufen können. 
    
- Unterstützung für das Flag MAPI_ASSOCIATED in die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode Clientanwendungen Nachrichten zu einem Ordner zugeordnete Inhaltstabelle hinzufügen können. 
    
- Legen Sie das MAPI_ACCESS_CREATE_ASSOCIATED Bit in die Eigenschaft **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) auf Folder-Objekten.
    
- Unterstützung für das Flag DEL_ASSOCIATED in die [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) -Methode. 
    
- Legen Sie das bit in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) für Nachrichten in der zugehörigen Inhaltstabelle MSGFLAG_ASSOCIATED.
    
- Verfügbar zu machen und reagieren auf die **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft auf den Ordner.
    
- Verwalten der **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))-Eigenschaft auf den Ordner.
    
Es ist keine Bit in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um anzugeben, ob Ihre Nachricht Speicheranbieter zugeordneten Inhalt Tabellen unterstützt. Wenn Ihre Nachricht Speicheranbieter diese nicht unterstützt, sollte beim Aufruf von Clientanwendungen eine der oben beschriebenen Methoden mit dem MAPI_ASSOCIATED-Flag MAPI_E_NO_SUPPORT zurückgegeben werden.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

