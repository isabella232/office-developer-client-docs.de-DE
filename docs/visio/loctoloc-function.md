---
title: LOCTOLOC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Gibt einen transformierten Punkt in lokalen Koordinaten im Zielkoordinatensystem zurück.
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797427"
---
# <a name="loctoloc-function"></a>LOCTOLOC Function

Gibt einen transformierten Punkt in lokalen Koordinaten im Zielkoordinatensystem zurück.
  
## <a name="syntax"></a>Syntax

LOCTOLOC (** *Quellpunkt* **, ** *SrcRef* **, ** *Zielbezug* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Quellpunkt_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Punkt in den lokalen Koordinaten des Quellkoordinatensystems.  <br/> |
| _srcRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Quellobjekt.  <br/> |
| _Zielbezug_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Zielobjekt.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die LOCTOLOC-Funktion konvertiert einen Punkt aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes. Sie können diese Funktion verwenden, um beispielsweise ein Shape aus einem Punkt eines anderen Koordinatensystems zu konstruieren. Außerdem können Sie diese Funktion verwenden, um einen lokalen Punkt in Zeichenblattkoordinaten zu transformieren- und umgekehrt.
  
Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.
  
Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt sein.
  
## <a name="example"></a>Beispiel

Mit der folgenden Formel wird der lokale Drehpunkt des mit der Formel verknüpften Shapes in einen Punkt auf dem Zeichenblatt konvertiert.
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


