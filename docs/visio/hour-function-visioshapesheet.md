---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Gibt eine ganze Zahl von 0 bis 23 für die Stunde des Tages in Datetime oder Expression zurück.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797162"
---
# <a name="hour-function-visioshapesheet"></a>HOUR Function (VisioShapeSheet)

Gibt eine ganze Zahl von 0 bis 23 für die Stunde des Tages in _Datetime_ oder _Expression_zurück.
  
## <a name="syntax"></a>Syntax

Stunde ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> | Eine Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Ein Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Nummer** <br/> | Ein lokaler Bezeichner, der bei der Auswertung eines nicht lokalen Werts für datetime verwendet werden soll. Der lokale Bezeichner ist eine Zahl, die in den Systemkopfdateien beschrieben wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in *Datetime* und *Expression* wird verworfen. 
  
Keine Rundung erfolgt. Die *Datetime* ist nicht vorhanden oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt die Funktion einen Fehler zurück. 
  
Der zurückgegebene  Wert wird in dem Zeitformat angezeigt, das aktuell in den Ländereinstellungen des Systems festgelegt ist. 
  
Die HOUR-Funktion nimmt auch einen einzelnen Zahlenwert für *Expression* , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

HOUR("15:45")
  
Gibt 15 zurück.
  
## <a name="example-2"></a>Beispiel 2

HOUR("30. Mai 1997 15:45:24")
  
Gibt 15 zurück.
  
## <a name="example-3"></a>Beispiel 3

HOUR(0.5)
  
Gibt 12 zurück.
  
## <a name="example-4"></a>Beispiel 4

HOUR("30/5/1997")
  
Gibt 0 zurück.
  

