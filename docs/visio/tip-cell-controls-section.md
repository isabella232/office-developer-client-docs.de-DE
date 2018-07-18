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
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798287"
---
# <a name="tip-cell-controls-section"></a>Tip Cell (Controls Section)

Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn ein Benutzer den Mauszeiger über dem Steuerpunkt eines Shapes platziert. Die Anwendung schließt diese Beschreibung in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden in der QuickInfo nicht angezeigt.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Tip aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . Tipwhere-Steuerelemente.  *Name* ist der Name der Zeile mit Steuerelementen.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Tip aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**VisRowControl** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlTip** <br/> |
   

