---
title: ConnectorSchemeIndex Cell (Theme Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48ab98bd-2966-443c-b3db-befeb271550f
description: Bestimmt das Verbinder-Schema eines Designs, das auf die Form angewendet wird, als ganze Zahl.
ms.openlocfilehash: 77d16632db63d187477ba62a1a6f4b9319e156fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319712"
---
# <a name="connectorschemeindex-cell-theme-properties-section"></a>ConnectorSchemeIndex Cell (Theme Properties section)

Bestimmt das Verbinder-Schema eines Designs, das auf die Form angewendet wird, als ganze Zahl. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ConnectorSchemeIndex** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConnectorSchemeIndex  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ConnectorSchemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowThemeProperties** <br/> |
| Zellenindex:  <br/> |* * visConnectorSchemeIndex * * <br/> |
   

