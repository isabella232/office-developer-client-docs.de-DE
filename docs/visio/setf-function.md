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
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425974"
---
# <a name="setf-function"></a>SETF Function

Legt die Formel einer Zelle fest. 
  
## <a name="syntax"></a>Syntax

SETF( GETREF(** *cell* ** ), ** *formula* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zelle_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zelle, deren Formel festgelegt werden soll.  <br/> |
| _formula_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu verwendende Formel.  <br/> |
   
## <a name="remarks"></a>Hinweise

Bei der Auswertung wird das Ergebnis des Ausdrucks in  _der Formel_ zur neuen Formel in  _zelle_. Wenn _formel_ in Anführungszeichen eingeschlossen ist, wird der in Anführungszeichen gesetzte Ausdruck in die Zelle _geschrieben._ Um die  _Zelle auf_ eine Zeichenfolge zu setzen, setzen Sie  _die Formel_ in drei Sätze von Anführungszeichen. 
  
Die Zielzelle muss mithilfe eines GETREF()-Bezugs oder als Zeichenfolge angegeben werden, um eine Zirkularität zu vermeiden. Die Verwendung von GETREF wird bevorzugt, da Bezüge in Microsoft Visio angepasst werden können, wenn das Shape in ein anderes Dokument verschoben wird.
  
Wenn  _zelle_ nicht mit GETREF oder als Zeichenfolge angegeben wird, gibt die Funktion einen Fehler zurück, und die Formel der Zelle wird nicht geändert. Wenn  _die Formel_ einen Syntaxfehler enthält, gibt die Funktion einen Fehler zurück, und die Formel in  _der_ Zelle wird nicht geändert. 
  
## <a name="example-1"></a>Beispiel 1

SETF( GETREF(Scratch.A1), 1,5 in \* 6 + 1 ft)
  
Legt die Formel von Scratch.A1 auf 39 cm fest.
  
## <a name="example-2"></a>Beispiel 2

SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")
  
Legt die Formel für Scratch. A1 bis zum Ausdruck 1,5 in \* 6+1 ft.
  
## <a name="example-3"></a>Beispiel 3

SETF( GETREF(Scratch.A1), """Sag """"ahh""""""")
  
Legt die Formel von Scratch.A1 auf die Zeichenfolge "Sag ""ahh""" fest, die in Sag "ahh" ausgewertet wird.
  

