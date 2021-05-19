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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435362"
---
# <a name="selectmode-cell-group-properties-section"></a>Zelle "SelectMode" (Abschnitt "Group Properties")

Bestimmt, wie Sie ein Gruppen-Shape und dessen Mitglieder auswählen.
  
|**Wert**|**Auswahlmodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nur das Gruppen-Shape auswählen.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Das Gruppen-Shape zuerst auswählen.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Mitglieder der Gruppe zuerst auswählen.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert  auch im Dialogfeld Verhalten festlegen (wenn [](run-in-developer-mode-display-the-developer-tab.md) die Gruppenform ausgewählt ist, klicken Sie auf der Registerkarte  Entwickler in der **Gruppe Shape-Entwurf** auf **Verhalten,** und klicken Sie dann unter Gruppenverhalten auf einen Modus in der Liste **Auswahl).** 
  
Um einen Verweis auf die Zelle SelectMode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |SelectMode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SelectMode nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupSelectMode** <br/> |
   

