---
title: SETATREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Leitet aktualisierte Werte, die Aktionen in der Benutzeroberfläche (UI) oder die Automatisierung in eine andere Zelle entsteht.
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797994"
---
# <a name="setatref-function"></a>SETATREF Function

Leitet aktualisierte Werte, die Aktionen in der Benutzeroberfläche (UI) oder die Automatisierung in eine andere Zelle entsteht. 
  
## <a name="syntax"></a>Syntax

SETATREF (** *Verweis* ** [, ** *Set_expression* ** [, ** *Ignore_eval* **]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Referenz (engl.)_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf die Zelle, in die Aktualisierungen umgeleitet werden.  <br/> |
| _set_expression_ <br/> |Optional  <br/> |**String** <br/> |Ein Ausdruck, der _Reference_zugewiesen ist.  <br/> |
| _ignore_eval_ <br/> |Optional  <br/> |**Boolean** <br/> |Wenn "true" ergibt die SETATREF-Funktion (0) 0 (null); ist der Wert FALSE ergibt (Standardeinstellung) die SETATREF-Funktion den Wert des _Verweises_.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn eine Benutzeraktion im Zeichnungsfenster oder eine Automatisierungsmethode bewirkt, Microsoft Visio dass, eine Zelle mit einer SETATREF-Formel zu aktualisieren, wird der Wert stattdessen auf die Zelle, die durch die SETATREF-Formel ( _Referenz_) umgeleitet. Die Formel in die Zelle mit der SETATREF-Funktion bleibt intakt.
  
Wenn _Set_expression_ ausgelassen wird, wird der Wert festgelegt, in der Benutzeroberfläche oder mithilfe der Automatisierung der referenzierten Zelle zugewiesen. Andernfalls werden der Inhalt von _Set_expression_ der referenzierten Zelle zugewiesen. Dadurch wird den neuen Wert geändert oder transformiert werden, bevor der referenzierten Zelle zugewiesen wird. 
  
Die SETATREF-Funktion besitzt zwei verwandte Funktionen: 
  
- Die SETATREFEXPR-Funktion, die Sie verwenden können, den neuen Wert innerhalb von _Set_expression_dargestellt. Beispielsweise _Set_expression_ () SETATREFEXPR-2 in. kann verwendet werden, 2 Zoll vom SETATREFEXPR-Ergebnis subtrahiert werden soll. 
    
- Die SETATREFEVAL-Funktion, die Sie verwenden können, um anzugeben, dass ein Teil von _Set_expression_ ausgewertet und durch das Ergebnis ersetzt werden soll. 
    
Die SETATREF-Funktion dient zur Verwendung in Zellen, die durch Benutzeraktionen im Zeichnungsfenster geändert werden können. Folgenden Zellen werden unterstützt:
  
- Abschnitt ShapeTransform - Zelle Width, Height, Angle, PinX und PinY
    
- Abschnitt Text Transform - Zelle TxtWidth, TxtHeight, TxtAngle, TxtPinX und TxtPinY
    
- Abschnitt 1-D Endpoints - Zelle BeginX, BeginY, EndX und EndY
    
- Abschnitt Controls - Zelle Controls.X und Controls.Y
    
- Abschnitt Shape Data
    
Da SETATREF den Speicherort geändert wird, in dem-Werte Zelle ändern, wirkt sich dies auf das Auslösen von Ereignissen. Wenn eine Zelle SETATREF enthält, ausgelöst, die **FormulaChanged** und **CellChanged** -Ereignisse für die Zelle, die von SETATREF Zelle SETATREF verwiesen wird. Wenn eine Zelle mit SETATREF auch SETATREFEXPR enthält, wird das **FormulaChanged** -Ereignis auch für die Zelle mit SETATREF ausgelöst, da ein Parameter-Funktion geändert wird. 
  
Beachten Sie folgende weiteren wichtigen Hinweise zur SETATREF-Funktion:
  
- SETATREF-Funktionen können bis zu 10 Referenzen auf andere SETATREF-Funktionen verketten. 
    
- Zellen können zusätzlich zur SETATREF-Funktion andere Ausdrücke enthalten, einschließlich mehrerer Vorkommen von SETATREF in einer einzigen Zelle.
    
- Wenn Shapes verbunden werden, folgt Visio der SETATREF-Referenzkette innerhalb desselben Blatts und platziert Klebeformeln in der referenzierten Zelle. 
    
- Die Automatisierung erkennt die SETATREF-Funktion und folgt der Kette referenzierter Zellen. 
    
- Ebenso wie GUARD schützt SETATREF die Zellen nicht vor Änderungen, die über die SETF-Funktion im ShapeSheet-Fenster vorgenommen wurden.
    
## <a name="example1"></a>Beispiel 1

Angenommen, ein Shape besitzt die benutzerdefinierte Eigenschaft Breite und die Zelle Width im Abschnitt Shape Transform enthält folgende Formel:
  
=SETATREF(Prop.Width)
  
Wenn ein Benutzer die Breite des Shapes in der Benutzeroberfläche ändern, wird der neue Wert der Zelle Prop.Width nicht auf die Zelle Width im Abschnitt ShapeTransform-Zelle zugewiesen. die Formel in die Zelle Width bleibt unverändert. Sie können auch die Breite des Shapes mithilfe von Shape-Daten festlegen.
  
## <a name="example2"></a>Beispiel 2

Visio-Lösungen enthalten oft Shapes mit hierarchischen Beziehungen, bei denen untergeordnete Shapes verschoben werden müssen, wenn ein übergeordnetes Shape verschoben wird. Im folgenden Beispiel wird beschrieben, wie Sie diese Beziehung mithilfe der SETATREF-Funktion im ShapeSheet-Fenster verwalten können. 
  
Folgende Formeln sind im Abschnitt Shape Transform des untergeordneten Shapes enthalten. Außerdem werden die benutzerdefinierten Zellen User.DeltaX und User.DeltaY definiert, die den Abstand von ParentShape verfolgen. Auf diese Weise kann das untergeordnete Shape verschoben werden, wenn das übergeordnete Shape verschoben wird, und die hierarchische Beziehung bleibt erhalten.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Wenn das untergeordnete Shape mithilfe der Benutzeroberfläche verschoben wird, werden die neuen Werte für DrehbezX und DrehbezY als Parameter der SETATREFEXPR-Funktion festgelegt. Die SETATREF-Funktion wertet die Formel in SETATREFEVAL eingeschlossen und ersetzt Sie durch ihre Ergebnisse DrehbezX und DrehbezY, und klicken Sie dann die Benutzerzellen verwiesen wird, in der enthaltene und User.DeltaY definiert die resultierende Formel zugewiesen ist. Schließlich werden die von SETATREF (User.DeltaX oder User.DeltaY definiert) zurückgegebenen Werte den Pin-Speicherort des ParentShape zum Berechnen des untergeordneten Shapes Pin Speicherort hinzugefügt.
  

