---
title: DAYOFYEAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Gibt eine ganze Zahl von 1 bis 366 zurück, die den sequenziellen Tag des Jahres in DateTime oder Expression darstellt. Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439451"
---
# <a name="dayofyear-function"></a>TAGDESJAHRES-Funktion

Gibt eine ganze Zahl von 1 bis 366 zurück, die den sequenziellen Tag des Jahres in _DateTime_ oder _Expression_darstellt. Die DAYOFYEAR-Funktion verwendet den gregorianischen Kalender.
  
## <a name="syntax"></a>Syntax

DAYOFYEAR ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Alle Zeitkomponenten in _DateTime_ oder _Expression_ werden verworfen. 
  
Das Ergebnis entspricht dem 1. Januar bis zum 31. Dezember. Es findet kein Auf- oder Abrunden statt. Wenn _DateTime_ fehlt oder nicht als gültige Datums-oder Uhrzeitangabe interpretiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Die DAYOFYEAR-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

DAYOFYEAR("30. Mai 1997 13:45:24")
  
Gibt 150 zurück
  
## <a name="example-2"></a>Beispiel 2

DAYOFYEAR(DATUMSWERT("30. Mai 1997")+7 t.)
  
Gibt 157 zurück.
  
## <a name="example-3"></a>Beispiel 3

DAYOFYEAR (35580.6337)
  
Gibt 150 zurück.
  

