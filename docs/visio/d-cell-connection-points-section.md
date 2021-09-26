---
title: Zelle "D" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
ms.localizationpriority: medium
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.
ms.openlocfilehash: 3db35be72fb80c7f08a751e961535403b5ceff8f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613016"
---
# <a name="d-cell-connection-points-section"></a>Zelle "D" (Abschnitt "Connection Points")

Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.
  
## <a name="remarks"></a>Bemerkungen

Um auf die Zelle D zuzugreifen, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern.** 
  
Um einen Verweis auf die Zelle D anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections.D[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle D anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visCnnctD** <br/> |
   

