---
title: Zelle "Value" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Enthält die Funktion für ein Feld.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430945"
---
# <a name="value-cell-text-fields-section"></a>Zelle "Value" (Abschnitt "Text Fields")

Enthält die Funktion für ein Feld.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle im Dialogfeld **Feld** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld**).
  
Wenn Sie einen Verweis auf die Zelle Wert aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Fields. Value [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Value nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
|Zeilenindex:  <br/> |**visRowField** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFieldCell** <br/> |
   

