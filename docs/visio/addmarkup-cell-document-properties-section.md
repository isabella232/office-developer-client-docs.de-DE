---
title: Zelle "AddMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
ms.localizationpriority: medium
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Gibt an, ob das Dokument für ein Markup überprüft wird.
ms.openlocfilehash: f97dc836d7307c8a35fe0db8f1cd73035c52ac94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560151"
---
# <a name="addmarkup-cell-document-properties-section"></a>Zelle "AddMarkup" (Abschnitt "Document Properties")

Gibt an, ob das Dokument für ein Markup überprüft wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Dokument wird überprüft.  <br/> |
|FALSE  <br/> |Dokument wird nicht überprüft (Standard).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Zelle AddMarkup auf WAHR festgelegt ist, fügt der Prüfer das Markup hinzu, und die Änderungen werden auf Markupüberlagerungsseiten angewendet, nicht auf die ursprünglichen Zeichenblätter. Wenn die Zelle AddMarkup auf FALSE festgelegt ist, ist die Markupverfolgung deaktiviert, und die Änderungen werden auf die ursprünglichen Zeichenblätter angewendet.
  
> [!NOTE]
> Sie können Markup für Ihre Dokumente mithilfe der GUARD-Funktion verhindern. Wenn die Zelle AddMarkup die Formel =GUARD(FALSE) enthält, ist der Befehl **"Markup nachverfolgen"** deaktiviert. 
  
Diese Einstellung entspricht der Einstellung für den Befehl **Änderungen markieren** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Um einen Verweis auf die Zelle "AddMarkup" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |AddMarkup  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "AddMarkup" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocAddMarkup** <br/> |
   

