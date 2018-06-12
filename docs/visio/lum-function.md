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
description: Gibt den Wert einer Farbkomponente Helligkeit zurück.
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797433"
---
# <a name="lum-function"></a>LUM Function

Gibt den Wert einer Farbkomponente Helligkeit zurück.
  
## <a name="syntax"></a>Syntax

LUM (** *Ausdruck* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Der Farbindex aus der Farbpalette des Dokuments oder ein Bezug auf eine Zelle, die einen Farbindex enthält.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 240. Bei einer ungültigen Eingabe wird 0 zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

LUM (Sheet4! FillForegnd)
  
Gibt die Farbkomponente Helligkeit der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

LUM(6)
  
Gibt 120 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Magenta die Farbe mit Index 6 ist.
  
## <a name="example-3"></a>Beispiel 3

LUM(HSL(10, 20, 30))
  
Gibt 30 zurück.
  

