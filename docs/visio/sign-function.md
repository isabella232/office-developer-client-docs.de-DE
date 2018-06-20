---
title: SIGN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Gibt einen Wert, der die Zeichen einer Zahl darstellt.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798124"
---
# <a name="sign-function"></a>SIGN-Funktion

Gibt einen Wert, der die Zeichen einer Zahl darstellt. 
  
## <a name="syntax"></a>Syntax

Vorzeichen (** *Anzahl* **, ** *mit zufälligen Daten* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numerische** <br/> | Die Zahl, für die das Vorzeichen bestimmt werden soll.  <br/> |
| _mit zufälligen Daten_ <br/> |Optional  <br/> |**Numerische** <br/> |Gibt an, wie klein der Wert einer Zahl sein muss, damit diese als gleich 0 (null) betrachtet wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Numeric
  
## <a name="remarks"></a>Bemerkungen

Die SIGN-Funktion gibt 1 zurück, wenn _Number_ positiv ist, 0, wenn die _Zahl_ 0 (null) oder-1 ist, ist _Zahl_ negativ. 
  
Ein Wert _mit zufälligen Daten_ Specifyin hilft bei Fließkommazahlen vermieden, wenn eine Berechnung fast gleich NULL ist. Wenn Sie einen Wert _mit zufälligen Daten_ nicht angeben, verwendet Visio 1E-9 (0.000000001). Sie möchten einen anderen Wert angeben, beim Skalieren von Zeichnungen, oder wenn Sie einen genauen Vergleich möchten. 
  
## <a name="example-1"></a>Beispiel 1

SIGN-5)
  
Gibt -1 zurück.
  
## <a name="example-2"></a>Beispiel 2

SIGN(0)
  
Gibt 0 zurück.
  
## <a name="example-3"></a>Beispiel 3

SIGN(0.00000000001)
  
Gibt 0 zurück.
  
## <a name="example-4"></a>Beispiel 4

SIGN(0.00000000001,0)
  
Gibt 1 zurück.
  

