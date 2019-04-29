---
title: ROUND-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Rundet eine Zahl auf die von Wert von AnzahlVonStellen dargestellte Genauigkeit.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439968"
---
# <a name="round-function-visioshapesheet"></a>ROUND-Funktion (VisioShapeSheet)

Rundet eine Zahl auf die von *Wert von AnzahlVonStellen* dargestellte Genauigkeit. 
  
## <a name="syntax"></a>Syntax

ROUND (* * *Number* * *, * * *Wert von AnzahlVonStellen* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _Wert von AnzahlVonStellen_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Anzahl der Dezimalstellen für den Grad der Genauigkeit.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn _Wert von AnzahlVonStellen_ größer als 0 ist, wird die _Zahl_ von _Wert von AnzahlVonStellen_ rechts vom Dezimaltrennzeichen gerundet. Wenn _Wert von AnzahlVonStellen_ 0 ist, wird _Zahl_ auf eine ganze Zahl gerundet. Wenn _Wert von AnzahlVonStellen_ kleiner als 0 ist, wird die _Zahl_ von _Wert von AnzahlVonStellen_ Links vom Dezimaltrennzeichen gerundet. 
  
## <a name="example-1"></a>Beispiel 1

ROUND (123.654, 2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

ROUND (123.654, 0)
  
Gibt 124 zurück.
  
## <a name="example-3"></a>Beispiel 3

ROUND (123.654,-1)
  
Gibt 120 zurück.
  

