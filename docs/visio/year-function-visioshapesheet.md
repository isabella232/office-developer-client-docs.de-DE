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
description: Gibt eine ganze Zahl zurück, die das gregorianische Jahr in Datetime oder Ausdruck darstellt, formatiert gemäß der kurzen Datumsformatvorlage, die durch die aktuellen Einstellungen für Region und Sprache des Systems festgelegt wird.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420710"
---
# <a name="year-function-visioshapesheet"></a>YEAR-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zurück, die das gregorianische Jahr in  _Datetime_ oder Ausdruck  _darstellt,_ formatiert gemäß der kurzen Datumsformatvorlage, die durch die aktuellen Einstellungen für Region und Sprache des Systems festgelegt wird.
  
## <a name="syntax"></a>Syntax

YEAR(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional.  <br/> |**Numeric** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente in  _datetime_ oder  _ausdruck_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt YEAR einen Fehler zurück. 
  
Die YEAR-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

YEAR("27.10.2007 13:45:24")
  
Gibt 2007 zurück.
  
## <a name="example-2"></a>Beispiel 2

YEAR(DATUMSWERT("25. Dez. 2006") + 7 ed.)
  
Gibt 2007 zurück.
  
## <a name="example-3"></a>Beispiel 3

YEAR(35580.6337)
  
Gibt 1997 zurück.
  

