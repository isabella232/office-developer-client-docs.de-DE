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
description: Gibt die Rotkomponente einer Farbe zurück.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797769"
---
# <a name="red-function"></a>RED Function

Gibt die Rotkomponente einer Farbe zurück. 
  
## <a name="syntax"></a>Syntax

Rot (** *Ausdruck* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Varies** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255 oder Bezug auf eine Zelle, die als Index aufgelöst wird. Wenn der _Ausdruck_ ungültig ist, gibt diese Funktion 0 (Schwarz). 
  
## <a name="example-1"></a>Beispiel 1

RED(22)
  
Gibt 51 zurück, wenn das Dokument die Farbpalette von Microsoft Office Visio verwendet, wobei Dunkelgrau die Farbe mit Index 22 ist.
  
## <a name="example-2"></a>Beispiel 2

Red(char.Color)
  
Gibt den Wert der Rotkomponente der Farbe der aktuellen Schriftart zurück.
  
## <a name="example-3"></a>Beispiel 3

RED(RGB(10, 20, 30))
  
Gibt 10 zurück.
  

