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
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796352"
---
# <a name="about-error-values"></a>Informationen zu Fehlerwerten

Fehlerwerte werden in Zellen angezeigt, bei denen falsche Formeln für diese Zelle angegeben sind.
  
Wenn eine Formel auf eine Zelle verweist, die einen Fehlerwert enthält, zeigt diese Formel ebenfalls einen Fehlerwert an. Sie können die Funktionen ISERR, ISERRNA, ISTFEHLER oder ISERROR verwenden, um nach Fehlerwerten zu suchen.
  
**Fehlerwerte**

||||
|:-----|:-----|:-----|
|**Wenn die Zelle anzeigt** <br/> |**Die Formel enthält.** <br/> |**Beispiel** <br/> |
| #DIV/0!  <br/> |Division durch 0  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Ein Argument oder Operand vom falschen Typ  <br/> | 5 + "Hütte"  <br/> |
| #REF!  <br/> | Ein Verweis auf eine Zelle, die nicht vorhanden ist  <br/> | Eine Zelle, die in eine andere Zelle verweist, die nicht mehr vorhanden ist  <br/> |
| #NUM!  <br/> | Eine ungültige Zahl  <br/> | Quadratwurzel einer negativen Zahl  <br/> |
| #N/V!  <br/> | Kein verfügbaren Wert  <br/> | Funktion NA)  <br/> |
| #DIM!  <br/> | Ein dimensionaler Wert, der den Bemaßungsbereich überschreitet (gültige Potenzen sind Ganzzahlen-128 \<n = \<= 127)  <br/> Ein dimensionaler Wert, der mit einem Vorgang ungeeignetes verwendet  <br/> |1In ^ 100 \* 1In ^ 100 (das Ergebnis ist 1In ^ 200 und liegt außerhalb des Bemaßungsbereichs)  <br/> 5, 2 cm ^ 1,5 (ist keine ganzzahlige Potenz)  <br/> |
   

