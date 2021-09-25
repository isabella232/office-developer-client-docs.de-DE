---
title: SETATREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
ms.localizationpriority: medium
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Leitet aktualisierte Werte, die aus Aktionen in der Benutzeroberfläche oder Automatisierung resultieren, an eine andere Zelle um.
ms.openlocfilehash: 2010cd324d87f9dbcfbfa2c71762ffc94a5484c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559589"
---
# <a name="setatref-function"></a>SETATREF Function

Leitet aktualisierte Werte, die aus Aktionen in der Benutzeroberfläche oder Automatisierung resultieren, an eine andere Zelle um. 
  
## <a name="syntax"></a>Syntax

SETATREF(** *reference* ** [, ** *set_expression* ** [, ** *ignore_eval* ** ]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf die Zelle, in die Aktualisierungen umgeleitet werden.  <br/> |
| _set_expression_ <br/> |Optional  <br/> |**String** <br/> |Ein Ausdruck, der dem  _Verweis_ zugewiesen ist.  <br/> |
| _ignore_eval_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |Wenn TRUE, wird die SETATREF-Funktion als (0) Null ausgewertet; Bei FALSE (Standardeinstellung) wird die SETATREF-Funktion als  _Verweiswert_ ausgewertet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine Benutzeraktion im Zeichnungsfenster oder eine Automatisierungsmethode bewirkt, dass Microsoft Visio eine Zelle aktualisiert, die eine SETATREF-Formel enthält, wird der Wert stattdessen an die Zelle umgeleitet, auf die durch die SETATREF-Formel ( _Verweis_) verwiesen wird. Die Formel in der Zelle mit der SETATREF-Funktion bleibt erhalten.
  
Wenn  _set_expression_ weggelassen wird, wird der in der Benutzeroberfläche oder mithilfe der Automatisierung festgelegte Wert der zelle zugewiesen, auf die verwiesen wird. andernfalls wird der Inhalt von  _set_expression_ der zelle zugewiesen, auf die verwiesen wird. Dadurch kann der neue Wert geändert oder transformiert werden, bevor er der zelle zugewiesen wird, auf die verwiesen wird. 
  
Die SETATREF-Funktion besitzt zwei verwandte Funktionen: 
  
- Die SETATREFEXPR-Funktion, die Sie verwenden können, um den neuen Wert in  _set_expression_ darzustellen. Beispiel: eine  _set_expression_ von SETATREFEXPR()-2 zoll. kann verwendet werden, um das SETATREFEXPR-Ergebnis um 2 Zoll zu subtrahieren. 
    
- Die SETATREFEVAL-Funktion, mit der Sie angeben können, dass ein Teil der  _set_expression_ ausgewertet und durch das Ergebnis ersetzt werden soll. 
    
Die SETATREF-Funktion wurde für die Verwendung in Zellen entwickelt, die durch Benutzeraktionen im Zeichnungsfenster geändert werden können. Folgende Zellen werden unterstützt:
  
- Abschnitt ShapeTransform - Zelle Width, Height, Angle, PinX und PinY
    
- Abschnitt Text Transform - Zelle TxtWidth, TxtHeight, TxtAngle, TxtPinX und TxtPinY
    
- Abschnitt 1-D Endpoints - Zelle BeginX, BeginY, EndX und EndY
    
- Abschnitt Controls - Zelle Controls.X und Controls.Y
    
- Abschnitt Shape Data
    
Da SETATREF den Speicherort von Zellwertänderungen ändert, wird das Auslösen von Ereignissen beeinflusst. Wenn eine Zelle SETATREF enthält, werden das **FormulaChanged**-Ereignis und das **CellChanged**-Ereignis für die von SETATREF referenzierte Zelle ausgelöst. Wenn eine Zelle, die SETATREF enthält, auch SETATREFEXPR enthält, wird das **FormulaChanged-Ereignis** auch für die Zelle ausgelöst, die SETATREF enthält, da ein Funktionsparameter geändert wird. 
  
Beachten Sie folgende weiteren wichtigen Hinweise zur SETATREF-Funktion:
  
- SETATREF-Funktionen können bis zu 10 Referenzen auf andere SETATREF-Funktionen verketten. 
    
- Zellen können zusätzlich zur SETATREF-Funktion andere Ausdrücke enthalten, einschließlich mehrerer Vorkommen von SETATREF in einer einzigen Zelle.
    
- Wenn Shapes verbunden werden, folgt Visio der SETATREF-Referenzkette innerhalb desselben Blatts und platziert Klebeformeln in der referenzierten Zelle. 
    
- Die Automatisierung erkennt die SETATREF-Funktion und folgt der Kette referenzierter Zellen. 
    
- Ebenso wie GUARD schützt SETATREF die Zellen nicht vor Änderungen, die über die SETF-Funktion im ShapeSheet-Fenster vorgenommen wurden.
    
## <a name="example1"></a>Beispiel1

Angenommen, ein Shape besitzt die benutzerdefinierte Eigenschaft Breite und die Zelle Width im Abschnitt Shape Transform enthält folgende Formel:
  
=SETATREF(Prop.Width)
  
Wenn ein Benutzer die Breite des Shapes in der Benutzeroberfläche ändern sollte, wird der neue Wert der Zelle Prop.Width zugewiesen, nicht der Zelle Width im Abschnitt ShapeTransform. Die Formel in der Zelle Width bleibt unverändert. Sie können die Breite des Shapes auch mithilfe von Shape-Daten festlegen.
  
## <a name="example2"></a>Beispiel2

Visio-Lösungen enthalten oft Shapes mit hierarchischen Beziehungen, bei denen untergeordnete Shapes verschoben werden müssen, wenn ein übergeordnetes Shape verschoben wird. Im folgenden Beispiel wird beschrieben, wie Sie diese Beziehung mithilfe der SETATREF-Funktion im ShapeSheet-Fenster verwalten können. 
  
Folgende Formeln sind im Abschnitt Shape Transform des untergeordneten Shapes enthalten. Außerdem werden die benutzerdefinierten Zellen User.DeltaX und User.DeltaY definiert, die den Abstand von ParentShape verfolgen. Auf diese Weise kann das untergeordnete Shape verschoben werden, wenn das übergeordnete Shape verschoben wird, und die hierarchische Beziehung bleibt erhalten.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Wenn das untergeordnete Shape mithilfe der Benutzeroberfläche verschoben wird, werden die neuen PinX- und PinY-Werte als Parameter in der SETATREFEXPR-Funktion festgelegt. Die SETATREF-Funktion wertet die in SETATREFEVAL eingeschlossene Formel aus und ersetzt PinX und PinY durch ihre Ergebnisse. Anschließend wird die resultierende Formel den Benutzerzellen zugewiesen, auf die in der SETATREF-Funktion verwiesen wird: User.DeltaX und User.DeltaY. Schließlich werden die von SETATREF (User.DeltaX oder User.DeltaY) zurückgegebenen Werte der Pinposition von ParentShape hinzugefügt, um die Position des untergeordneten Shapes zu berechnen.
  

