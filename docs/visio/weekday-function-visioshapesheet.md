---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Gibt eine ganze Zahl von 1 bis 7, die den Wochentag in Datetime oder Expression darstellt.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798412"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY Function (VisioShapeSheet)

Gibt eine ganze Zahl von 1 bis 7, die den Wochentag in _Datetime_ oder _Expression_darstellt.
  
## <a name="syntax"></a>Syntax

Wochentag ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
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
  
Das Ergebnis entspricht Montag (1) bis Sonntag (7). Keine Rundung erfolgt. Wenn _Datetime_ nicht vorhanden ist oder nicht als gültige Datum oder Uhrzeit interpretiert werden kann, gibt die Funktion einer #VALUE! Fehler. 
  
Die WEEKDAY-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht. 
  
## <a name="example-1"></a>Beispiel 1

WEEKDAY("30. Mai 1999")
  
Gibt 7 zurück.
  
## <a name="example-2"></a>Beispiel 2

WEEKDAY(DATUMSWERT("30. Mai 1999")+2 vt.)
  
Gibt 2 zurück.
  
## <a name="example-3"></a>Beispiel 3

WEEKDAY(35880.6337)
  
Gibt 4 zurück.
  

