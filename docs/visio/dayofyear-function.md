---
title: DAYOFYEAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
ms.localizationpriority: medium
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Gibt eine ganze Zahl zwischen 1 und 366 zurück, die den sequenziellen Tag des Jahres in datetime oder Ausdruck darstellt. Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: 8a73d4c8c7df501e1969d8aa9279f720407d2e7b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559969"
---
# <a name="dayofyear-function"></a>TAGDESJAHRES-Funktion

Gibt eine ganze Zahl, 1 bis 366, die den sequenziellen Tag des Jahres in  _Datum und Uhrzeit_ oder  _Ausdruck_ darstellt. Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.
  
## <a name="syntax"></a>Syntax

DAYOFYEAR(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
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
  
Das Ergebnis entspricht dem 1. Januar bis zum 31. Dezember. Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Die DAYOFYEAR-Funktion akzeptiert auch einen einzelnen Zahlenwert für  _einen Ausdruck,_ wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

DAYOFYEAR("30. Mai 1997 13:45:24")
  
Gibt 150 zurück
  
## <a name="example-2"></a>Beispiel 2

DAYOFYEAR(DATUMSWERT("30. Mai 1997")+7 t.)
  
Gibt 157 zurück.
  
## <a name="example-3"></a>Beispiel 3

DAYOFYEAR(35580.6337)
  
Gibt 150 zurück.
  

