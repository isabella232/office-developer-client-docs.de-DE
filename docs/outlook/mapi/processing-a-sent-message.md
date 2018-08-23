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
ms.openlocfilehash: bd86e5d06e868ebc540d8eb779c059089045cd8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574181"
---
# <a name="processing-a-sent-message"></a>Verarbeiten einer gesendeten Nachricht

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ausgehende Nachrichten, nachdem sie gesendet wurden, kann im Postausgang bleiben gesendete Nachrichten-Ordner, in einen Ordner gehalten festgelegte verschoben oder gelöscht. Die Art der Verarbeitung hängt davon ab, unabhängig davon, ob Sie die Nachricht Speichereigenschaften festgelegt haben:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die andernfalls true zurück, wenn Nachrichten gelöscht werden soll, nachdem sie gesendet werden, und FALSE festgelegt. **PR_SENTMAIL_ENTRYID** ist die Eintrags-ID eines Ordners. Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner, die von diesem Eintrag Bezeichner dargestellte verschieben. Die gespeicherten Nachrichten in der Regel haben die Identität des letzten Nachrichtenspeichers oder transport-Anbieter dies veranlassen. 
  
Entweder der anderen, oder keine dieser Eigenschaften sollte Set, jedoch nicht beide. Wenn Sie **PR_SENTMAIL_ENTRYID**festlegen, muss es einen gültigen Eintrag Bezeichner enthalten. 
  
In der folgenden Tabelle wird beschrieben, wie diese Eigenschaften auswirken, was Sie mit gesendete Nachrichten machen.
  
|||
|:-----|:-----|
|Wenn weder-Eigenschaft festgelegt ist:  <br/> |Lassen Sie die Nachricht in den Ordner, von dem sie (in der Regel im Ordner Postausgang) gesendet wurde.  <br/> |
|Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:  <br/> |Verschieben der Nachricht in den angegebenen Ordner.  <br/> |
|Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:  <br/> |Löschen der Nachricht.  <br/> |
   

