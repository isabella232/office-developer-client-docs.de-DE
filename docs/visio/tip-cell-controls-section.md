---
title: Zelle "Tip" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307721"
---
# <a name="tip-cell-controls-section"></a>Zelle "Tip" (Abschnitt "Controls")

Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Tip aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . Tipwhere-Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Tip aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlTip** <br/> |
   

