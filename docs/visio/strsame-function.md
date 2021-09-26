---
title: STRSAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
ms.localizationpriority: medium
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Bestimmt, ob Zeichenfolgen identisch sind. Es gibt TRUE zurück, wenn sie identisch sind, und FALSE, wenn dies nicht der Fall ist.
ms.openlocfilehash: 502d1b782c900d872b95a790cad38416b8d851dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603438"
---
# <a name="strsame-function"></a>STRSAME Function

Bestimmt, ob Zeichenfolgen identisch sind. Es gibt TRUE zurück, wenn sie identisch sind, und FALSE, wenn dies nicht der Fall ist. 
  
## <a name="syntax"></a>Syntax

STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Erforderlich  <br/> |**String** <br/> |Die erste zu vergleichende Zeichenfolge.  <br/> |
| _string2_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zweite zu vergleichende Zeichenfolge.  <br/> |
| _Ignorecase_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |TRUE steht für "Groß- und Kleinschreibung ignorieren" und FALSE für "Groß- und Kleinschreibung berücksichtigen". Die Standardeinstellung ist FALSE.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche mit Groß- und Kleinschreibregeln für ein bestimmtes Gebietsschema durchführen möchten, verwenden Sie die STRSAMEEX-Funktion.
  
## <a name="example-1"></a>Beispiel 1

STRSAME("cat","dog")
  
Gibt FALSE zurück.
  
## <a name="example-2"></a>Beispiel 2

STRSAME("cat","cat")
  
Gibt TRUE zurück.
  
## <a name="example-3"></a>Beispiel 3

STRSAME("Katze","Katze", WAHR)
  
Gibt TRUE zurück.
  
## <a name="example-4"></a>Beispiel 4

STRSAME("cat","CAT")
  
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
  

