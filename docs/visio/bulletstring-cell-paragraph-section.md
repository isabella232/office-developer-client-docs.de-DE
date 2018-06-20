---
title: Zelle "BulletString" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796571"
---
# <a name="bulletstring-cell-paragraph-section"></a>BulletString Cell (Paragraph Section)

Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen. 
  
## <a name="remarks"></a>Bemerkungen

Geben Sie die Formatvorlage in Form einer Zeichenfolge (eingeschlossen in Anführungszeichen) ein. Sie können beispielsweise die Zeichenfolge "ooo" eingeben.
  
Sie können auch den Wert dieser Zelle durch Festlegen der rechten Maustaste auf ein Shape klicken, auf **Format**, auf **Text**klicken und dann auf die Registerkarte **Aufzählungszeichen** zeigen. 
  
Zum Abrufen eines Verweises auf die Zelle BulletString nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para.BulletStr [ *i* ] wobei *i* = < 1 >, 2, 3,...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BulletString aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visBulletString** <br/> |
   

