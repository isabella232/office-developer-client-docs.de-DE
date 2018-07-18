---
title: TIMEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Gibt der Time-Wert dargestellt durch Datetime oder Expression, basierend auf dem System Region und Sprache Einstellungen.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798276"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE Function (VisioShapeSheet)

Gibt der Time-Wert dargestellt durch _Datetime_ oder _Expression_, basierend auf dem System Region und Sprache Einstellungen.
  
## <a name="syntax"></a>Syntax

TIMEVALUE ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Varies** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Nummer** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Alle Datumskomponenten in _Datetime_ oder _Expression_ wird verworfen. 
  
Wenn _Datetime_ nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion ein #VALUE! Fehler. 
  
Die TIMEVALUE-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

TIMEVALUE("06:00")
  
Gibt den Wert für 06:00 zurück.
  
## <a name="example-2"></a>Beispiel 2

TIMEVALUE("14:30")+4 vs.+30 vm.
  
Gibt den Wert für 19:00:00 zurück.
  
## <a name="example-3"></a>Beispiel 3

TIMEVALUE("11:00, 1. Juli 1997")
  
Gibt den Wert für 11:00 zurück.
  
## <a name="example-4"></a>Beispiel 4

TIMEVALUE(0.6337)
  
Gibt den Wert für 15:12:32 zurück.
  
## <a name="example-5"></a>Beispiel 5

TIMEVALUE("7:89")
  
Gibt einen Fehler vom Typ #WERT! zurück.
  

