---
title: PLAYSOUND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Gibt eine Sounddatei oder einen Systemsound wieder.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346844"
---
# <a name="playsound-function"></a>PLAYSOUND Function

Gibt eine Sounddatei oder einen Systemsound wieder. 
  
## <a name="syntax"></a>Syntax

PlaySound ("* * *filename* * *" | "* * *Alias* * *", * * *isalias* * *, * * *Beep* * *, * * *Synch* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Audiodatei, die abgespielt werden soll.  <br/> |
| _alias_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Systemsignal, das durch einen Alias dargestellt wird.  <br/> |
| _isAlias_ <br/> |Erforderlich  <br/> |**Boolean** <br/> | Gibt an, ob der vorangegangene Ausdruck ein Alias oder ein Dateiname ist. Verwenden Sie einen Wert ungleich null zur Angabe eines Alias.  <br/> |
| _Signalton_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, ob Microsoft Visio eine akustische Meldung ausgibt, wenn der Sound nicht abgespielt werden kann. Verwenden Sie einen Wert ungleich null, um ein akustisches Signal zu veranlassen.  <br/> |
| _Synch_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Bestimmt, ob Klänge asynchron (0) oder synchron (1) abgespielt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie sollten Sounds in der Regel asynchron abspielen, damit Visio die Verarbeitung fortsetzen kann, während der Sound wiedergegeben wird. Um mehrere Sounds miteinander zu verbinden, spielen Sie sie synchron ab, oder es kann ein Fehler auftreten. 
  
## <a name="example-1"></a>Beispiel 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
Spielt die Wave-Datei chord.wav asynchron und ohne akustische Warnung ab.
  
## <a name="example-2"></a>Beispiel 2

PLAYSOUND("Systemklang", 1, 0, 0)
  
Spielt das Systemsignal für Hinweise asynchron und ohne akustische Warnung ab.
  

