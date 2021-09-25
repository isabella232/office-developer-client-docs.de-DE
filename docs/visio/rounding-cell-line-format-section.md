---
title: Zelle "Rounding" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
ms.localizationpriority: medium
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
ms.openlocfilehash: 8012422c654b3090ee2c007ce8911e53eef28cfd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607794"
---
# <a name="rounding-cell-line-format-section"></a>Zelle "Rounding" (Abschnitt "Line Format")

Zeigt den Radius des Rundungsbogens an, der sich dort befindet, wo zwei fortlaufende Segmente eines Pfads aufeinander treffen. Die Abrundungsfunktion kann beispielsweise verwendet werden, um die Ecken eines Rechtecks abzurunden. Um die Abrundung festzulegen, geben Sie einen Wert mit einer Maßeinheit ein (d. h. ein Paar aus einer Zahl und einer Einheit).
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch im Dialogfeld **"Linie"** festlegen (klicken Sie auf der Registerkarte **"Start"** in der Gruppe **"Shape"** auf **"Linie",** zeigen Sie auf **"Gewichtung",** und klicken Sie dann auf **"Weitere Linien").**
  
Um einen Verweis auf die Rundungszelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Rundung  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Rundungszelle anhand des Indexes aus einem Programm abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineRounding** <br/> |
   

