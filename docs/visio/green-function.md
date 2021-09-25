---
title: GREEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
ms.localizationpriority: medium
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Gibt die grüne Komponente einer Farbe zurück.
ms.openlocfilehash: fa80526aebc21fc227f54f6c6bb25d397a46b5a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554712"
---
# <a name="green-function"></a>GREEN Function

Gibt die grüne Komponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

GREEN(** *Ausdruck* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Index einer Farbe in der Farbtabelle des Dokuments, ein Ausdruck, der in eine benutzerdefinierte Farbe aufgelöst wird (z. B. RGB oder HSL) oder ein Verweis auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255, oder ein Zellbezug, der als Index aufgelöst wird. Wenn  *der Ausdruck*  ungültig ist, wird 0 (schwarz) zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

GREEN(Sheet.4! FillForegnd)
  
Gibt den Wert der Grünkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

GREEN(11)
  
Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Dunkelgelb die Farbe mit Index 11 darstellt.
  
## <a name="example-3"></a>Beispiel 3

GREEN(RGB(10, 20, 30))
  
Gibt 20 zurück.
  

