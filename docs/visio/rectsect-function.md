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
description: Berechnet den Bereich eines Rechtecks, das mit x und y verknüpft ist, und gibt eine ganze Zahl zwischen 0 und 4 zurück, die den Sektor angibt.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360030"
---
# <a name="rectsect-function"></a>RECTSECT Function

Berechnet den Bereich eines Rechtecks, das mit *x* und *y* verknüpft ist, und gibt eine ganze Zahl zwischen 0 und 4 zurück, die den Sektor angibt. 
  
## <a name="syntax"></a>Syntax

RECTSECT (* * *Breite* * *, * * *Höhe* * *, * * *x* * *, * * *y* * *, * * *Option* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Breite des Rechtecks.  <br/> |
| _height_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Höhe des Rechtecks.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _Option_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Betrachten Sie ein Rechteck mit einer *Breite* und einer *Höhe* und einen Punkt (*x, y*) vom Mittelpunkt des Rechtecks. Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks, um Sie in vier Sektoren und einen Mittelpunkt zu teilen. Die Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, Links und unten dar. 
  
![Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, Links und unten dar.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Beispiel

RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0) 
  
Gibt 4 zurück. 
  

