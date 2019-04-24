---
title: Zelle "Rounding" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358583"
---
# <a name="rounding-cell-line-format-section"></a>Zelle "Rounding" (Abschnitt "Line Format")

Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Gewicht**, und klicken Sie dann auf **Weitere Linien**).
  
Wenn Sie einen Verweis auf die Zelle Rundung aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Rounding  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Rundung aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineRounding** <br/> |
   

