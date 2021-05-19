---
title: LUM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Gibt den Wert der Leuchtkraftkomponente einer Farbe zurück.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419338"
---
# <a name="lum-function"></a>LUM Function

Gibt den Wert der Leuchtkraftkomponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

LUM(** *Expression* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex aus der Farbpalette des Dokuments oder ein Bezug auf eine Zelle, die einen Farbindex enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Nummer
  
## <a name="remarks"></a>Hinweise

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
  

