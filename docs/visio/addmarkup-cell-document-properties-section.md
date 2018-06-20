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
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796399"
---
# <a name="addmarkup-cell-document-properties-section"></a>AddMarkup Cell (Document Properties Section)

Gibt an, ob das Dokument für ein Markup überprüft wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|WAHR  <br/> |Dokument wird überprüft.  <br/> |
|FALSCH  <br/> |Dokument wird nicht überprüft (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Zelle auf true festgelegt ist, der Prüfer festgelegt ist AddMarkup ist gelten Hinzufügen von Markup und Änderungen für Markup Überlagerung Seiten, nicht auf das ursprüngliche Zeichenblätter. Wenn die Zelle AddMarkup Markup nachverfolgen "false" ist ist deaktiviert, und Änderungen auf die ursprüngliche Zeichenblätter angewendet werden.
  
> [!NOTE]
> Sie können auf Ihre Dokumente Markup verhindern, mithilfe der GUARD-Funktion. Wenn die Zelle AddMarkup die Formel =Guard(falsch), der Befehl **Markup verfolgen** ist deaktiviert. 
  
Diese Einstellung entspricht der Einstellung **Markup verfolgen** den Befehl in der Gruppe **Markup** der Registerkarte **Überprüfen** . 
  
Wenn Sie einen Verweis auf die Zelle AddMarkup nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |AddMarkup  <br/> |
   
Wenn Sie einen Verweis auf die Zelle AddMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocAddMarkup** <br/> |
   

