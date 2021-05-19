---
title: Löschen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433164"
---
# <a name="deleting-a-message"></a>Löschen einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann eine Nachricht löschen, wenn sie geöffnet ist und der Benutzer sie liest, oder wenn sie geschlossen ist und der Benutzer die Inhaltstabelle anschaut. Um einen Benutzer vor versehentlichem Entfernen einer Nachricht zu schützen, definiert MAPI das Löschen von Nachrichten als zwei Schritte:
  
1. Markieren Sie eine Nachricht zum Löschen, indem Sie sie in den Ordner verschieben, der als Ordner "Gelöschte Elemente" festgelegt wurde – dem Ordner, dessen Eintrags-ID in der **eigenschaft PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) gespeichert ist. 
    
2. Entfernen Sie die Nachricht, indem Sie die [IMAPIFolder::D eleteMessages-Methode](imapifolder-deletemessages.md) aufrufen. 
    
Wenn ein Benutzer eine Nachricht in einem anderen Ordner als dem Ordner "Gelöschte Elemente" löschen will, markieren Sie sie zum Löschen. Nur wenn ein Benutzer Nachrichten aus dem Ordner Gelöschte Elemente auswählt, sollten die Nachrichten physisch von der Arbeitsstation entfernt werden. Sie können den Benutzer dazu aufgefordert, zu überprüfen, ob der Benutzer wirklich beabsichtigt hat, den Löschvorgang durchzuführen.
  
 **So löschen Sie eine Nachricht**
  
1. Bestätigen Sie mit dem Benutzer, dass der bevorstehende Löschvorgang beabsichtigt ist.
    
2. Bestimmen Sie das übergeordnete Element des zu löschenden Ordners. Wenn es sich um den Ordner "Gelöschte Elemente" oder einen Unterordner im Ordner "Gelöschte Elemente" handelt, rufen Sie [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) auf, um die Nachricht zu entfernen. 
    
3. Wenn der Ordner nicht im Ordner "Gelöschte Elemente" enthalten ist, rufen Sie [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) auf, deren MESSAGE_MOVE festgelegt ist, um die Nachricht in den Ordner "Gelöschte Elemente" zu verschieben. 
    

