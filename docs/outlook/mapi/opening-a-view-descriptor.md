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
  
Viele Ordner können mit einer Normalansicht, einer Standardansicht oder einer beliebigen Anzahl von personalisierten Ansichten geöffnet werden. In einer Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird. Die Normalansicht wird verwendet, wenn keine Alternative Ansicht vorhanden ist und Sie den Ordner zum ersten Mal öffnen. Wenn eine Alternative Ansicht vorhanden ist, müssen Sie Sie verwenden, um den Ordner zu öffnen.
  
Eine Ansicht wird in einer Nachricht beschrieben, die als Ansichts Deskriptor bezeichnet wird. Ansichts Deskriptoren werden in der Regel als zugeordnete Nachrichten erstellt und können in den Ordnern allgemeine oder persönliche Ansicht oder in einem beliebigen IPM-Ordner angezeigt werden.
  
### <a name="to-open-a-view-descriptor"></a>So öffnen Sie einen Ansichts Deskriptor
  
1. Rufen Sie [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable auf, um die zugeordnete Inhaltstabelle für den Ordner abzurufen. 
    
2. Erstellen Sie eine Einschränkung, die nur Nachrichten sucht, deren Nachrichtenklasse für Ansichts Deskriptoren reserviert ist, und rufen Sie [IMAPITable:: Restrict](imapitable-restrict.md) auf, um die Tabelle zu begrenzen, und [IMAPITable:: QueryRows](imapitable-queryrows.md) , um die entsprechenden Zeilen abzurufen, oder...
    
   Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Ordners auf, um die zugehörige **PR_DEFAULT_VIEW_ENTRYID** ([pidtagdefaultviewentryid (](pidtagdefaultviewentryid-canonical-property.md))-Eigenschaft abzurufen. **PR_DEFAULT_VIEW_ENTRYID** enthält die Eintrags-ID für die Nachricht, die den Standard Ansichts Deskriptor für einen Ordner enthält. Dieser Aufruf kann erfolgreich ausgeführt werden, wenn der Ordner die Verwendung des MAPI_ASSOCIATED-Flags für Aufrufe von [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontentable unterstützt.
    
3. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit der Eintrags-ID des Ansichts Deskriptors auf, um Sie zu öffnen. 
    

