---
title: SECOND-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Gibt eine ganze Zahl von 0 bis 59 zurück, die die Sekundenkomponente von DateTime oder Expression darstellt.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404876"
---
# <a name="second-function-visioshapesheet"></a>SECOND-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl von 0 bis 59 zurück, die die Sekundenkomponente von _DateTime_ oder _Expression_darstellt.
  
## <a name="syntax"></a>Syntax

Sekunde ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numeric** <br/> |Der Gebietsschemabezeichner, der beim Auswerten einer nicht lokalen _DateTime_verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in _DateTime_ oder _Expression_ wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn _DateTime_ fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion einen Fehler zurück. 
  
Die zweite Funktion akzeptiert auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tags seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

SEKUNDE ("05/30/1997 13:45:32")
  
Gibt 32 zurück.
  
## <a name="example-2"></a>Beispiel 2

SECOND(ZEITWERT("30. Mai 1996 12:07:45")+7 as.)
  
Gibt 52 zurück.
  
## <a name="example-3"></a>Beispiel 3

SEKUNDE (0.6337)
  
Gibt 32 zurück.
  

