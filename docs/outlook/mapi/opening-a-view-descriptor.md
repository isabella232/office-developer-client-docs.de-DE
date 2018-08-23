---
title: Öffnen eine Beschreibung der Ansicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 680d80c0827399f3b7a0ea5819e51be654a05810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592479"
---
# <a name="opening-a-view-descriptor"></a>Öffnen eine Beschreibung der Ansicht
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Viele Ordner können mit einer Normalansicht, eine Standardansicht oder eine beliebige Anzahl von personalisierte Ansichten geöffnet werden. Eine Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird. Die Normalansicht wird verwendet, wenn keine alternativen Ansicht vorhanden ist und wenn Sie den Ordner zum ersten Mal öffnen. Wenn Sie eine alternative Ansicht vorhanden ist, müssen Sie es zum Öffnen des Ordners verwenden.
  
Eine Ansicht wird in einer Nachricht als ein Deskriptor Ansicht bezeichnet beschrieben. Ansicht Deskriptoren werden in der Regel als zugeordneten Nachrichten erstellt und in den allgemeinen oder persönliche Ansicht-Ordnern oder in einem Ordner IPM können angezeigt werden.
  
### <a name="to-open-a-view-descriptor"></a>Eine Beschreibung der Ansicht öffnen
  
1. Rufen Sie [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) zum Abrufen des zugehörigen Inhaltsverzeichnisses für den Ordner. 
    
2. Erstellen Sie eine Beschränkung, der nur Nachrichten mit der Nachrichtenklasse für die Ansicht Deskriptoren reserviert ermittelt und rufen Sie die [Methode IMAPITable:: Restrict](imapitable-restrict.md) zur Begrenzung der Tabelle und [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen der entsprechenden Zeilen, oder...
    
   Rufen Sie den Ordner [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** enthält die Eintrags-ID für die Nachricht mit der standardmäßigen Ansicht Deskriptor für einen Ordner. Dieser Aufruf erfolgreich, wenn der Ordner die Verwendung des MAPI_ASSOCIATED-Flags für Aufrufe von [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)unterstützt.
    
3. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) , wobei die Eintrags-ID der Ansicht Deskriptor zu öffnen. 
    

