---
title: RED-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
ms.localizationpriority: medium
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Gibt die rote Komponente einer Farbe zurück.
ms.openlocfilehash: 37d54cb5cb35bb285b92ab31eea8482709410911
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623138"
---
# <a name="red-function"></a>RED Function

Gibt die rote Komponente einer Farbe zurück. 
  
## <a name="syntax"></a>Syntax

RED(** *Ausdruck* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255, oder ein Zellbezug, der als Index aufgelöst wird. Wenn  _der Ausdruck_ ungültig ist, gibt diese Funktion 0 (schwarz) zurück. 
  
## <a name="example-1"></a>Beispiel 1

RED(22)
  
Gibt 51 zurück, wenn das Dokument die Farbpalette von Microsoft Office Visio verwendet, wobei Dunkelgrau die Farbe mit Index 22 ist.
  
## <a name="example-2"></a>Beispiel 2

RED(Char.Color)
  
Gibt den Wert der Rotkomponente der Farbe der aktuellen Schriftart zurück.
  
## <a name="example-3"></a>Beispiel 3

RED(RGB(10, 20, 30))
  
Gibt 10 zurück.
  

