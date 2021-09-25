---
title: BLUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
ms.localizationpriority: medium
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Gibt die Blaukomponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Bereich von 0 bis einschließlich 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
ms.openlocfilehash: eac92b4b83f63d99f65ba7f70cc2dfdcf2634a76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616005"
---
# <a name="blue-function"></a>BLUE Function

Gibt die Blaukomponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Bereich von 0 bis einschließlich 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
  
## <a name="syntax"></a>Syntax

BLUE(** *Ausdruck* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="example-1"></a>Beispiel 1

BLUE(Sheet.4! FillForegnd)
  
Gibt die Blaukomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

BLUE(13)
  
Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Cyan die Farbe mit Index 13 ist.
  
## <a name="example-3"></a>Beispiel 3

BLUE(RGB(10, 20, 30))
  
Gibt 30 zurück.
  

