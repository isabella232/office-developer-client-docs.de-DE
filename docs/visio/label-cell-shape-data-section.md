---
title: Zelle "Label" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Gibt die Beschriftung, die für Benutzer im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich des Unterstrich (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797257"
---
# <a name="label-cell-shape-data-section"></a>Label Cell (Shape Data Section)

Gibt die Beschriftung, die für Benutzer im Fenster **Shape-Daten** angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich des Unterstrich (_). 
  
## <a name="remarks"></a>Hinweise

Die Anwendung schließt die Beschriftungszeichenfolge automatisch in Anführungszeichen in der Zelle, aber diese Anführungszeichen werden im Fenster **Shape-Daten** nicht angezeigt. 
  
Wird kein Beschriftungstext gefunden wird, zeigt Visio den Zeilennamen (Prop.Row) im Fenster **Shape-Daten** an. 
  
Wenn Sie einen Verweis auf die Zelle Label nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Eigenschaft. *Name* . Beschriftung wobei Prop.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Label aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCustPropsLabel** <br/> |
   

