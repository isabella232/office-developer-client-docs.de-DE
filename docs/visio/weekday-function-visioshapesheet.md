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
description: Gibt eine ganze Zahl von 1 bis 7 zurück, die den Wochentag in DateTime oder Expression darstellt.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285244"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl von 1 bis 7 zurück, die den Wochentag in _DateTime_ oder _Expression_darstellt.
  
## <a name="syntax"></a>Syntax

Wochentag ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numerisch** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente in _DateTime_ oder _Expression_ wird verworfen. 
  
Das Ergebnis entspricht Montag (1) bis Sonntag (7). Es findet kein Auf- oder Abrunden statt. Wenn _DateTime_ fehlt oder nicht als gültige Datums-oder Uhrzeitangabe interpretiert werden kann, gibt die funktion eine #VALUE! zurück. 
  
Die WEEKDAY-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

WEEKDAY("30. Mai 1999")
  
Gibt 7 zurück.
  
## <a name="example-2"></a>Beispiel 2

WEEKDAY(DATUMSWERT("30. Mai 1999")+2 vt.)
  
Gibt 2 zurück.
  
## <a name="example-3"></a>Beispiel 3

WOCHENTAG (35880.6337)
  
Gibt 4 zurück.
  

