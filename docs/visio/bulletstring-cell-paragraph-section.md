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
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409748"
---
# <a name="bulletstring-cell-paragraph-section"></a>Zelle "BulletString" (Abschnitt "Paragraph")

Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen. 
  
## <a name="remarks"></a>Hinweise

Geben Sie die Formatvorlage in Form einer Zeichenfolge (eingeschlossen in Anführungszeichen) ein. Sie können beispielsweise die Zeichenfolge "ooo" eingeben.
  
Sie können den Wert für diese Zelle auch festlegen, indem Sie mit der rechten Maustaste auf ein Shape klicken, auf **Format** zeigen, auf **Text** klicken und dann die Registerkarte **Aufzählungszeichen** auswählen. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle BulletString anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para.BulletStr[ *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle BulletString nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visBulletString** <br/> |
   

