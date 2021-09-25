---
title: MONTH-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
ms.localizationpriority: medium
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Gibt eine ganze Zahl zwischen 1 und 12 zurück, die einen Monat darstellt.
ms.openlocfilehash: 44e033ab2719a45b6ddfba48ac53b4a4e9606d3b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573887"
---
# <a name="month-function-visioshapesheet"></a>MONTH-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zwischen 1 und 12 zurück, die einen Monat darstellt.
  
## <a name="syntax"></a>Syntax

MONTH(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente von _datetime_ oder Expression wird verworfen.  
  
Es findet kein Auf- oder Abrunden statt. Wenn die Eingabezeichenfolge nicht angegeben wurde oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die MONTH-Funktion einen Fehler zurück.
  
Der Wert wird in dem Kurzdatumsformat zurückgegeben, der aktuell in den Ländereinstellungen des Systems festgelegt ist.
  
The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899. 
  
## <a name="example-1"></a>Beispiel 1

MONTH("30. Mai 1999 13:45:24")
  
Gibt 5 zurück.
  
## <a name="example-2"></a>Beispiel 2

MONTH(DATUMSWERT("30. Mai 1999")+7 t.)
  
Gibt 6 zurück.
  
## <a name="example-3"></a>Beispiel 3

MONTH(35580.6337)
  
Gibt 5 zurück.
  

