---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Rundet eine Zahl auf die durch AnzahlVonStellen dargestellte Präzision.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19797883"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Rundet eine Zahl auf die durch *AnzahlVonStellen* dargestellte Präzision. 
  
## <a name="syntax"></a>Syntax

ROUND (** *Anzahl* **, ** *AnzahlVonStellen* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die zu rundende Zahl.  <br/> |
| _AnzahlVonStellen_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Anzahl der Dezimalstellen für den Grad der Genauigkeit.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der _Wert von AnzahlVonStellen_ größer als 0 ist, wird die _Zahl_ durch _AnzahlVonStellen_ rechts vom Dezimalkomma gerundet. Wenn _AnzahlVonStellen_ 0 ist, wird die _Zahl_ in eine ganze Zahl gerundet. Wenn der _Wert von AnzahlVonStellen_ kleiner als 0 ist, wird die _Zahl_ durch _AnzahlVonStellen_ links vom Dezimalkomma gerundet. 
  
## <a name="example-1"></a>Beispiel 1

ROUND(123.654,2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

ROUND(123.654,0)
  
Gibt 124 zurück.
  
## <a name="example-3"></a>Beispiel 3

ROUND(123.654,-1)
  
Gibt 120 zurück.
  

