---
title: RED-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Gibt die rote Komponente einer Farbe zurück.
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415523"
---
# <a name="red-function"></a>RED Function

Gibt die rote Komponente einer Farbe zurück. 
  
## <a name="syntax"></a>Syntax

RED(** *Expression* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Nummer
  
## <a name="remarks"></a>Hinweise

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255, oder ein Zellbezug, der als Index aufgelöst wird. Wenn  _Ausdruck_ ungültig ist, gibt diese Funktion 0 (Schwarz) zurück. 
  
## <a name="example-1"></a>Beispiel 1

RED(22)
  
Gibt 51 zurück, wenn das Dokument die Farbpalette von Microsoft Office Visio verwendet, wobei Dunkelgrau die Farbe mit Index 22 ist.
  
## <a name="example-2"></a>Beispiel 2

RED(Char.Color)
  
Gibt den Wert der Rotkomponente der Farbe der aktuellen Schriftart zurück.
  
## <a name="example-3"></a>Beispiel 3

RED(RGB(10, 20, 30))
  
Gibt 10 zurück.
  

