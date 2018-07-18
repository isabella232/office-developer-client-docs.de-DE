---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Gibt eine ganze Zahl 0 und 59, die die Sekundenkomponente in Datetime oder Expression darstellt.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797977"
---
# <a name="second-function-visioshapesheet"></a>SECOND Function (VisioShapeSheet)

Gibt eine ganze Zahl 0 und 59, die die Sekundenkomponente in _Datetime_ oder _Expression_darstellt.
  
## <a name="syntax"></a>Syntax

ZWEITE ("** *Datetime* **" | ** *Ausdruck* ** [, ** *Lcid* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die allgemein als Datums- und Zeitangabe erkannt wird, oder ein Bezug auf eine Zelle mit einer Datums- und Zeitangabe.  <br/> |
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> | Beliebiger Ausdruck, der eine Datums- und Zeitangabe liefert.  <br/> |
| _lcid_ <br/> |Optional  <br/> |**Numerisch** <br/> |Die Gebietsschema-ID an, bei der Bewertung von Währungssymbole _Datetime_verwendet werden. Die Gebietsschema-ID ist eine Zahl, die in den Headerdateien System beschrieben.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Die Datumskomponente in _Datetime_ oder _Expression_ wird verworfen. 
  
Keine Rundung erfolgt. Wenn _Datetime_ nicht vorhanden ist oder nicht in ein gültiges Ergebnis konvertiert werden kann, gibt diese Funktion einen Fehler zurück. 
  
Die SECOND-Funktion nimmt auch einen einzelnen Zahlenwert für _Expression_ , wobei der Dezimalteil des Ergebnisses den Bruchteil eines Tages seit Mitternacht darstellt. 
  
## <a name="example-1"></a>Beispiel 1

SECOND("30/05/1997 13:45:32")
  
Gibt 32 zurück.
  
## <a name="example-2"></a>Beispiel 2

SECOND(ZEITWERT("30. Mai 1996 12:07:45")+7 as.)
  
Gibt 52 zurück.
  
## <a name="example-3"></a>Beispiel 3

SECOND(0.6337)
  
Gibt 32 zurück.
  

