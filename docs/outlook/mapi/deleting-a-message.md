---
title: Löschen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc8f6886f324f38d195f79727af0f0542e8534cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556805"
---
# <a name="deleting-a-message"></a>Löschen einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann eine Nachricht löschen, wenn sie geöffnet ist und der Benutzer sie liest oder wenn sie geschlossen wird und der Benutzer das Inhaltsverzeichnis anzeigt. Um einen Benutzer vor dem versehentlichen Entfernen einer Nachricht zu schützen, definiert MAPI das Löschen von Nachrichten als zwei Schritte:
  
1. Markieren Sie eine Nachricht zum Löschen, indem Sie sie in den Ordner verschieben, der als Ordner "Gelöschte Elemente" festgelegt wurde – den Ordner, dessen Eintragsbezeichner in der **eigenschaft PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) gespeichert ist. 
    
2. Entfernen Sie die Nachricht, indem Sie die [IMAPIFolder::D eleteMessages-Methode](imapifolder-deletemessages.md) aufrufen. 
    
Wenn ein Benutzer eine Nachricht in einem anderen Ordner als dem Ordner "Gelöschte Elemente" löscht, markieren Sie sie zum Löschen. Nur wenn ein Benutzer Nachrichten aus dem Ordner "Gelöschte Elemente" auswählt, sollten die Nachrichten physisch von der Arbeitsstation entfernt werden. Sie können den Benutzer auffordern, zu überprüfen, ob der Benutzer den Löschvorgang wirklich durchführen wollte.
  
 **So löschen Sie eine Nachricht**
  
1. Bestätigen Sie mit dem Benutzer, dass der bevorstehende Löschvorgang beabsichtigt ist.
    
2. Bestimmen Sie das übergeordnete Element des zu löschenden Ordners. Wenn es sich um den Ordner "Gelöschte Elemente" oder einen Unterordner im Ordner "Gelöschte Elemente" handelt, rufen Sie [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) auf, um die Nachricht zu entfernen. 
    
3. Wenn der Ordner nicht im Ordner "Gelöschte Elemente" enthalten ist, rufen Sie [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) auf, wobei das flag MESSAGE_MOVE festgelegt ist, um die Nachricht in den Ordner "Gelöschte Elemente" zu verschieben. 
    

