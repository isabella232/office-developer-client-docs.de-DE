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
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798212"
---
# <a name="strsameex-function"></a>STRSAMEEX Function

Bestimmt, ob zwei Zeichenfolgen identisch sind.
  
## <a name="syntax"></a>Syntax

STRSAMEEX ("** *Zeichenfolge1* **","** *Zeichenfolge2* **", ** *LocaleID* **, ** *Flag* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeichenfolge1_ <br/> |Erforderlich  <br/> |**String** <br/> |Die erste zu vergleichende Zeichenfolge.  <br/> |
| _Zeichenfolge2_ <br/> |Erforderlich  <br/> |**String** <br/> | Die zweite zu vergleichende Zeichenfolge.  <br/> |
| _Gebietsschema-ID_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der lokale ID-Code.  <br/> |
| _Flag_ <br/> |Erforderlich  <br/> |**Numeric** <br/> | Ein Bit, das den Typ des Vergleichs bestimmt.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Boolean
  
## <a name="remarks"></a>Bemerkungen

STRSAMEEX gibt TRUE zurück, wenn beide Eingabezeichenfolgen identisch sind. Ist dies nicht der Fall, wird FALSE zurückgegeben. Verwenden Sie diese Funktion, wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche mit Groß- und Kleinschreibregeln für ein bestimmtes Gebietsschema durchführen möchten.
			

  
Sie können eine beliebige Kombination folgender Flags mit der STRGLEICHEX-Funktion verwenden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1  <br/> |Groß- und Kleinschreibung ignorieren.  <br/> |
|2  <br/> |Nicht-gesperrte Zeichen ignorieren.  <br/> |
|4  <br/> |Symbole ignorieren.  <br/> |
|4096  <br/> |Interpunktionszeichen wie Symbole behandeln.  <br/> |
|65536  <br/> |Nicht zwischen Hiragana- und Katakana-Zeichen unterscheiden.  <br/> |
|131072  <br/> |Nicht zwischen Einzel-Byte-Zeichen und dem gleichen Zeichen als Doppel-Byte-Zeichen unterscheiden.  <br/> |
   

