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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338633"
---
# <a name="addmarkup-cell-document-properties-section"></a>Zelle "AddMarkup" (Abschnitt "Document Properties")

Gibt an, ob das Dokument für ein Markup überprüft wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Dokument wird überprüft.  <br/> |
|FALSE  <br/> |Dokument wird nicht überprüft (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Zelle AddMarkup auf WAHR festgelegt ist, fügt der Prüfer das Markup hinzu, und die Änderungen werden auf Markupüberlagerungsseiten angewendet, nicht auf die ursprünglichen Zeichenblätter. Wenn die Zelle AddMarkup auf FALSE festgelegt ist, ist die Markupverfolgung deaktiviert, und die Änderungen werden auf die ursprünglichen Zeichenblätter angewendet.
  
> [!NOTE]
> Sie können das Markup in Ihren Dokumenten mithilfe der GUARD-Funktion verhindern. Wenn die Zelle addMarkup die Formel = GUARD (FALSE) enthält, ist der Befehl **Markup verfolgen** deaktiviert. 
  
Diese Einstellung entspricht der Einstellung für den Befehl **Änderungen markieren** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Wenn Sie einen Verweis auf die Zelle addMarkup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"AddMarkup  <br/> |
   
Wenn Sie einen Verweis auf die Zelle addMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocAddMarkup** <br/> |
   

