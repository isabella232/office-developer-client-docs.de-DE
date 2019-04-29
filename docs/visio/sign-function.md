---
title: SIGN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Gibt einen Wert zurück, der das Zeichen einer Zahl darstellt.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420654"
---
# <a name="sign-function"></a>SIGN Function

Gibt einen Wert zurück, der das Zeichen einer Zahl darstellt. 
  
## <a name="syntax"></a>Syntax

SIGN (* * *Number* * *, * * *Fuzz* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> | Die Zahl, für die das Vorzeichen bestimmt werden soll.  <br/> |
| _Fuzz_ <br/> |Optional  <br/> |**Numeric** <br/> |Gibt an, wie klein der Wert einer Zahl sein muss, damit diese als gleich 0 (null) betrachtet wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numeric
  
## <a name="remarks"></a>Bemerkungen

Die SIGN-Funktion gibt 1 zurück, wenn _Number_ positiv ist __ , 0, wenn Number gleich NULL ist, oder-1, wenn _Number_ negativ ist. 
  
Angeben in ein _Fuzz_ -Wert hilft beim Vermeiden von Gleitkomma-Rundungs-Fehlern, wenn eine Berechnung fast null ist. Wenn Sie keinen _Fuzz_ -Wert angeben, verwendet Visio 1E-9 (0,000000001). Sie können bei Bedarf einen anderen Wert angeben, wenn Sie Zeichnungen skalieren möchten oder einen exakten Vergleich anstreben. 
  
## <a name="example-1"></a>Beispiel 1

SIGN (-5)
  
Gibt -1 zurück.
  
## <a name="example-2"></a>Beispiel 2

SIGN (0)
  
Gibt 0 zurück.
  
## <a name="example-3"></a>Beispiel 3

SIGN (0.00000000001)
  
Gibt 0 zurück.
  
## <a name="example-4"></a>Beispiel 4

SIGN (0.00000000001, 0)
  
Gibt 1 zurück.
  

