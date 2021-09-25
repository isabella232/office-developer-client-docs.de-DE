---
title: Öffnen einer Ansichtsbeschreibung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d510d1f016da2214c46aadd918a7e3cae1804379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625147"
---
# <a name="opening-a-view-descriptor"></a>Öffnen einer Ansichtsbeschreibung
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Ordner können mit einer Normalansicht, einer Standardansicht oder einer beliebigen Anzahl von personalisierten Ansichten geöffnet werden. In einer Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird. Die Normalansicht wird verwendet, wenn keine alternative Ansicht vorhanden ist und Sie den Ordner zum ersten Mal öffnen. Wenn eine alternative Ansicht vorhanden ist, müssen Sie sie verwenden, um den Ordner zu öffnen.
  
Eine Ansicht wird in einer Meldung beschrieben, die als Ansichtsdeskriptor bezeichnet wird. Ansichtsdeskriptoren werden in der Regel als zugeordnete Nachrichten erstellt und können entweder in den allgemeinen oder persönlichen Ansichtsordnern oder in einem beliebigen IPM-Ordner angezeigt werden.
  
### <a name="to-open-a-view-descriptor"></a>So öffnen Sie einen Ansichtsdeskriptor
  
1. Rufen Sie [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) auf, um die zugeordnete Inhaltstabelle für den Ordner abzurufen. 
    
2. Erstellen Sie eine Einschränkung, die nur Nachrichten mit der Nachrichtenklasse sucht, die für Ansichtsdeskriptoren reserviert ist, und rufen Sie [IMAPITable::Restrict](imapitable-restrict.md) auf, um die Tabelle und [IMAPITable::QueryRows](imapitable-queryrows.md) einzuschränken, um die entsprechenden Zeilen abzurufen, oder...
    
   Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Ordners auf, um die **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) -Eigenschaft abzurufen. **PR_DEFAULT_VIEW_ENTRYID** enthält den Eintragsbezeichner für die Nachricht, die den Standardansichtsdeskriptor für einen Ordner enthält. Dieser Aufruf ist erfolgreich, wenn der Ordner die Verwendung des MAPI_ASSOCIATED Flags für Aufrufe von [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)unterstützt.
    
3. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) mit dem Eintragsbezeichner der Ansichtsbeschreibung auf, um sie zu öffnen. 
    

