---
title: Zelle "Value" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Enthält die Funktion für ein Feld.
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798372"
---
# <a name="value-cell-text-fields-section"></a>Value Cell (Text Fields Section)

Enthält die Funktion für ein Feld.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle im Dialogfeld **Feld** festlegen (klicken Sie auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld**).
  
Wenn Sie einen Verweis auf die Zelle Value nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Fields.Value [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Value aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
|Zeilenindex:  <br/> |**VisRowField** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFieldCell** <br/> |
   

