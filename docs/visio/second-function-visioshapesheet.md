---
title: SECOND-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
ms.localizationpriority: medium
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Sekundenkomponente von DateTime oder Ausdruck darstellt.
ms.openlocfilehash: f9f8a3f823ed4b0989abd6f338aaf44a0f56a059
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553926"
---
# <a name="second-function-visioshapesheet"></a>SECOND-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl zwischen 0 und 59 zurück, die die Sekundenkomponente von _datetime_ oder Ausdruck darstellt. 
  
## <a name="syntax"></a>Syntax

SECOND(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numeric** <br/> |Der Gebietsschemabezeichner, der beim Auswerten einer nicht lokalen  _DateTime_ verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in _datetime_ oder Expression wird verworfen.  
  
Es findet kein Auf- oder Abrunden statt. Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion einen Fehler zurück. 
  
The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight. 
  
## <a name="example-1"></a>Beispiel 1

SECOND("30.05.1997 13:45:32")
  
Gibt 32 zurück.
  
## <a name="example-2"></a>Beispiel 2

SECOND(ZEITWERT("30. Mai 1996 12:07:45")+7 as.)
  
Gibt 52 zurück.
  
## <a name="example-3"></a>Beispiel 3

SECOND(0,6337)
  
Gibt 32 zurück.
  

