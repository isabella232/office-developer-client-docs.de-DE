---
title: HOUR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
ms.localizationpriority: medium
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Gibt eine ganze Zahl zwischen 0 und 23 zurück, die die Stunde des Tages von Datum/Uhrzeit oder Ausdruck darstellt.
ms.openlocfilehash: 152dc3bc995ebfdcfe3f419f51d761f9ff054f7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628199"
---
# <a name="hour-function-visioshapesheet"></a>HOUR-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zwischen 0 und 23 zurück, die die Stunde des Tages von  _Datum/Uhrzeit_ oder  _Ausdruck_ darstellt.
  
## <a name="syntax"></a>Syntax

HOUR(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> | Eine Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> | Ein lokaler Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in  *datetime*  und  *Expression*  wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn  *datetime*  fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist. 
  
The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight. 
  
## <a name="example-1"></a>Beispiel 1

HOUR("15:45")
  
Gibt 15 zurück.
  
## <a name="example-2"></a>Beispiel 2

HOUR("30. Mai 1997 15:45:24")
  
Gibt 15 zurück.
  
## <a name="example-3"></a>Beispiel 3

HOUR(0,5)
  
Gibt 12 zurück.
  
## <a name="example-4"></a>Beispiel 4

HOUR("30.05.1997")
  
Gibt 0 zurück.
  

