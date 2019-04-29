---
title: Implementieren von Standard mäßigen Formular Verben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426121"
---
# <a name="implementing-standard-form-verbs"></a>Implementieren von Standard mäßigen Formular Verben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von Standardverben oder Aktionen, die ausgeführt werden, wenn ein Benutzer eine Menüauswahl vornimmt oder auf eine Schaltfläche klickt, die von allen Formular Betrachtern unterstützt werden sollte. Jedem Verb ist eine Konstante zugeordnet, die in der EXCHFORM definiert ist. H-Headerdatei. In der folgenden Tabelle sind die standardmäßigen Verben und die zugehörigen Konstanten aufgeführt:
  
|**Verb**|**Wert**|
|:-----|:-----|
|Öffnen  <br/> |EXCHIVERB_OPEN  <br/> |
|Antworten  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Allen antworten  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Weiterleiten  <br/> |EXCHIVERB_FORWARD  <br/> |
|Print  <br/> |EXCHIVERB_PRINT  <br/> |
|Speichern unter  <br/> |EXCHIVERB_SAVEAS  <br/> |
|In Ordner antworten  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Wenn ein Benutzer ein Verb auswählt, übergibt seine Konstante in einem Aufruf an die [IMAPIForm::D overb](imapiform-doverb.md) -Methode des Formulars, um die entsprechende Aktion auszuführen. 
  
Zusätzlich zum Zugreifen auf Verben über den Formular Betrachter können Benutzer manchmal direkt über das Formular auf Verben zugreifen. Einige Formularobjekte ermöglichen es dem Benutzer beispielsweise, das **Druck** -Verb aufzurufen, indem Sie mit der rechten Maustaste auf das Formular klicken und im kontextabhängigen Menü **Drucken** auswählen. 
  

