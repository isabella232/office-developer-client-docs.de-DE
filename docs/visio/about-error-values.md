---
title: Informationen zu Fehlerwerten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423867"
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
| #DIM!  <br/> | Ein dimensionaler Wert, der den Dimensions Umfang überschreitet (gültige Potenzen \<sind ganze \<Zahlen-128 = n = 127)  <br/> Ein Bemaßungswert, der in einer nicht zulässigen Operation verwendet wurde.  <br/> |1In ^ 100 \* 1In ^ 100 (das Ergebnis ist 1In ^ 200, das sich jenseits des Dimensions befindet)  <br/> 5,2cm^1,5 (ist keine ganzzahlige Potenz)  <br/> |
   

