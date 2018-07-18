---
title: HSL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe durch seine Farbton, Sättigung und Helligkeit Komponenten.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797166"
---
# <a name="hsl-function"></a>HSL-Funktion

Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe durch seine Farbton, Sättigung und Helligkeit Komponenten.
  
## <a name="syntax"></a>Syntax

HSL (** *Farbton* **, ** *Sättigung* **, ** *Helligkeit* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Farbton_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Der Farbton einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 239 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.  <br/> |
| _Sättigung_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Sättigung einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 240 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.  <br/> |
| _Helligkeit_ <br/> |Erforderlich  <br/> |**Nummer** <br/> | Die Helligkeit einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 240 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie der Liste der verfügbaren Farben im Dokument hinzugefügt. 
  
In der folgenden Tabelle sind einige Standardfarben mit ihren Farbton-, Sättigungs- und Helligkeitswerten aufgelistet. 
  
|**Color**|**Farbton**|**Sättigung**|**Helligkeitswert**|
|:-----|:-----|:-----|:-----|
|Schwarz  <br/> |0  <br/> |0  <br/> |24  <br/> |
|Blau  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Grün  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Cyan  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Rot  <br/> |0  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Gelb  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Weiß  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Beispiel 1

HSL(160,240,120)
  
Gibt den Index für die Farbe Blau zurück.
  
## <a name="example-2"></a>Beispiel 2

HSL(Hue(FillForegnd),SAT(FillForegnd),Min(LUM(FillForegnd)+100,240))
  
Gibt den Index für eine Farbe zurück, der die Vordergrundfüllfarbe mit erhöhter Helligkeit darstellt.
  

