---
title: SAT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
ms.localizationpriority: medium
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Gibt den Wert der Sättigungskomponente einer Farbe zurück.
ms.openlocfilehash: 619a221e1b22442605364ee8cdf1b29f3fc002c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627548"
---
# <a name="sat-function"></a>SAT Function

Gibt den Wert der Sättigungskomponente einer Farbe zurück. 
  
## <a name="syntax"></a>Syntax

SAT(** *Ausdruck* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numeric
  
## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 240. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
  
## <a name="example-1"></a>Beispiel 1

SAT(Sheet.4! FillForegnd)
  
Gibt den Wert der Sättigung der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

SAT(8)
  
Gibt 240 zurück, wenn das Dokument die Farbpalette von Visio verwendet, wobei Dunkelrot die Farbe mit Index 8 ist.
  
## <a name="example-3"></a>Beispiel 3

SAT(HSL(10, 20, 30))
  
Gibt 20 zurück.
  

