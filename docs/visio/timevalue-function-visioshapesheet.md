---
title: TIMEVALUE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Gibt basierend auf den Regions-und Spracheinstellungen des Systems den Zeitwert zurück, der durch DateTime oder Expression dargestellt wird.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361110"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE-Funktion (VisioShapeSheet)

Gibt basierend auf den Regions-und Spracheinstellungen des Systems den Zeitwert zurück, der durch _DateTime_ oder _Expression_dargestellt wird.
  
## <a name="syntax"></a>Syntax

TIMEvalue ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine beliebige Datumskomponente in _DateTime_ oder _Expression_ wird verworfen. 
  
Wenn _DateTime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese funktion einen #VALUE! zurück. 
  
Die TIMEvalue-Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tags seit Mitternacht darstellt. 
  
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

TIMEVALUE (0.6337)
  
Gibt den Wert für 15:12:32 zurück.
  
## <a name="example-5"></a>Beispiel 5

TIMEVALUE ("7:89")
  
Gibt einen Fehler vom Typ #WERT! zurück.
  

