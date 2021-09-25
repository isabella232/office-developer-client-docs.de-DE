---
title: DAY-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
ms.localizationpriority: medium
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Gibt eine ganze Zahl zwischen 1 und 31 zurück, die den Tag in DateTime oder Ausdruck darstellt. Die DAY-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: d8e098f6e3f8646d7cda9fa4070844139b511adf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586565"
---
# <a name="day-function-visioshapesheet"></a>DAY-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl, 1 bis 31, die den Tag in  _Datum und Uhrzeit_ oder  _Ausdruck_ darstellt. Die DAY-Funktion verwendet den gregorianischen Kalender.
  
## <a name="syntax"></a>Syntax

DAY(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Jede Zeitkomponente in _datetime_ oder Expression wird verworfen.  
  
Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899. 
  
## <a name="example-1"></a>Beispiel 1

DAY("30. Mai 1997 15:45:24")
  
Gibt 30 zurück.
  
## <a name="example-2"></a>Beispiel 2

DAY(DATUMSWERT("30. Mai 1997")+7 t.)
  
Gibt 6 zurück.
  
## <a name="example-3"></a>Beispiel 3

DAY(35580,6337)
  
Gibt 30 zurück.
  

