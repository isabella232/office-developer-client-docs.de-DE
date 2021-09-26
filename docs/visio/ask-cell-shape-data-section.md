---
title: Zelle "Ask" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
ms.localizationpriority: medium
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
ms.openlocfilehash: a6d588721f34426a7af60e09ca5d1c463d1b5d77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608662"
---
# <a name="ask-cell-shape-data-section"></a>Zelle "Ask" (Abschnitt "Shape Data")

Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Benutzer wird aufgefordert, Shape-Daten in das Dialogfeld **Shape-Daten definieren** einzugeben.  <br/> |
|FALSE  <br/> |Benutzer nicht zur Dateneingabe auffordern.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Beim Ablegen fragen** im Dialogfeld **Shape-Daten definieren**. (Klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**.)
  
Um einen Verweis auf die Zelle "Ask" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Prop. *name*  . Überprüfen Sie, wo Prop.  *name*  is the name of the custom property row.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Ask anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visCustPropsAsk** <br/> |
   

