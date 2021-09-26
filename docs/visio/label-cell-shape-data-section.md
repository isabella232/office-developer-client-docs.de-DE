---
title: Zelle "Label" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
ms.localizationpriority: medium
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).
ms.openlocfilehash: 352e113e685a4952f31334947f81d16b0358f375
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618721"
---
# <a name="label-cell-shape-data-section"></a>Zelle "Label" (Abschnitt "Shape Data")

Legt die Beschriftung fest, die Benutzern im Fenster **Shape-Daten** angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_). 
  
## <a name="remarks"></a>Bemerkungen

Die Anwendung schließt die Beschriftungszeichenfolge in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden im Fenster **Shape-Daten** nicht angezeigt. 
  
Wenn kein Beschriftungstext gefunden wird, zeigt Visio den Zeilennamen (Prop.Row) im **Shape-Datenfenster an.** 
  
Um einen Verweis auf die Zelle "Label" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Prop. *Name*  . Beschriftung, wobei Prop.  *Name*  ist der Zeilenname  <br/> |
   
Um einen Verweis auf die Zelle "Label" anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCustPropsLabel** <br/> |
   

