---
title: Zelle "Gamma" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Passt die Intensität einer Grafik für ein spezifisches Ausgabegerät (z. B. Monitor oder Scanner) an. Der Standardwert ist 1 (keine Korrektur).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315204"
---
# <a name="gamma-cell-image-properties-section"></a>Zelle "Gamma" (Abschnitt "Image Properties")

Passt die Intensität einer Grafik für ein spezifisches Ausgabegerät (z. B. Monitor oder Scanner) an. Der Standardwert ist 1 (keine Korrektur).
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Gamma aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Gamma  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Gamma aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowImage** <br/> |
| Zellenindex:  <br/> |**visImageGamma** <br/> |
   

