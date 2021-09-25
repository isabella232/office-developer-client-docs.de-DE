---
title: RGB-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
ms.localizationpriority: medium
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe anhand ihrer roten, grünen und blauen Komponenten an, wobei jede eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.
ms.openlocfilehash: 9705d0e4c881a2d98e176a9982bbc7a95140755c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573523"
---
# <a name="rgb-function-visioshapesheet"></a>RGB-Funktion (VisioShapeSheet)

Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe anhand ihrer roten, grünen und blauen Komponenten an, wobei jede eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird. 
  
## <a name="syntax"></a>Syntax

RGB(** *red* **, ** *green* **, ** *blue* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Rot_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Rotkomponente.  <br/> |
| _Grün_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Grünkomponente.  <br/> |
| _Blau_ <br/> |Erforderlich  <br/> |**Nmber** <br/> |Die Blaukomponente.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie in diese eingefügt.
  
Die folgende Tabelle listet einige Standardfarben mit ihren Rot-, Grün- und Blauwerten auf.
  
|**Color**|**Rotwert**|**Grünwert**|**Blauwert**|
|:-----|:-----|:-----|:-----|
|Black  <br/> |0  <br/> |0  <br/> |0  <br/> |
|Blau  <br/> |0  <br/> |0  <br/> |255  <br/> |
|Grün  <br/> |0  <br/> |255  <br/> |0  <br/> |
|Cyan  <br/> |0  <br/> |255  <br/> |255  <br/> |
|Rot  <br/> |255  <br/> |0  <br/> |0  <br/> |
|Magenta  <br/> |255  <br/> |0  <br/> |255  <br/> |
|Gelb  <br/> |255  <br/> |255  <br/> |0  <br/> |
|Weiß  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>Beispiel 1

RGB(0,0,255)
  
Gibt den Index für die Farbe Blau zurück.
  
## <a name="example-2"></a>Beispiel 2

RGB(RED(Sheet.1! FillForegnd),120,0)
  
Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.
  

