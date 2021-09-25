---
title: Implementieren von Standardformularverben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a85a3adcd2fab920e9cbbd39bdd7a5ad52f223db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600834"
---
# <a name="implementing-standard-form-verbs"></a>Implementieren von Standardformularverben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von Standardverben oder Aktionen, die ausgeführt werden, wenn ein Benutzer eine Menüauswahl vornimmt oder auf eine Schaltfläche klickt, die von allen Formularviewern unterstützt werden sollen. Jedem Verb ist zur Identifizierung eine Konstante zugeordnet, die im EXCHFORM definiert ist. H-Headerdatei. In der folgenden Tabelle sind die Standardformularverben und die zugehörigen Konstanten aufgeführt:
  
|**Verb**|**Wert**|
|:-----|:-----|
|Öffnen  <br/> |EXCHIVERB_OPEN  <br/> |
|Antworten  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Allen antworten  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Weiterleiten  <br/> |EXCHIVERB_FORWARD  <br/> |
|Drucken  <br/> |EXCHIVERB_PRINT  <br/> |
|Speichern unter  <br/> |EXCHIVERB_SAVEAS  <br/> |
|In Ordner antworten  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Wenn ein Benutzer ein Verb auswählt, übergeben Sie seine Konstante in einem Aufruf an die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formulars, um die entsprechende Aktion auszuführen. 
  
Zusätzlich zum Zugriff auf Verben über die Formularanzeige können Benutzer manchmal direkt über das Formular auf Verben zugreifen. Bei einigen Formularobjekten kann der Benutzer beispielsweise das Verb **"Drucken"** aufrufen, indem er mit der rechten Maustaste auf das Formular klickt und in einem kontextabhängigen Menü **"Drucken"** auswählt. 
  

