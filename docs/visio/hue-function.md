---
title: HUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
ms.localizationpriority: medium
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Gibt den Wert der Farbtonkomponente einer Farbe zurück.
ms.openlocfilehash: e259355f13f1b40739d63b8d76e32ef7c2d22c03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618798"
---
# <a name="hue-function"></a>HUE Function

Gibt den Wert der Farbtonkomponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

HUE(** *Ausdruck* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Ausdruck, der eine Farbe ergibt.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Wert ist eine Zahl im Bereich von 0 bis einschließlich 239. Die Eingabe ist ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der in eine angepasste Farbe (wie RGB oder HSL) aufgelöst wird oder ein Verweis auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält. Die Funktion gibt bei einer ungültigen Eingabe 0 zurück. 
  
## <a name="example-1"></a>Beispiel 1

HUE(Sheet.4! FillForegnd)
  
Gibt den Wert der Farbtonkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

HUE(7)
  
Gibt 120 zurück, wenn das Dokument die Farbpalette von Microsoft Visio verwendet, wobei Zyan die Farbe mit Index 7 darstellt.
  
## <a name="example-3"></a>Beispiel 3

HUE(HSL(10, 20, 30))
  
Gibt 10 zurück.
  

