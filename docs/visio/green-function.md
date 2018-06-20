---
title: GREEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Gibt die Grünkomponente einer Farbe zurück.
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797141"
---
# <a name="green-function"></a>GREEN-Funktion

Gibt die Grünkomponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

Grün (** *Ausdruck* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Index einer Farbe in das Dokument Farbe Tabelle ein Ausdruck, der in einer benutzerdefinierten Farbe (wie RGB oder HSL) oder ein Bezug auf eine Zelle, die eine Farbe Index oder Farbe Ergebnis enthält aufgelöst wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Integer
  
## <a name="remarks"></a>Hinweise

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255 oder Bezug auf eine Zelle, die als Index aufgelöst wird. Wenn *Ausdruck* ungültig ist, wird 0 (Schwarz) zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

Grün (Sheet4! FillForegnd)
  
Gibt den Wert der Grünkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

GREEN(11)
  
Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Dunkelgelb die Farbe mit Index 11 darstellt.
  
## <a name="example-3"></a>Beispiel 3

GREEN(RGB(10, 20, 30))
  
Gibt 20 zurück.
  

