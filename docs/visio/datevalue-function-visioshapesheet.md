---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Der Date-Wert dargestellt durch Datetime oder Expression zurückgegeben.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796806"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE Function (VisioShapeSheet)

Der Date-Wert dargestellt durch _Datetime_ oder _Expression_zurückgegeben.
  
## <a name="syntax"></a>Syntax

DATEVALUE ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Nummer** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Datetime
  
## <a name="remarks"></a>Bemerkungen

Alle Zeitkomponenten in *Datetime* oder *Expression* wird verworfen. 
  
Wenn *Datetime* nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt DATEVALUE ein #VALUE! Fehler. 
  
Der Wert wird in dem Kurzdatumsformat angezeigt, der aktuell in den Ländereinstellungen des Systems festgelegt ist. 
  
DATEVALUE-Funktion nimmt auch einen einzelnen Zahlenwert für *Expression* , wobei der Ganzzahlteil des Ergebnisses die Tagen seit dem 30. Dezember 1899 steht. 
  
## <a name="example-1"></a>Beispiel 1

DATEVALUE(JETZT( ))+5 ed.
  
Gibt das Datum fünf Tage nach dem aktuellen Datum zurück.
  
## <a name="example-2"></a>Beispiel 2

DATEVALUE("19/7/1995 12:30")
  
Gibt das Datum zurück.
  
## <a name="example-3"></a>Beispiel 3

DATEVALUE("33. Mai 1997")
  
Gibt einen Fehler vom Typ #WERT! zurück.
  
## <a name="example-4"></a>Beispiel 4

DATEVALUE(35580.6337)
  
Gibt 30.5. 1997 zurück.
  

