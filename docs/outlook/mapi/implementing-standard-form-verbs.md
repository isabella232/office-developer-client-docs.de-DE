---
title: Implementieren von standardmäßigen Formularverben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568749"
---
# <a name="implementing-standard-form-verbs"></a>Implementieren von standardmäßigen Formularverben

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von standardmäßigen Verben oder Aktionen ausgeführt, wenn ein Benutzer eine Menüauswahl im trifft oder auf eine Schaltfläche, die alle Formular-Viewer unterstützen soll. Jedes Verb hat, eine Konstante, die für die Identifikation in der EXCHFORM definierten zugeordnet wird. H-Headerdatei. Die folgende Tabelle enthält die Standardformular Verben und deren zugeordneten Konstanten:
  
|**Verb**|**Wert**|
|:-----|:-----|
|Öffnen  <br/> |EXCHIVERB_OPEN  <br/> |
|Antworten  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Allen antworten  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Forward  <br/> |EXCHIVERB_FORWARD  <br/> |
|Drucken  <br/> |EXCHIVERB_PRINT  <br/> |
|Speichern als  <br/> |EXCHIVERB_SAVEAS  <br/> |
|In Ordner antworten  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Wenn ein Benutzer ein Verb auswählt, übergeben Sie die Konstante in einen Anruf an das Formular [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode zum Ausführen der entsprechenden Aktion. 
  
Benutzer können über Ihr Formular Viewer auf Verben zugreifen, Verben manchmal direkt aus dem Formular zugreifen. Beispielsweise Benutzer einige Formularobjekte sollen das Verb **Drucken** aufrufen, indem Sie mit der rechten Maustaste auf das Formular, und wählen Sie **Drucken** aus einem Kontextmenü. 
  

