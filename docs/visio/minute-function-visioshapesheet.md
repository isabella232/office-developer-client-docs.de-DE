---
title: MINUTE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
ms.localizationpriority: medium
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Minutenkomponente von datetime oder Ausdruck darstellt.
ms.openlocfilehash: b57eae5388969461056e6d2fe00b5e1035e8a24b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594517"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Minutenkomponente von *datetime* oder Ausdruck darstellt.  
  
## <a name="syntax"></a>Syntax

MINUTE(" *datetime*  "|  *Ausdruck*  [,  *lcid*  ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in  _datetime_ und  _Expression_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.
  
Die MINUTE-Funktion akzeptiert auch einen einzelnen Zahlenwert für  _einen Ausdruck,_ wobei der Dezimalteil den Bruchteil eines Tages seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

MINUTE("7.07.1999 13:45:24")
  
Gibt 45 zurück.
  
## <a name="example-2"></a>Beispiel 2

MINUTE(ZEITWERT("25. Jan. 1999 12:07:45")+6 vm.)
  
Gibt 13 zurück.
  
## <a name="example-3"></a>Beispiel 3

MINUTE(0,575)
  
Gibt 48 zurück.
  

