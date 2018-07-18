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
description: Berechnet den Sektor eines Rechtecks zugeordnete x und y und gibt eine Ganzzahl zwischen 0 und 4, der angibt, des Sektors.
ms.openlocfilehash: 1f35704cdb827c9c751f11593436c110755d7777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797772"
---
# <a name="rectsect-function"></a>RECTSECT Function

Berechnet den Sektor eines Rechtecks *X* und *y* zugeordnet und gibt eine Ganzzahl zwischen 0 und 4, der angibt, des Sektors. 
  
## <a name="syntax"></a>Syntax

RECTSECT (** *Breite* **, ** *Höhe* **, ** *X* **, ** *y* **, ** *Option* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Breite des Rechtecks.  <br/> |
| _height_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Höhe des Rechtecks.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _Option_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Berücksichtigen Sie ein Rechteck mit einer *Breite* und eine *Höhe* und einem Punkt (*X, y*) vom Mittelpunkt des Rechtecks. Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks in vier Bereiche und einen Mittelpunkt unterteilen. Sektor 0 bis 4 darstellen der Mittelpunkt, rechts, oben, links und jeweils unten. 
  
![](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Beispiel

RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0) 
  
Gibt 4 zurück. 
  

