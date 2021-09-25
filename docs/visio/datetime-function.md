---
title: DATETIME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
ms.localizationpriority: medium
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Gibt den Datums- und Uhrzeitwert zurück, der durch DateTime oder Ausdruck dargestellt wird.
ms.openlocfilehash: 2d8d3bd17bf2c89b09b59a203bbe21a33bc6d8f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594636"
---
# <a name="datetime-function"></a>DATETIME-Funktion

Gibt den Datums- und Uhrzeitwert zurück, der durch  _DateTime_ oder  _Ausdruck_ dargestellt wird.
  
## <a name="syntax"></a>Syntax

DATETIME(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Datetime
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  *datetime*  fehlt oder nicht als gültiges Datum oder eine gültige Uhrzeit interpretiert werden kann, gibt DATETIME eine #VALUE! zurück. 
  
Der Wert wird in dem kurzen Zeit- und Datumsformat geliefert, das aktuell in den länderspezifischen Systemeinstellungen festgelegt ist. 
  
Die DATETIME-Funktion akzeptiert auch einen einzelnen Zahlenwert für  *einen Ausdruck,*  wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt und der Dezimalteil den Bruchteil eines Tags seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

DATETIME("30. Mai 1997")+5 t.
  
Liefert den Wert, der 04.06.97 darstellt.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(DATETIME("20/5/1997 14:30:45"),"C")
  
Liefert die Zeichenfolge "Dienstag, 20, Mai 1997, 14:30:45."
  
## <a name="example-3"></a>Beispiel 3

DATETIME("13:30 Juli 19")
  
Liefert den Wert, der den 19.7.2001 13:30:00 darstellt (wenn als aktuelles Jahr 2001 unterstellt wird).
  
## <a name="example-4"></a>Beispiel 4

DATETIME(35580.6337)
  
Liefert den Wert, der den 30.5.1997 15:12:32 darstellt.
  

