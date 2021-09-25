---
title: Informationen zu Fehlerwerten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
ms.localizationpriority: medium
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.
ms.openlocfilehash: d2d0f9714e0a25078b765c636d0f3c606d241706
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578305"
---
# <a name="about-error-values"></a>Informationen zu Fehlerwerten

Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.
  
Wenn eine Formel auf eine Zelle verweist, die einen Fehlerwert enthält, zeigt diese Formel ebenfalls einen Fehlerwert an. Sie können die Funktionen ISERR, ISERRNA, ISTFEHLER oder ISERROR verwenden, um nach Fehlerwerten zu suchen.
  
**Fehlerwerte**

||||
|:-----|:-----|:-----|
|**Wenn die Zelle anzeigt** <br/> |**Formel enthält** <br/> |**Beispiel** <br/> |
| #DIV/0!  <br/> |Division durch 0  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Ein Argument oder Operand vom falschen Typ  <br/> | 5 + "Haus"  <br/> |
| #REF!  <br/> | Ein Bezug auf eine nicht vorhandene Zelle  <br/> | Eine Zelle, die auf eine nicht mehr vorhandene Zelle verweist  <br/> |
| #NUM!  <br/> | Eine ungültige Zahl  <br/> | Quadratwurzel einer negativen Zahl  <br/> |
| #N/A!  <br/> | Kein verfügbarer Wert  <br/> | Funktion NA( )  <br/> |
| #DIM!  <br/> | Ein dimensionaler Wert, der den Dimensionsbereich überschreitet (gültige Potenzen sind ganze Zahlen -128 \<= n \<= 127)  <br/> Eindimensionalwert, der bei einem unangemessenen Vorgang verwendet wird.  <br/> |1in^100 \* 1in^100 (das Ergebnis ist 1in^200, was über dem Dimensionsbereich liegt)  <br/> 5,2cm^1,5 (ist keine ganzzahlige Potenz)  <br/> |
   

