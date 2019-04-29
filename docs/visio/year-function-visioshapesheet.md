---
title: YEAR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Gibt eine ganze Zahl zurück, die das gregorianische Jahr in DateTime oder Expression darstellt, formatiert entsprechend der kurzen Datumsformat Vorlage, die durch die aktuelle Regions-und Spracheinstellungen des Systems festgelegt ist.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420710"
---
# <a name="year-function-visioshapesheet"></a>YEAR-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zurück, die das gregorianische Jahr in _DateTime_ oder _Expression_darstellt, formatiert entsprechend der kurzen Datumsformat Vorlage, die durch die aktuelle Regions-und Spracheinstellungen des Systems festgelegt ist.
  
## <a name="syntax"></a>Syntax

Jahr ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numeric** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente in _DateTime_ oder _Expression_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn _DateTime_ fehlt oder nicht als gültige Datums-oder Uhrzeitangabe interpretiert werden kann, gibt Year einen Fehler zurück. 
  
Die YEAR-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

JAHR ("10/27/2007 13:45:24")
  
Gibt 2007 zurück.
  
## <a name="example-2"></a>Beispiel 2

YEAR(DATUMSWERT("25. Dez. 2006") + 7 ed.)
  
Gibt 2007 zurück.
  
## <a name="example-3"></a>Beispiel 3

JAHR (35580.6337)
  
Gibt 1997 zurück.
  

