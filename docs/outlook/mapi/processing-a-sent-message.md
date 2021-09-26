---
title: Verarbeiten einer gesendeten Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 969977764539c05735704f9bceea45c2c84036e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624405"
---
# <a name="processing-a-sent-message"></a>Verarbeiten einer gesendeten Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ausgehende Nachrichten können, nachdem sie gesendet wurden, im Ordner "Postausgang" abgelegt, in einen Ordner verschoben werden, der für gesendete Nachrichten vorgesehen ist, oder gelöscht werden. Die Art der Verarbeitung hängt davon ab, ob Sie die Nachrichtenspeichereigenschaften festgelegt haben:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die auf TRUE festgelegt ist, wenn Nachrichten nach dem Senden gelöscht werden sollen, und andernfalls FALSE. **PR_SENTMAIL_ENTRYID** ist der Eintragsbezeichner eines Ordners. Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner verschieben, der durch diesen Eintragsbezeichner dargestellt wird. Die gespeicherten Nachrichten haben in der Regel die Identität des letzten Nachrichtenspeichers oder Transportanbieters, der sie senden soll. 
  
Entweder eine oder die andere oder keine dieser Eigenschaften sollte festgelegt werden, jedoch nicht beide. Wenn Sie jedoch **PR_SENTMAIL_ENTRYID** festlegen, muss sie einen gültigen Eintragsbezeichner enthalten. 
  
In der folgenden Tabelle wird beschrieben, wie sich diese Eigenschaften auf die Aktionen bei gesendeten Nachrichten auswirken.
  
|||
|:-----|:-----|
|Wenn keine der beiden Eigenschaften festgelegt ist:  <br/> |Belassen Sie die Nachricht in dem Ordner, aus dem sie gesendet wurde (in der Regel der Postausgang).  <br/> |
|Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner.  <br/> |
|Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:  <br/> |Löschen Sie die Nachricht.  <br/> |
   

