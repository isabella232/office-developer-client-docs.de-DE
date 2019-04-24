---
title: HOUR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Gibt eine ganze Zahl von 0 bis 23 zurück, die die Stunde des Tages von DateTime oder Expression darstellt.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329967"
---
# <a name="hour-function-visioshapesheet"></a>HOUR-Funktion (VisioShapeSheet)

Gibt eine ganze Zahl von 0 bis 23 zurück, die die Stunde des Tages von _DateTime_ oder _Expression_darstellt.
  
## <a name="syntax"></a>Syntax

HOUR ("* * *DateTime* * *" | * * *Expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Eine Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Number** <br/> | Ein lokaler Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in *DateTime* und *Expression* wird verworfen. 
  
Es findet kein Auf- oder Abrunden statt. Wenn *DateTime* fehlt oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Der zurückgegebene Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist. 
  
Die HOUR-Funktion akzeptiert auch einen einzelnen Zahlenwert für *Expression* , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tags seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

STUNDE ("15:45")
  
Gibt 15 zurück.
  
## <a name="example-2"></a>Beispiel 2

HOUR("30. Mai 1997 15:45:24")
  
Gibt 15 zurück.
  
## <a name="example-3"></a>Beispiel 3

STUNDE (0,5)
  
Gibt 12 zurück.
  
## <a name="example-4"></a>Beispiel 4

HOUR ("5/30/1997")
  
Gibt 0 zurück.
  

