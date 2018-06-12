---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Gibt eine Ganzzahl zwischen 1 und 12, die einen Monat darstellt.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797531"
---
# <a name="month-function-visioshapesheet"></a>MONTH Function (VisioShapeSheet)

Gibt eine Ganzzahl zwischen 1 und 12, die einen Monat darstellt.
  
## <a name="syntax"></a>Syntax

Monat ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Nummer** <br/> |Der lokale Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Integer
  
## <a name="remarks"></a>Bemerkungen

Die Zeitkomponente in _Datetime_ oder _Expression_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn die Eingabezeichenfolge nicht angegeben wurde oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die MONTH-Funktion einen Fehler zurück.
  
Der Wert wird in dem Kurzdatumsformat zurückgegeben, der aktuell in den Ländereinstellungen des Systems festgelegt ist.
  
MONTH-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Ganzzahlteil des Ergebnisses für die Anzahl von Tagen seit dem 30. Dezember 1899 steht. 
  
## <a name="example-1"></a>Beispiel 1

MONTH("30. Mai 1999 13:45:24")
  
Gibt 5 zurück.
  
## <a name="example-2"></a>Beispiel 2

MONTH(DATUMSWERT("30. Mai 1999")+7 t.)
  
Gibt 6 zurück.
  
## <a name="example-3"></a>Beispiel 3

MONTH(35580.6337)
  
Gibt 5 zurück.
  

