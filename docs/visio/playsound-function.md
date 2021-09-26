---
title: PLAYSOUND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
ms.localizationpriority: medium
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Gibt eine Sounddatei oder einen Systemsound wieder.
ms.openlocfilehash: 7dab11245389c02054b5f3d626334867dcbad437
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627716"
---
# <a name="playsound-function"></a>PLAYSOUND Function

Gibt eine Sounddatei oder einen Systemsound wieder. 
  
## <a name="syntax"></a>Syntax

PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Dateiname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Audiodatei, die abgespielt werden soll.  <br/> |
| _alias_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Systemsignal, das durch einen Alias dargestellt wird.  <br/> |
| _isAlias_ <br/> |Erforderlich  <br/> |**Boolean** <br/> | Gibt an, ob der vorangegangene Ausdruck ein Alias oder ein Dateiname ist. Verwenden Sie einen Wert ungleich null zur Angabe eines Alias.  <br/> |
| _Beep_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, ob Microsoft Visio eine akustische Meldung ausgibt, wenn der Sound nicht abgespielt werden kann. Verwenden Sie einen Wert ungleich null, um ein akustisches Signal zu veranlassen.  <br/> |
| _Synch_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Bestimmt, ob Klänge asynchron (0) oder synchron (1) abgespielt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sounds sollten normalerweise asynchron abgespielt werden, damit Visio fortgesetzt werden kann, während der Sound abgespielt wird. Wenn Sie mehrere Sounds hintereinander abspielen möchten, sollten Sie diese synchron abspielen. Sonst könnte es geschehen, dass einige nicht abgespielt werden.
 
  
## <a name="example-1"></a>Beispiel 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
Spielt die Wave-Datei chord.wav asynchron und ohne akustische Warnung ab.
  
## <a name="example-2"></a>Beispiel 2

PLAYSOUND("Systemklang", 1, 0, 0)
  
Spielt das Systemsignal für Hinweise asynchron und ohne akustische Warnung ab.
  

