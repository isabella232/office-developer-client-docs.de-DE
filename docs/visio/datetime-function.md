---
title: DATETIME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Gibt den Datums-und Uhrzeitwert zurück, der durch DateTime oder Expression dargestellt wird.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360319"
---
# <a name="datetime-function"></a>DATETIME-Funktion

Gibt den Datums-und Uhrzeitwert zurück, der durch _DateTime_ oder _Expression_dargestellt wird.
  
## <a name="syntax"></a>Syntax

DATETIME ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Gibt den lokalen Bezeichner an, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

DateTime
  
## <a name="remarks"></a>Bemerkungen

Wenn *DateTime* fehlt oder nicht als gültige Datums-oder Uhrzeitangabe interpretiert werden kann, gibt datetime einen #VALUE zurück! zurück. 
  
Der Wert wird in dem kurzen Zeit- und Datumsformat geliefert, das aktuell in den länderspezifischen Systemeinstellungen festgelegt ist. 
  
Die DATETIME-Funktion akzeptiert auch einen einzelnen Zahlenwert für *Expression* , wobei der ganzzahlige Teil des Ergebnisses die Anzahl von Tagen seit dem 30. Dezember 1899 darstellt und der Dezimalteil den Bruchteil eines Tags seit Mitternacht darstellt. 
  
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

DATETIME (35580.6337)
  
Liefert den Wert, der den 30.5.1997 15:12:32 darstellt.
  

