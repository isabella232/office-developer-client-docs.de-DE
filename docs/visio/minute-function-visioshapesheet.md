---
title: MINUTE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Gibt eine ganze Zahl von 0 bis 59, die die Minutenkomponente in Datetime oder Expression darstellt.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797528"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE Function (VisioShapeSheet)

Gibt eine ganze Zahl von 0 bis 59, die die Minutenkomponente in *Datetime* oder *Expression* darstellt. 
  
## <a name="syntax"></a>Syntax

MINUTE (" *Datetime* " |  *Ausdruck*  [, *Lcid* ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Nummer** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Integer
  
## <a name="remarks"></a>Hinweise

Die Datumskomponente in _Datetime_ und _Expression_ wird verworfen. 
  
Keine Rundung erfolgt. Wenn _Datetime_ nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Der zurückgegebene  Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist.
  
Die MINUTE-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil für den Bruchteil eines Tages seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

MINUTE("7/7/1999 13:45:24")
  
Gibt 45 zurück.
  
## <a name="example-2"></a>Beispiel 2

MINUTE(ZEITWERT("25. Jan. 1999 12:07:45")+6 vm.)
  
Gibt 13 zurück.
  
## <a name="example-3"></a>Beispiel 3

MINUTE(0.575)
  
Gibt 48 zurück.
  

