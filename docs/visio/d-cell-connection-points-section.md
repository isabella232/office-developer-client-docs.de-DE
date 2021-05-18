---
title: Zelle "D" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408173"
---
# <a name="d-cell-connection-points-section"></a>Zelle "D" (Abschnitt "Connection Points")

Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.
  
## <a name="remarks"></a>Hinweise

Klicken Sie zum Zugreifen auf die Zelle D mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp** ändern. 
  
Um einen Verweis auf die Zelle D anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections.D[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle D nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visCnnctD** <br/> |
   

