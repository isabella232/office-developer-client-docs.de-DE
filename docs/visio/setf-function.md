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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325837"
---
# <a name="setf-function"></a>SETF Function

Legt die Formel einer Zelle fest. 
  
## <a name="syntax"></a>Syntax

Setf (GETREF (* * *Cell* * *), * * *Formel* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zelle_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zelle, deren Formel festgelegt werden soll.  <br/> |
| _formula_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu verwendende Formel.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei der Auswertung wird das Ergebnis des Ausdrucks in der _Formel_ zur neuen Formel in _Cell_. Wenn die _Formel_ in Anführungszeichen eingeschlossen ist, wird der zitierte Ausdruck in _Cell_geschrieben. Um eine _Zelle_ auf eine Zeichenfolge festzulegen, müssen Sie die _Formel_ in drei Gruppen von Anführungszeichen einschließen. 
  
Die Zielzelle muss mithilfe eines GETREF()-Bezugs oder als Zeichenfolge angegeben werden, um eine Zirkularität zu vermeiden. Die Verwendung von GETREF wird bevorzugt, da Bezüge in Microsoft Visio angepasst werden können, wenn das Shape in ein anderes Dokument verschoben wird.
  
Wenn _Cell_ nicht mit getref oder als Zeichenfolge angegeben wird, gibt die Funktion einen Fehler zurück, und die Formel der Zelle wird nicht geändert. Wenn die _Formel_ einen Syntaxfehler enthält, gibt die Funktion einen Fehler zurück, und die Formel in _Cell_ wird nicht geändert. 
  
## <a name="example-1"></a>Beispiel 1

SETF (GETREF (Scratch. a1), 1,5 in \* 6 + 1 ft)
  
Legt die Formel von Scratch.A1 auf 39 cm fest.
  
## <a name="example-2"></a>Beispiel 2

SETF (GETREF (Scratch. a1), "1,5 in \* 6 + 1 ft")
  
Legt die Formel für Scratch. A1 auf den Ausdruck 1,5 in\*6 + 1 ft.
  
## <a name="example-3"></a>Beispiel 3

SETF( GETREF(Scratch.A1), """Sag """"ahh""""""")
  
Legt die Formel von Scratch.A1 auf die Zeichenfolge "Sag ""ahh""" fest, die in Sag "ahh" ausgewertet wird.
  

