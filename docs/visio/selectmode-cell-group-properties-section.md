---
title: Zelle "SelectMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
ms.localizationpriority: medium
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.
ms.openlocfilehash: e98e900afa6a6ca1ca166a08615c266c88df5457
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559619"
---
# <a name="selectmode-cell-group-properties-section"></a>Zelle "SelectMode" (Abschnitt "Group Properties")

Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.
  
|**Wert**|**Auswahlmodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nur das Gruppen-Shape auswählen.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Das Gruppen-Shape zuerst auswählen.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Mitglieder der Gruppe zuerst auswählen.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch im Dialogfeld **"Verhalten"** festlegen (wobei das Gruppen-Shape auf der Registerkarte ["Entwickler"](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **"Shape-Entwurf"** ausgewählt ist, klicken Sie auf **"Verhalten",** und klicken Sie dann in der **Auswahlliste** unter **"Gruppenverhalten"** auf einen Modus). 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "SelectMode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Selectmode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "SelectMode" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupSelectMode** <br/> |
   

