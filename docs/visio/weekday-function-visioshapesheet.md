---
title: WEEKDAY-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Gibt eine ganze Zahl von 1 bis 7 zurück, die den Wochentag in Datetime oder Ausdruck darstellt.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404806"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl von 1 bis 7 zurück, die den Wochentag in _Datetime oder_ Ausdruck _darstellt._
  
## <a name="syntax"></a>Syntax

WEEKDAY(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
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
  
Das Ergebnis entspricht Montag (1) bis Sonntag (7). Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt die Funktion eine #VALUE! zurück. 
  
Die WEEKDAY-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

WEEKDAY("30. Mai 1999")
  
Gibt 7 zurück.
  
## <a name="example-2"></a>Beispiel 2

WEEKDAY(DATUMSWERT("30. Mai 1999")+2 vt.)
  
Gibt 2 zurück.
  
## <a name="example-3"></a>Beispiel 3

WEEKDAY(35880.6337)
  
Gibt 4 zurück.
  

