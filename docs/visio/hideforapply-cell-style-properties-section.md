---
title: Zelle "HideForApply" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
ms.localizationpriority: medium
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Bestimmt, wo eine Formatvorlage auf der Benutzeroberfläche von Microsoft Visio angezeigt wird.
ms.openlocfilehash: 18750f8191d468483b63f7e076ada1b4cd2072f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570491"
---
# <a name="hideforapply-cell-style-properties-section"></a>Zelle "HideForApply" (Abschnitt "Style Properties")

Bestimmt, wo eine Formatvorlage auf der Benutzeroberfläche von Microsoft Visio angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Formatvorlage nur im **Zeichnungsexplorer** anzeigen.  <br/> |
| FALSE  <br/> | Formatvorlage im **Zeichnungsexplorer** anzeigen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie eine neue Formatvorlage auf der Grundlage einer ausgeblendeten Formatvorlage erstellen, erbt die neue Formatvorlage dieses Attribut nicht.
  
Um einen Verweis auf die Zelle "HideForApply" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | HideForApply  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "HideForApply" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowStyle** <br/> |
| Zellenindex:  <br/> |**visStyleHidden** <br/> |
   

