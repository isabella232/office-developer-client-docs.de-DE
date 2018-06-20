---
title: Verarbeiten einer gesendeten Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795300"
---
# <a name="processing-a-sent-message"></a>Verarbeiten einer gesendeten Nachricht

  
  
**Betrifft**: Outlook 
  
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
   

