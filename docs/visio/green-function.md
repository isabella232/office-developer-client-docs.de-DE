---
title: GREEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Gibt die grüne Komponente einer Farbe zurück.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360207"
---
# <a name="green-function"></a>GREEN Function

Gibt die grüne Komponente einer Farbe zurück.
  
## <a name="syntax"></a>Syntax

Grün (* * *Ausdruck* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Index einer Farbe in der Farbtabelle des Dokuments, ein Ausdruck, der in eine benutzerdefinierte Farbe (wie RGB oder GSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255, oder ein Zellbezug, der als Index aufgelöst wird. Wenn *Ausdruck* ungültig ist, gibt er 0 (schwarz) zurück. 
  
## <a name="example-1"></a>Beispiel 1

Grün (Blatt. 4! Zelle FillForegnd
  
Gibt den Wert der Grünkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.
  
## <a name="example-2"></a>Beispiel 2

GRÜN (11)
  
Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Dunkelgelb die Farbe mit Index 11 darstellt.
  
## <a name="example-3"></a>Beispiel 3

GREEN(RGB(10, 20, 30))
  
Gibt 20 zurück.
  

