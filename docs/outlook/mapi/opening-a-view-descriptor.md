---
title: Öffnen eine Beschreibung der Ansicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 525c817cfc3bdcf96455d35025e85486ec8b5b42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793305"
---
# <a name="opening-a-view-descriptor"></a>Öffnen eine Beschreibung der Ansicht
  
**Betrifft**: Outlook 
  
Viele Ordner können mit einer Normalansicht, eine Standardansicht oder eine beliebige Anzahl von personalisierte Ansichten geöffnet werden. Eine Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird. Die Normalansicht wird verwendet, wenn keine alternativen Ansicht vorhanden ist und wenn Sie den Ordner zum ersten Mal öffnen. Wenn Sie eine alternative Ansicht vorhanden ist, müssen Sie es zum Öffnen des Ordners verwenden.
  
Eine Ansicht wird in einer Nachricht als ein Deskriptor Ansicht bezeichnet beschrieben. Ansicht Deskriptoren werden in der Regel als zugeordneten Nachrichten erstellt und in den allgemeinen oder persönliche Ansicht-Ordnern oder in einem Ordner IPM können angezeigt werden.
  
### <a name="to-open-a-view-descriptor"></a>Eine Beschreibung der Ansicht öffnen
  
1. Rufen Sie [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) zum Abrufen des zugehörigen Inhaltsverzeichnisses für den Ordner. 
    
2. Erstellen Sie eine Beschränkung, der nur Nachrichten mit der Nachrichtenklasse für die Ansicht Deskriptoren reserviert ermittelt und rufen Sie die [Methode IMAPITable:: Restrict](imapitable-restrict.md) zur Begrenzung der Tabelle und [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen der entsprechenden Zeilen, oder...
    
   Rufen Sie den Ordner [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** enthält die Eintrags-ID für die Nachricht mit der standardmäßigen Ansicht Deskriptor für einen Ordner. Dieser Aufruf erfolgreich, wenn der Ordner die Verwendung des MAPI_ASSOCIATED-Flags für Aufrufe von [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)unterstützt.
    
3. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) , wobei die Eintrags-ID der Ansicht Deskriptor zu öffnen. 
    

