---
title: SETF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
ms.localizationpriority: medium
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Legt die Formel einer Zelle fest.
ms.openlocfilehash: cb474104a76ab45f45a03e15f9c9e3facd0ad88a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622942"
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
   
## <a name="remarks"></a>Bemerkungen

Bei der Auswertung wird das Ergebnis des Ausdrucks in der  _Formel_ zur neuen Formel in  _zelle_. Wenn  _die Formel_ in Anführungszeichen eingeschlossen ist, wird der in Anführungszeichen gesetzte Ausdruck in die  _Zelle_ geschrieben. Um eine  _Zelle_ auf eine Zeichenfolge festzulegen, schließen Sie  _die Formel_ in drei Anführungszeichen ein. 
  
Die Zielzelle muss mithilfe eines GETREF()-Bezugs oder als Zeichenfolge angegeben werden, um eine Zirkularität zu vermeiden. Die Verwendung von GETREF wird bevorzugt, da Bezüge in Microsoft Visio angepasst werden können, wenn das Shape in ein anderes Dokument verschoben wird.
  
Wenn  _die Zelle_ nicht mit GETREF oder als Zeichenfolge angegeben wird, gibt die Funktion einen Fehler zurück, und die Formel der Zelle wird nicht geändert. Wenn  _die Formel_ einen Syntaxfehler enthält, gibt die Funktion einen Fehler zurück, und die Formel in der  _Zelle_ wird nicht geändert. 
  
## <a name="example-1"></a>Beispiel 1

SETF( GETREF(Scratch.A1), 1,5 in \* 6 + 1 ft)
  
Legt die Formel von Scratch.A1 auf 39 cm fest.
  
## <a name="example-2"></a>Beispiel 2

SETF( GETREF(Scratch.A1), "1,5 in \* 6 + 1 ft")
  
Legt die Formel für Scratch. A1 bis zum Ausdruck 1,5 in \* 6+1 fuß.
  
## <a name="example-3"></a>Beispiel 3

SETF( GETREF(Scratch.A1), """Sag """"ahh""""""")
  
Legt die Formel von Scratch.A1 auf die Zeichenfolge "Sag ""ahh""" fest, die in Sag "ahh" ausgewertet wird.
  

