---
title: Löschen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c8d46ac6f47eb4dc68aebfa4562403ef1b738213
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791518"
---
# <a name="deleting-a-message"></a>Löschen einer Nachricht

  
  
**Betrifft**: Outlook 
  
Ein Client kann eine Nachricht löschen, wenn es geöffnet ist und der Benutzer ist es lesen oder wenn es geschlossen wird, und der Benutzer wird die Inhaltstabelle anzeigen. Um ein Benutzer eine Nachricht versehentlich entfernen zu schützen, definiert MAPI Löschen von Nachrichten als zwei Schritten zusammen:
  
1. Markieren Sie eine Nachricht zum Löschen, indem Sie in den Ordner, die als den Ordner Gelöschte Objekte festgelegt wurde verschoben – Ordners, dessen Eintrags-ID in der **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft gespeichert ist. 
    
2. Entfernen Sie die Meldung durch Aufrufen der Methode [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) . 
    
Wenn ein Benutzer beschließt, eine Nachricht in einem anderen Ordner als dem Ordner Gelöschte Objekte löschen, markieren Sie es zum Löschen. Nur, wenn ein Benutzer Nachrichten von in den Ordner Gelöschte Elemente auswählt sollten die Nachrichten physisch aus der Arbeitsstation entfernt werden. Sie können der Benutzer aufgefordert, stellen Sie sicher, dass der Benutzer wirklich für die direkte Verwendung den Löschvorgang ausführen.
  
 **So löschen Sie eine Nachricht**
  
1. Bestätigen Sie mit dem Benutzer, dass der Löschvorgang bevorstehenden beabsichtigt ist.
    
2. Bestimmen Sie das übergeordnete Element des Ordners gelöscht werden soll. Wenn sie den Ordner Gelöschte Objekte oder einen Unterordner im Ordner Gelöschte Elemente ist, rufen Sie [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) , um die Nachricht zu entfernen. 
    
3. Wenn der Ordner nicht in den Ordner Gelöschte Objekte enthalten ist, rufen Sie [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) mit der MESSAGE_MOVE-Flag, die Nachricht in den Ordner Gelöschte Elemente zu verschieben. 
    

