---
title: TIMEVALUE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
ms.localizationpriority: medium
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Gibt basierend auf den Einstellungen für Region und Sprache des Systems den durch datetime oder Expression dargestellten Zeitwert zurück.
ms.openlocfilehash: 19b6d92fa5efeb1f9881e429a3368b20b3bc9893
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549469"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE-Funktion (VisioShapeSheet)

Gibt basierend auf den Einstellungen für Region und Sprache des Systems den Zeitwert zurück, der durch _Datum/Uhrzeit_ oder Ausdruck dargestellt wird. 
  
## <a name="syntax"></a>Syntax

TIMEVALUE(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Datetime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Jede Datumskomponente in _datetime_ oder Expression wird verworfen.  
  
Wenn  _datetime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion eine #VALUE! zurück. 
  
Die TIMEVALUE-Funktion akzeptiert auch einen einzelnen Zahlenwert für  _einen Ausdruck,_ bei dem der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt. 
  
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

TIMEVALUE(0,6337)
  
Gibt den Wert für 15:12:32 zurück.
  
## <a name="example-5"></a>Beispiel 5

TIMEVALUE("7:89")
  
Gibt einen Fehler vom Typ #WERT! zurück.
  

