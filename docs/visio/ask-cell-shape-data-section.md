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
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796393"
---
# <a name="ask-cell-shape-data-section"></a>Zelle "Ask" (Abschnitt "Shape Data")

Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Auffordern Sie Benutzer zu Shape-Daten in das Dialogfeld **Shape-Daten definieren** einzugeben.  <br/> |
|FALSE  <br/> |Bitten Sie die Benutzer Daten eingeben nicht.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **beim Ablegen fragen** im Dialogfeld **Shape-Daten definieren** (mit der rechten Maustaste in des Shapes, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).
  
Zum Abrufen eines Verweises auf die Zelle Ask nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Eigenschaft. *Name* . Stellen Sie sicher, auf dem Prop.  *Name* ist der Name der Zeile mit der benutzerdefinierten Eigenschaft.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Ask aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visCustPropsAsk** <br/> |
   

