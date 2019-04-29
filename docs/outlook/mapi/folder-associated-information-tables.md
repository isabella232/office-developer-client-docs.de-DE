---
title: Ordner zugeordnete Informationstabellen
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
# <a name="folder-associated-information-tables"></a>Ordner zugeordnete Informationstabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert das MAPI_ASSOCIATED-Flag für verschiedene MAPI-Komponenten, die beim Umgang mit zugeordneten Informationstabellen verwendet werden sollen. Jeder Ordner in einem Nachrichtenspeicher sollte über eine zugehörige Inhaltstabelle sowie die Tabelle mit den Standardinhalten verfügen. Client Anwendungen speichern spezielle Nachrichten in der zugeordneten Inhaltstabelle eines Ordners, um Formulare und Ansichten aufzunehmen. Zur Unterstützung von Formularen und Ansichten muss der Nachrichtenspeicher Anbieter zugehörige Inhaltstabellen implementieren.
  
Um zugeordnete Inhaltstabellen zu implementieren, müssen Sie Folgendes tun:
  
- Unterstützen Sie das MAPI_ASSOCIATED-Flag in der [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode, sodass Clientanwendungen die Tabelle mit den zugeordneten Inhalten des Ordners anstelle der Standardinhalts Tabelle abrufen können. 
    
- Unterstützen Sie das MAPI_ASSOCIATED-Flag in der [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode, sodass Clientanwendungen der Tabelle zugeordnete Inhaltsstoffe eines Ordners Nachrichten hinzufügen können. 
    
- Legen Sie das MAPI_ACCESS_CREATE_ASSOCIATED-Bit in der **PR_ACCESS** ([pidtagaccess (](pidtagaccess-canonical-property.md))-Eigenschaft für Folder-Objekte fest.
    
- Unterstützen Sie das DEL_ASSOCIATED-Flag in der [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) -Methode. 
    
- Legen Sie das MSGFLAG_ASSOCIATED-Bit in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft für Nachrichten in der Tabelle zugeordnete Inhalte fest.
    
- Verfügbar machen und reagieren auf die **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft in Ordnern.
    
- Verwalten der **PR_ASSOC_CONTENT_COUNT** ([pidtagassociatedcontentcount (](pidtagassociatedcontentcount-canonical-property.md))-Eigenschaft für Ordner.
    
Die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft gibt kein Bit an, um anzugeben, ob der Nachrichtenspeicher Anbieter zugeordnete Inhaltstabellen unterstützt. Wenn Ihr Nachrichtenspeicher Anbieter diese nicht unterstützt, sollte MAPI_E_NO_SUPPORT zurückgegeben werden, wenn Clientanwendungen eine der obigen Methoden mit dem MAPI_ASSOCIATED-Flag aufrufen.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

