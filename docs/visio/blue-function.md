---
title: BLUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Gibt die blaue Komponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Wertebereich von 0 bis 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297354"
---
# <a name="blue-function"></a>BLUE Function

Gibt die blaue Komponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Wertebereich von 0 bis 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
  
## <a name="syntax"></a>Syntax

BLAU (* * *Ausdruck* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="example-1"></a>Beispiel 1

BLAU (Blatt. 4! Zelle FillForegnd
  
Gibt die Blaukomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

BLAU (13)
  
Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Cyan die Farbe mit Index 13 ist.
  
## <a name="example-3"></a>Beispiel 3

BLUE(RGB(10, 20, 30))
  
Gibt 30 zurück.
  

