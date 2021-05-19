---
title: Zelle "Ask" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426864"
---
# <a name="ask-cell-shape-data-section"></a>Zelle "Ask" (Abschnitt "Shape Data")

Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Benutzer wird aufgefordert, Shape-Daten in das Dialogfeld **Shape-Daten definieren** einzugeben.  <br/> |
|FALSE  <br/> |Benutzer nicht zur Dateneingabe auffordern.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Beim Ablegen fragen** im Dialogfeld **Shape-Daten definieren**. (Klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**.)
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Ask anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Prop. *Name*  . Überprüfen Sie, wo Prop.  *name*  ist der Name der benutzerdefinierten Eigenschaftenzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Ask nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**visRowProp**  +   *i,* *wobei i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visCustPropsAsk** <br/> |
   

