---
title: FLOOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von Vielfaches.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797020"
---
# <a name="floor-function"></a>FLOOR Function

Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von _Vielfaches_.
  
## <a name="syntax"></a>Syntax

FLOOR (** *Anzahl* **, ** *mehrere* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die zu rundende Zahl.  <br/> |
| _mehrere_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Das Vielfache, auf das gerundet werden soll.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Hinweise

Wenn _mehrere_ nicht angegeben ist, wird die Zahl in Richtung 0 auf die nächste ganze Zahl gerundet. 
  
 _Anzahl_ und _Vielfaches_ müssen die gleichen Vorzeichen oder ein #NUM haben. Fehler wird zurückgegeben. Wenn _Zahl_ oder _mehrere_ auf einen Wert, der ein #VALUE konvertiert werden kann! Fehler wird zurückgegeben. Wenn _Zahl_ oder _mehrere_ 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

FLOOR(3.7)
  
Gibt 3 zurück.
  
## <a name="example-2"></a>Beispiel 2

FLOOR(-3.7)
  
Gibt -3 zurück.
  
## <a name="example-3"></a>Beispiel 3

FLOOR (3.7, 0,5)
  
Gibt 3,5 zurück.
  

