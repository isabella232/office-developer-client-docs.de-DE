---
title: MINUTE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Minutenkomponente von DateTime oder Expression darstellt.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283972"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Minutenkomponente von *DateTime* oder *Expression* darstellt. 
  
## <a name="syntax"></a>Syntax

MINUTE (" *DateTime* " |  *Ausdruck*  [, *LCID* ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in _DateTime_ und _Expression_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn _DateTime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.
  
Die MINUTE-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil den Bruchteil eines Tags seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

MINUTE ("7/7/1999 13:45:24")
  
Gibt 45 zurück.
  
## <a name="example-2"></a>Beispiel 2

MINUTE(ZEITWERT("25. Jan. 1999 12:07:45")+6 vm.)
  
Gibt 13 zurück.
  
## <a name="example-3"></a>Beispiel 3

MINUTE (0.575)
  
Gibt 48 zurück.
  

