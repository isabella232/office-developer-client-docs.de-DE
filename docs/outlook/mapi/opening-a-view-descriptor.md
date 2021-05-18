---
title: Öffnen einer Ansichtsbeschreibung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413038"
---
# <a name="opening-a-view-descriptor"></a>Öffnen einer Ansichtsbeschreibung
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Ordner können mit einer normalen Ansicht, einer Standardansicht oder einer beliebigen Anzahl personalisierter Ansichten geöffnet werden. In einer Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird. Die Normalansicht wird verwendet, wenn es keine alternative Ansicht gibt und Sie den Ordner zum ersten Mal öffnen. Wenn eine alternative Ansicht vorhanden ist, müssen Sie sie zum Öffnen des Ordners verwenden.
  
Eine Ansicht wird in einer Meldung beschrieben, die als Ansichtsdeskriptor bezeichnet wird. Ansichtsdeskriptoren werden in der Regel als zugeordnete Nachrichten erstellt und können entweder in den allgemeinen oder persönlichen Ansichtsordnern oder in einem beliebigen IPM-Ordner angezeigt werden.
  
### <a name="to-open-a-view-descriptor"></a>So öffnen Sie einen Ansichtsdeskriptor
  
1. Rufen [Sie IMAPIContainer::GetContentsTable auf,](imapicontainer-getcontentstable.md) um die zugeordnete Inhaltstabelle für den Ordner abzurufen. 
    
2. Erstellen Sie eine Einschränkung, die nur Nachrichten mit der Nachrichtenklasse sucht, die für Ansichtsdeskriptoren reserviert ist, und rufen Sie [IMAPITable::Restrict](imapitable-restrict.md) auf, um die Tabelle und [IMAPITable::QueryRows](imapitable-queryrows.md) einzuschränken, um die entsprechenden Zeilen abzurufen, oder...
    
   Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Ordners auf, um die **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) abzurufen. **PR_DEFAULT_VIEW_ENTRYID** enthält die Eintrags-ID für die Nachricht, die den Standardansichtsdeskriptor für einen Ordner enthält. Dieser Aufruf ist erfolgreich, wenn der Ordner die Verwendung des MAPI_ASSOCIATED für Aufrufe von [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::GetContentsTable unterstützt.](imapicontainer-getcontentstable.md)
    
3. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) mit dem Eintragsbezeichner des Ansichtsdeskriptors auf, um ihn zu öffnen. 
    

