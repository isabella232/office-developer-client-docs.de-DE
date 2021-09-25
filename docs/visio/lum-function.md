---
title: LUM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
ms.localizationpriority: medium
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Gibt den Wert der Leuchtdichtekomponente einer Farbe zurück.
ms.openlocfilehash: 752af49222ed7919e6c7b9cce4a51821bbe9f4b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582525"
---
# <a name="lum-function"></a>LUM Function

Gibt den Wert der Leuchtdichtekomponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

LUM(** *Ausdruck* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex aus der Farbpalette des Dokuments oder ein Bezug auf eine Zelle, die einen Farbindex enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 240. Bei einer ungültigen Eingabe wird 0 zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

LUM(Sheet.4! FillForegnd)
  
Gibt die Farbkomponente Helligkeit der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

LUM(6)
  
Gibt 120 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Magenta die Farbe mit Index 6 ist.
  
## <a name="example-3"></a>Beispiel 3

LUM(HSL(10, 20, 30))
  
Gibt 30 zurück.
  

