---
title: SETF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Legt die Formel einer Zelle fest.
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797996"
---
# <a name="setf-function"></a>SETF Function

Legt die Formel einer Zelle fest. 
  
## <a name="syntax"></a>Syntax

SETF (GETREF (** *Zelle* **), ** *Formel* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zelle_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zelle, deren Formel festgelegt.  <br/> |
| _formula_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu verwendende Formel.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ausgewertet, wird das Ergebnis des Ausdrucks in _Formel_ als neue Formel in _Zelle_. Wenn die _Formel_ in Anführungszeichen eingeschlossen ist, wird der Ausdruck in Anführungszeichen in _Zelle_geschrieben. Um eine _Zelle_ in eine Zeichenfolge festgelegt, setzen Sie _Formel_ in drei Gruppen von Anführungszeichen. 
  
Die Zielzelle muss mithilfe eines GETREF()-Bezugs oder als Zeichenfolge angegeben werden, um eine Zirkularität zu vermeiden. Die Verwendung von GETREF wird bevorzugt, da Bezüge in Microsoft Visio angepasst werden können, wenn das Shape in ein anderes Dokument verschoben wird.
  
Wenn _Zelle_ mithilfe GETREF nicht angegeben ist oder als eine Zeichenfolge ist, gibt die Funktion einen Fehler zurück, und keine Formel geändert wird. Wenn die _Formel_ einen Syntaxfehler enthält, gibt die Funktion einen Fehler zurück, und die Formel in _Zelle_ wird nicht geändert. 
  
## <a name="example-1"></a>Beispiel 1

SETF (SETF(GETREF(Scratch.a1), 1,5 cm \* 6 + 1 ft)
  
Legt die Formel von Scratch.A1 auf 39 cm fest.
  
## <a name="example-2"></a>Beispiel 2

SETF (GETREF(Scratch.A1), "1,5 cm \* 6 + 1 ft")
  
Legt die Formel von Scratch. A1 auf den Ausdruck 1,5 in\*6 + 1 ft.
  
## <a name="example-3"></a>Beispiel 3

SETF( GETREF(Scratch.A1), """Sag """"ahh""""""")
  
Legt die Formel von Scratch.A1 auf die Zeichenfolge "Sag ""ahh""" fest, die in Sag "ahh" ausgewertet wird.
  

