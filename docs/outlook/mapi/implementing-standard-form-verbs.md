---
title: Implementieren von Standardformularverben
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
# <a name="implementing-standard-form-verbs"></a>Implementieren von Standardformularverben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von Standardverben oder Aktionen, die von allen Formularbetrachtern unterstützt werden sollen, wenn ein Benutzer eine Menüauswahl vor nimmt oder auf eine Schaltfläche klickt. Jedem Verb ist eine Konstante zur Identifikation zugeordnet, die in EXCHFORM definiert ist. H-Headerdatei. In der folgenden Tabelle sind die Standardformularverben und die zugehörigen Konstanten aufgeführt:
  
|**Verb**|**Wert**|
|:-----|:-----|
|Öffnen  <br/> |EXCHIVERB_OPEN  <br/> |
|Reply  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Allen antworten  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Forward  <br/> |EXCHIVERB_FORWARD  <br/> |
|Drucken  <br/> |EXCHIVERB_PRINT  <br/> |
|Speichern unter  <br/> |EXCHIVERB_SAVEAS  <br/> |
|In Ordner antworten  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Wenn ein Benutzer ein Verb aus wählt, übergeben Sie seine Konstante in einem Aufruf an die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formulars, um die entsprechende Aktion durchzuführen. 
  
Neben dem Zugriff auf Verben über die Formularanzeige können Benutzer manchmal direkt über das Formular auf Verben zugreifen. Bei einigen Formularobjekten kann der Benutzer beispielsweise das **Verb Print** aufrufen, indem er mit der rechten Maustaste auf das Formular klickt und **in** einem kontextbezogenen Menü Drucken wählt. 
  

