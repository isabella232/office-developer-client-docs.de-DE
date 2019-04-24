---
title: DATEVALUE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Gibt den durch DateTime oder Expression dargestellten Date-Wert zurück.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360312"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE-Funktion (VisioShapeSheet)

Gibt den durch _DateTime_ oder _Expression_dargestellten Date-Wert zurück.
  
## <a name="syntax"></a>Syntax

DATEvalue ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

DateTime
  
## <a name="remarks"></a>Bemerkungen

Alle Zeitkomponenten in *DateTime* oder *Expression* werden verworfen. 
  
Wenn *DateTime* fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt DateValue eine #VALUE zurück! zurück. 
  
Der Wert wird in dem Kurzdatumsformat angezeigt, der aktuell in den Ländereinstellungen des Systems festgelegt ist. 
  
Die DATEvalue-Funktion akzeptiert auch einen einzelnen Zahlenwert für *Expression* , wobei der ganzzahlige Teil des Ergebnisses die Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

DATEVALUE(JETZT( ))+5 ed.
  
Gibt das Datum fünf Tage nach dem aktuellen Datum zurück.
  
## <a name="example-2"></a>Beispiel 2

DATEVALUE ("7/19/1995 12:30")
  
Gibt das Datum zurück.
  
## <a name="example-3"></a>Beispiel 3

DATEVALUE("33. Mai 1997")
  
Gibt einen Fehler vom Typ #WERT! zurück.
  
## <a name="example-4"></a>Beispiel 4

DATEVALUE (35580.6337)
  
Gibt 30.5. 1997 zurück.
  

