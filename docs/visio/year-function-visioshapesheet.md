---
title: YEAR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Gibt eine ganze Zahl, die das gregorianische Jahr in Datetime oder Expression, formatiert entsprechend der im kurzen Datumsformat festlegen, indem die Standardeinstellungen des Systems aktuellen Region und Sprache darstellt.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798469"
---
# <a name="year-function-visioshapesheet"></a>YEAR Function (VisioShapeSheet)

Gibt eine ganze Zahl, die das gregorianische Jahr in _Datetime_ oder _Ausdruck_, der im kurzen Datumsformat festlegen, indem die Standardeinstellungen des Systems aktuellen Region und Sprache darstellt.
  
## <a name="syntax"></a>Syntax

Jahr ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numerische** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Integer
  
## <a name="remarks"></a>Hinweise

Die Zeitkomponente in _Datetime_ oder _Expression_ wird verworfen. 
  
Keine Rundung erfolgt. Wenn _Datetime_ nicht vorhanden ist oder nicht als gültige Datum oder Uhrzeit interpretiert werden kann, gibt Jahr einen Fehler zurück. 
  
Die YEAR-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht. 
  
## <a name="example-1"></a>Beispiel 1

YEAR("27/10/2007 13:45:24")
  
Gibt 2007 zurück.
  
## <a name="example-2"></a>Beispiel 2

YEAR(DATUMSWERT("25. Dez. 2006") + 7 ed.)
  
Gibt 2007 zurück.
  
## <a name="example-3"></a>Beispiel 3

YEAR(35580.6337)
  
Gibt 1997 zurück.
  

