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
  
Ausgehende Nachrichten können nach dem Senden im Ordner "Posteingang" bleiben, in einen Ordner verschoben werden, der zum Speichern gesendeter Nachrichten bestimmt ist, oder gelöscht werden. Die Art der Verarbeitung hängt davon ab, ob Sie die Eigenschaften des Nachrichtenspeichers festgelegt haben:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die auf TRUE festgelegt ist, wenn Nachrichten nach dem Senden gelöscht werden sollen, andernfalls FALSE. **PR_SENTMAIL_ENTRYID** ist die Eintrags-ID eines Ordners. Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner verschieben, der durch diese Eintrags-ID dargestellt wird. Die gespeicherten Nachrichten haben in der Regel die Identität des letzten Nachrichtenspeichers oder Transportanbieters, der sie senden soll. 
  
Entweder die eine oder die andere oder keine dieser Eigenschaften sollte festgelegt werden, aber nicht beides. Wenn Sie jedoch **eine** PR_SENTMAIL_ENTRYID, muss sie einen gültigen Eintragsbezeichner enthalten. 
  
In der folgenden Tabelle wird beschrieben, wie sich diese Eigenschaften auf das, was Sie mit gesendeten Nachrichten tun, auswirken.
  
|||
|:-----|:-----|
|Wenn keine eigenschaft festgelegt ist:  <br/> |Lassen Sie die Nachricht im Ordner, aus dem sie gesendet wurde (in der Regel der Posteingang).  <br/> |
|Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner.  <br/> |
|Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:  <br/> |Löschen Sie die Nachricht.  <br/> |
   

