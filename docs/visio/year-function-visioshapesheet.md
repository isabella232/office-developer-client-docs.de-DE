---
title: YEAR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
ms.localizationpriority: medium
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Gibt eine ganze Zahl zurück, die das gregorianische Jahr in datetime oder Ausdruck darstellt, formatiert gemäß der kurzen Datumsart, die von den aktuellen Einstellungen für Region und Sprache des Systems festgelegt wurde.
ms.openlocfilehash: f201e6cf4efe308e0c79e0795ef97d33e1bd5868
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612427"
---
# <a name="year-function-visioshapesheet"></a>YEAR-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zurück, die das gregorianische Jahr in _datetime_ oder Ausdruck darstellt, formatiert gemäß dem kurzen Datumsformat, das durch die aktuellen Einstellungen für Region und Sprache des Systems festgelegt wurde. 
  
## <a name="syntax"></a>Syntax

YEAR(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numeric** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente in _datetime_ oder Expression wird verworfen.  
  
Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt YEAR einen Fehler zurück. 
  
The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899. 
  
## <a name="example-1"></a>Beispiel 1

YEAR("27.10.2007 13:45:24")
  
Gibt 2007 zurück.
  
## <a name="example-2"></a>Beispiel 2

YEAR(DATUMSWERT("25. Dez. 2006") + 7 ed.)
  
Gibt 2007 zurück.
  
## <a name="example-3"></a>Beispiel 3

YEAR(35580,6337)
  
Gibt 1997 zurück.
  

