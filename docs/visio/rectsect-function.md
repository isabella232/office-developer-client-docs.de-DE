---
title: RECTSECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Berechnet den Sektor eines Rechtecks, das x und y zugeordnet ist, und gibt eine ganze Zahl von 0 bis 4 zurück, die den Sektor angibt.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160272"
---
# <a name="rectsect-function"></a>RECTSECT Function

Berechnet den Sektor eines Rechtecks, das  *x*  und  *y*  zugeordnet ist, und gibt eine ganze Zahl von 0 bis 4 zurück, die den Sektor angibt. 
  
## <a name="syntax"></a>Syntax

RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Breite des Rechtecks.  <br/> |
| _height_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Höhe des Rechtecks.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _option_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Betrachten Sie ein Rechteck, das eine  *Breite*  und eine  *Höhe*  und einen Punkt (*x,y*) vom Mittelpunkt des Rechtecks hat. Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks, um es in vier Sektoren und einen Mittelpunkt zu teilen. Die Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, links und unten dar. 
  
![Die Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, links und unten dar.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Beispiel

RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0) 
  
Gibt 4 zurück. 
  

