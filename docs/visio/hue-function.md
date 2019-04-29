---
title: HUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Gibt den Wert der Farbtonkomponente einer Farbe zurück.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439492"
---
# <a name="hue-function"></a>HUE Function

Gibt den Wert der Farbtonkomponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

HUE (* * *Expression* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Ausdruck, der eine Farbe ergibt.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Wert ist eine Zahl im Bereich von 0 bis einschließlich 239. Die Eingabe ist ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der in eine angepasste Farbe (wie RGB oder HSL) aufgelöst wird oder ein Verweis auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält. Die Funktion gibt bei einer ungültigen Eingabe 0 zurück. 
  
## <a name="example-1"></a>Beispiel 1

Farbton (Blatt. 4! Zelle FillForegnd
  
Gibt den Wert der Farbtonkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

FARBTON (7)
  
Gibt 120 zurück, wenn das Dokument die Farbpalette von Microsoft Visio verwendet, wobei Zyan die Farbe mit Index 7 darstellt.
  
## <a name="example-3"></a>Beispiel 3

HUE(HSL(10, 20, 30))
  
Gibt 10 zurück.
  

