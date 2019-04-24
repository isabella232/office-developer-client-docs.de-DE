---
title: STRSAMEEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Bestimmt, ob zwei Zeichenfolgen identisch sind.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329792"
---
# <a name="strsameex-function"></a>STRSAMEEX Function

Bestimmt, ob zwei Zeichenfolgen identisch sind.
  
## <a name="syntax"></a>Syntax

STRSAMEEX ("* * *string1* * *", "* * *string2* * *", * * *Gebietsschema* -Nr. * *, * * *Flag* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Erforderlich  <br/> |**String** <br/> |Die erste zu vergleichende Zeichenfolge.  <br/> |
| _string2_ <br/> |Erforderlich  <br/> |**String** <br/> | Die zweite zu vergleichende Zeichenfolge.  <br/> |
| _localeID_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der lokale ID-Code.  <br/> |
| _Flag_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> | Ein Bit, das den Typ des Vergleichs bestimmt.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

STRSAMEEX gibt TRUE zurück, wenn beide Eingabezeichenfolgen identisch sind, und FALSE, wenn dies nicht der Fall ist. Mit dieser Funktion können Sie Multi-Byte-Zeichenfolgenvergleichen oder Vergleiche ausführen, die Fall Regeln für ein bestimmtes Gebietsschema verwenden.
  
Sie können eine beliebige Kombination folgender Flags mit der STRGLEICHEX-Funktion verwenden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1  <br/> |Groß- und Kleinschreibung ignorieren.  <br/> |
|2  <br/> |Nicht-gesperrte Zeichen ignorieren.  <br/> |
|4  <br/> |Symbole ignorieren.  <br/> |
|4096  <br/> |Interpunktionszeichen wie Symbole behandeln.  <br/> |
|65536  <br/> |Nicht zwischen Hiragana- und Katakana-Zeichen unterscheiden.  <br/> |
|131072  <br/> |Nicht zwischen Einzel-Byte-Zeichen und dem gleichen Zeichen als Doppel-Byte-Zeichen unterscheiden.  <br/> |
   

