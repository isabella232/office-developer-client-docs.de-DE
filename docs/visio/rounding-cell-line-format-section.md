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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427010"
---
# <a name="rounding-cell-line-format-section"></a>Zelle "Rounding" (Abschnitt "Line Format")

Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
  
## <a name="remarks"></a>Hinweise

Sie können diesen Wert  auch im Dialogfeld  Linie festlegen (klicken Sie auf der Registerkarte Start in der **Gruppe Shape** auf **Linie,** zeigen Sie auf **Gewichtung,** und klicken Sie dann auf **Weitere Linien**).
  
Um einen Verweis auf die Rounding-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Rounding  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Rounding-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineRounding** <br/> |
   

