---
title: STRSAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Bestimmt, ob die Zeichenfolgen identisch sind. Es gibt TRUE zurück, wenn sie identisch sind, und FALSE, wenn sie nicht.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798190"
---
# <a name="strsame-function"></a>STRSAME-Funktion

Bestimmt, ob die Zeichenfolgen identisch sind. Es gibt TRUE zurück, wenn sie identisch sind, und FALSE, wenn sie nicht. 
  
## <a name="syntax"></a>Syntax

STRSAME ("** *Zeichenfolge1* **","** *Zeichenfolge2* **", ** *IgnoreCase* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeichenfolge1_ <br/> |Erforderlich  <br/> |**String** <br/> |Die erste zu vergleichende Zeichenfolge.  <br/> |
| _Zeichenfolge2_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zweite zu vergleichende Zeichenfolge.  <br/> |
| _ignoreCase_ <br/> |Optional  <br/> |**Boolean** <br/> |TRUE steht für "Groß- und Kleinschreibung ignorieren" und FALSE für "Groß- und Kleinschreibung berücksichtigen". Die Standardeinstellung ist FALSE.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Boolescher Wert
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche mit Groß- und Kleinschreibregeln für ein bestimmtes Gebietsschema durchführen möchten, verwenden Sie die STRSAMEEX-Funktion.
  
## <a name="example-1"></a>Beispiel 1

STRSAME("Katze","Hund")
  
Gibt FALSE zurück.
  
## <a name="example-2"></a>Beispiel 2

STRSAME("Katze","Katze")
  
Gibt TRUE zurück.
  
## <a name="example-3"></a>Beispiel 3

STRSAME("Katze","Katze", WAHR)
  
Gibt TRUE zurück.
  
## <a name="example-4"></a>Beispiel 4

STRSAME("katze","KATZE")
  
Gibt FALSE zurück.
  
## <a name="example-5"></a>Beispiel 5

STRSAME("katze","KATZE", WAHR)
  
Gibt TRUE zurück.
  
## <a name="example-6"></a>Beispiel 6

STRSAME("kätze","KATZE", WAHR)
  
Gibt FALSE zurück.
  
## <a name="example-7"></a>Beispiel 7

STRSAME("kätze","KÄTZE", WAHR)
  
Gibt TRUE zurück.
  

