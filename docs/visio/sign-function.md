---
title: SIGN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
ms.localizationpriority: medium
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Gibt einen Wert zurück, der das Vorzeichen einer Zahl darstellt.
ms.openlocfilehash: ea7ed2ec4cacb6d926d907934f8745b8ab7538ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622822"
---
# <a name="sign-function"></a>SIGN Function

Gibt einen Wert zurück, der das Vorzeichen einer Zahl darstellt. 
  
## <a name="syntax"></a>Syntax

SIGN(** *number* **, ** *fuzz* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> | Die Zahl, für die das Vorzeichen bestimmt werden soll.  <br/> |
| _Fuzz_ <br/> |Optional  <br/> |**Numeric** <br/> |Gibt an, wie klein der Wert einer Zahl sein muss, damit diese als gleich 0 (null) betrachtet wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numeric
  
## <a name="remarks"></a>Bemerkungen

Die SIGN-Funktion gibt 1 zurück, wenn  _die Zahl_ positiv ist, 0, wenn  _Zahl_ null ist, oder -1, wenn  _die Zahl_ negativ ist. 
  
Die Angabe eines  _Fuzzwerts_ hilft, Gleitkomma-Roundofffehler zu vermeiden, wenn eine Berechnung fast null ist. Wenn Sie keinen _Fuzzwert_ angeben, verwendet Visio 1E-9 (0,0000000001). Sie können bei Bedarf einen anderen Wert angeben, wenn Sie Zeichnungen skalieren möchten oder einen exakten Vergleich anstreben. 
  
## <a name="example-1"></a>Beispiel 1

SIGN(-5)
  
Gibt -1 zurück.
  
## <a name="example-2"></a>Beispiel 2

SIGN(0)
  
Gibt 0 zurück.
  
## <a name="example-3"></a>Beispiel 3

SIGN(0,000000000001)
  
Gibt 0 zurück.
  
## <a name="example-4"></a>Beispiel 4

SIGN(0,000000000001,0)
  
Gibt 1 zurück.
  

