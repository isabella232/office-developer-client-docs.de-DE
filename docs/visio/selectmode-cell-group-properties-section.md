---
title: Zelle "SelectMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326012"
---
# <a name="selectmode-cell-group-properties-section"></a>Zelle "SelectMode" (Abschnitt "Group Properties")

Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.
  
|**Wert**|**Auswahlmodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nur das Gruppen-Shape auswählen.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Das Gruppen-Shape zuerst auswählen.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Mitglieder der Gruppe zuerst auswählen.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Verhalten** festlegen (wenn das Gruppen-Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann in der **Auswahl** Liste Untergruppe auf einen Modus. ** Verhalten** ). 
  
Wenn Sie einen Verweis auf die Zelle "SelectMode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"SelectMode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "SelectMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupSelectMode** <br/> |
   

