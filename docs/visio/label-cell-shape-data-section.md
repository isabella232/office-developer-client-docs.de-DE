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
description: Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358751"
---
# <a name="label-cell-shape-data-section"></a>Zelle "Label" (Abschnitt "Shape Data")

Legt die Beschriftung fest, die Benutzern im Fenster **Shape-Daten** angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_). 
  
## <a name="remarks"></a>Bemerkungen

Die Anwendung schließt die Beschriftungszeichenfolge in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden im Fenster **Shape-Daten** nicht angezeigt. 
  
Wenn kein Bezeichnungstext gefunden wird, zeigt Visio im Fenster **Shape-Daten** den Zeilennamen (Prop. Row) an. 
  
Wenn Sie einen Verweis auf die Zelle Label aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Prop. *Name* . Bezeichnung, wobei Prop.  *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Label aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**visRowProp** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCustPropsLabel** <br/> |
   

