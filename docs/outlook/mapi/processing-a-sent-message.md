---
title: Verarbeiten einer gesendeten Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434676"
---
# <a name="processing-a-sent-message"></a>Verarbeiten einer gesendeten Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ausgehende Nachrichten können, nachdem Sie gesendet wurden, im Ordner Postausgang hinterlassen, in einen Ordner verschoben werden, der für gesendete Nachrichten reserviert oder gelöscht wurde. Die Art der Verarbeitung hängt davon ab, ob Sie die Eigenschaften für den Nachrichtenspeicher festgelegt haben:
  
- **PR_DELETE_AFTER_SUBMIT** ([Pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([Pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die auf true festgelegt ist, wenn Nachrichten nach dem Senden gelöscht werden sollen, andernfalls false. **PR_SENTMAIL_ENTRYID** ist die Eintrags-ID eines Ordners. Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner verschieben, der durch diese Eintrags-ID dargestellt wird. Die gespeicherten Nachrichten weisen in der Regel die Identität des letzten Nachrichtenspeichers oder Transportanbieters auf, um Sie zu senden. 
  
Entweder die eine oder die andere oder keine dieser Eigenschaften sollte festgelegt werden, aber nicht beides. Wenn Sie jedoch **PR_SENTMAIL_ENTRYID**festlegen, muss es eine gültige Eintrags-ID enthalten. 
  
In der folgenden Tabelle wird beschrieben, wie sich diese Eigenschaften auf das Verhalten von gesendeten Nachrichten auswirken.
  
|||
|:-----|:-----|
|Wenn keine Eigenschaft festgelegt ist:  <br/> |BeLassen Sie die Nachricht in dem Ordner, von dem Sie gesendet wurde (in der Regel der Postausgang).  <br/> |
|Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner.  <br/> |
|Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:  <br/> |Löschen Sie die Nachricht.  <br/> |
   

