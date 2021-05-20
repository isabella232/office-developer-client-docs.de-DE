---
title: MONTH-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Gibt eine ganze Zahl von 1 bis 12 zurück, die einen Monat darstellt.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431974"
---
# <a name="month-function-visioshapesheet"></a>MONTH-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl von 1 bis 12 zurück, die einen Monat darstellt.
  
## <a name="syntax"></a>Syntax

MONTH(" ** *datetime* ** "| ** *Ausdruck* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional.  <br/> |**Number** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente  _von datetime_ oder  _ausdruck_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn die Eingabezeichenfolge nicht angegeben wurde oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die MONTH-Funktion einen Fehler zurück.
  
Der Wert wird in dem Kurzdatumsformat zurückgegeben, der aktuell in den Ländereinstellungen des Systems festgelegt ist.
  
Die MONTH-Funktion akzeptiert auch  einen einzelnen Zahlenwert für ausdruck, wobei der ganzzahlige Teil des Ergebnisses die Anzahl der Tage seit dem 30. Dezember 1899 darstellt. 
  
## <a name="example-1"></a>Beispiel 1

MONTH("30. Mai 1999 13:45:24")
  
Gibt 5 zurück.
  
## <a name="example-2"></a>Beispiel 2

MONTH(DATUMSWERT("30. Mai 1999")+7 t.)
  
Gibt 6 zurück.
  
## <a name="example-3"></a>Beispiel 3

MONTH(35580.6337)
  
Gibt 5 zurück.
  

