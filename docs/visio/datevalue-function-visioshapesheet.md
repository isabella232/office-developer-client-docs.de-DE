---
title: DATEVALUE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
ms.localizationpriority: medium
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Gibt den Datumswert zurück, der durch datetime oder Expression dargestellt wird.
ms.openlocfilehash: 571d0f319ccbbefa412e2b31bbc01d49ee9ec46c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582813"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE-Funktion (VisioShapeSheet)

Gibt den Datumswert zurück, der durch _Datetime_ oder Ausdruck dargestellt wird. 
  
## <a name="syntax"></a>Syntax

DATEVALUE(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Datetime
  
## <a name="remarks"></a>HinwBemerkungeneise

Jede Zeitkomponente in *datetime* oder Expression wird verworfen.  
  
Wenn  *datetime*  fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt DATEVALUE eine #VALUE! zurück. 
  
Der Wert wird in dem Kurzdatumsformat angezeigt, der aktuell in den Ländereinstellungen des Systems festgelegt ist. 
  
Die DATEVALUE-Funktion akzeptiert auch einen einzelnen Zahlenwert für  *einen Ausdruck,*  wobei der ganzzahlige Teil des Ergebnisses die Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

DATEVALUE(JETZT( ))+5 ed.
  
Gibt das Datum fünf Tage nach dem aktuellen Datum zurück.
  
## <a name="example-2"></a>Beispiel 2

DATEVALUE("19.07.1995 12:30")
  
Gibt das Datum zurück.
  
## <a name="example-3"></a>Beispiel 3

DATEVALUE("33. Mai 1997")
  
Gibt einen Fehler vom Typ #WERT! zurück.
  
## <a name="example-4"></a>Beispiel 4

DATEVALUE(35580.6337)
  
Gibt 30.5. 1997 zurück.
  

