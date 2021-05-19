---
title: Zelle "AddMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Gibt an, ob das Dokument für ein Markup überprüft wird.
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427633"
---
# <a name="addmarkup-cell-document-properties-section"></a>Zelle "AddMarkup" (Abschnitt "Document Properties")

Gibt an, ob das Dokument für ein Markup überprüft wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Dokument wird überprüft.  <br/> |
|FALSE  <br/> |Dokument wird nicht überprüft (Standard).  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die Zelle AddMarkup auf WAHR festgelegt ist, fügt der Prüfer das Markup hinzu, und die Änderungen werden auf Markupüberlagerungsseiten angewendet, nicht auf die ursprünglichen Zeichenblätter. Wenn die Zelle AddMarkup auf FALSE festgelegt ist, ist die Markupverfolgung deaktiviert, und die Änderungen werden auf die ursprünglichen Zeichenblätter angewendet.
  
> [!NOTE]
> Sie können Markup für Ihre Dokumente mithilfe der GUARD-Funktion verhindern. Wenn die Zelle AddMarkup die Formel =GUARD(FALSE) enthält, ist der **Befehl Markup** nachverfolgen deaktiviert. 
  
Diese Einstellung entspricht der Einstellung für den Befehl **Änderungen markieren** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Verwenden Sie zum Erhalten eines Verweises auf die AddMarkup-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |AddMarkup  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die AddMarkup-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocAddMarkup** <br/> |
   

