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
description: Eine Audiodatei oder Systemsound wiedergegeben.
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797653"
---
# <a name="playsound-function"></a>PLAYSOUND Function

Eine Audiodatei oder Systemsound wiedergegeben. 
  
## <a name="syntax"></a>Syntax

PLAYSOUND ("** *Filename* **" | "** *Alias* **", ** *istAlias* **, ** *Beep* **, ** *Synch* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Dateiname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Audiodatei, die abgespielt werden soll.  <br/> |
| _alias_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Systemsignal, das durch einen Alias dargestellt wird.  <br/> |
| _istAlias_ <br/> |Erforderlich  <br/> |**Boolean** <br/> | Gibt an, ob der vorangegangene Ausdruck ein Alias oder ein Dateiname ist. Verwenden Sie einen Wert ungleich null zur Angabe eines Alias.  <br/> |
| _Signalton_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, ob Microsoft Visio eine akustische Meldung ausgibt, wenn der Sound nicht abgespielt werden kann. Verwenden Sie einen Wert ungleich null, um ein akustisches Signal zu veranlassen.  <br/> |
| _Synch_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Bestimmt, ob Klänge asynchron (0) oder synchron (1) abgespielt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie sollten in der Regel Sounds asynchron wiedergegeben werden sollen, damit Visio fortgeführt werden kann, während es der Sound wiedergegeben wird. Mehrere Sounds hintereinander abspielen möchten, deren synchron oder einige möglicherweise nicht wiedergegeben werden sollen. 
  
## <a name="example-1"></a>Beispiel 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
Spielt die Wave-Datei chord.wav asynchron und ohne akustische Warnung ab.
  
## <a name="example-2"></a>Beispiel 2

PLAYSOUND("Systemklang", 1, 0, 0)
  
Spielt das Systemsignal für Hinweise asynchron und ohne akustische Warnung ab.
  

