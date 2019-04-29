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
description: Leitet aktualisierte Werte aus Aktionen auf der Benutzeroberfläche oder Automatisierung in eine andere Zelle um.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416804"
---
# <a name="setatref-function"></a>SETATREF Function

Leitet aktualisierte Werte aus Aktionen auf der Benutzeroberfläche oder Automatisierung in eine andere Zelle um. 
  
## <a name="syntax"></a>Syntax

SETATREF (* * *Reference* * * [, * * *set_expression* * * [, * * *ignore_eval* * *]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf die Zelle, in die Aktualisierungen umgeleitet werden.  <br/> |
| _set_expression_ <br/> |Optional  <br/> |**String** <br/> |Ein Ausdruck, der _Reference_zugeordnet ist.  <br/> |
| _ignore_eval_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |Wenn der Wert TRUE ist, wird die SETATREF-Funktion zu (0) NULL ausgewertet. Wenn FALSE (Standardeinstellung), wird die SETATREF-Funktion als Wert von _Reference_ausgewertet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn eine Benutzeraktion im Zeichnungsfenster oder eine Automatisierungsmethode Microsoft Visio veranlasst, eine Zelle zu aktualisieren, die eine SETATREF-Formel enthält, wird der Wert stattdessen an die Zelle umgeleitet, auf die von der SETATREF-Formel ( _Reference_) verwiesen wird. Die Formel in der Zelle mit der SETATREF-Funktion bleibt erhalten.
  
Wenn _set_expression_ ausgelassen wird, wird der auf der Benutzeroberfläche oder mithilfe der Automatisierung festgelegte Wert der referenzierten Zelle zugewiesen; Andernfalls wird der Inhalt von _set_expression_ der referenzierten Zelle zugewiesen. Dadurch kann der neue Wert geändert oder transformiert werden, bevor er der referenzierten Zelle zugewiesen wird. 
  
Die SETATREF-Funktion besitzt zwei verwandte Funktionen: 
  
- Die SETATREFEXPR-Funktion, die Sie verwenden können, um den neuen Wert in _set_expression_darzustellen. Beispiel: ein _set_expression_ von SETATREFEXPR ()-2 in. kann verwendet werden, um 2 Zoll vom SETATREFEXPR-Ergebnis zu subtrahieren. 
    
- Die SETATREFEVAL-Funktion, die Sie verwenden können, um anzugeben, dass ein Teil von _set_expression_ ausgewertet und durch das Ergebnis ersetzt werden soll. 
    
Die SETATREF-Funktion ist für die Verwendung in Zellen vorgesehen, die von Benutzeraktionen im Zeichnungsfenster geändert werden können. Folgende Zellen werden unterstützt:
  
- Abschnitt ShapeTransform - Zelle Width, Height, Angle, PinX und PinY
    
- Abschnitt Text Transform - Zelle TxtWidth, TxtHeight, TxtAngle, TxtPinX und TxtPinY
    
- Abschnitt 1-D Endpoints - Zelle BeginX, BeginY, EndX und EndY
    
- Abschnitt Controls - Zelle Controls.X und Controls.Y
    
- Abschnitt Shape Data
    
Da SETATREF den Speicherort von Zellwertänderungen ändert, wird das Auslösen von Ereignissen beeinflusst. Wenn eine Zelle SETATREF enthält, werden das **FormulaChanged**-Ereignis und das **CellChanged**-Ereignis für die von SETATREF referenzierte Zelle ausgelöst. Wenn eine Zelle mit SETATREF auch SETATREFEXPR, wird das **Formula** -Ereignis auch für die Zelle ausgelöst, die SETATREF enthält, da ein Funktionsparameter geändert wird. 
  
Beachten Sie folgende weiteren wichtigen Hinweise zur SETATREF-Funktion:
  
- SETATREF-Funktionen können bis zu 10 Referenzen auf andere SETATREF-Funktionen verketten. 
    
- Zellen können zusätzlich zur SETATREF-Funktion andere Ausdrücke enthalten, einschließlich mehrerer Vorkommen von SETATREF in einer einzigen Zelle.
    
- Wenn Shapes verbunden werden, folgt Visio der SETATREF-Referenzkette innerhalb desselben Blatts und platziert Klebeformeln in der referenzierten Zelle. 
    
- Die Automatisierung erkennt die SETATREF-Funktion und folgt der Kette referenzierter Zellen. 
    
- Ebenso wie GUARD schützt SETATREF die Zellen nicht vor Änderungen, die über die SETF-Funktion im ShapeSheet-Fenster vorgenommen wurden.
    
## <a name="example1"></a>Beispiel1

Angenommen, ein Shape besitzt die benutzerdefinierte Eigenschaft Breite und die Zelle Width im Abschnitt Shape Transform enthält folgende Formel:
  
= SETATREF (Prop. Width)
  
Wenn ein Benutzer die Breite der Form in der Benutzeroberfläche ändern würde, wird der neue Wert der Zelle Prop. Width und nicht der Zelle "width" im Abschnitt ShapeTransform zugewiesen. die Formel in der Zelle "width" bleibt unverändert. Sie können die Breite der Form auch mithilfe von Shape-Daten festlegen.
  
## <a name="example2"></a>Example2

Visio-Lösungen enthalten oft Shapes mit hierarchischen Beziehungen, bei denen untergeordnete Shapes verschoben werden müssen, wenn ein übergeordnetes Shape verschoben wird. Im folgenden Beispiel wird beschrieben, wie Sie diese Beziehung mithilfe der SETATREF-Funktion im ShapeSheet-Fenster verwalten können. 
  
Folgende Formeln sind im Abschnitt Shape Transform des untergeordneten Shapes enthalten. Außerdem werden die benutzerdefinierten Zellen User.DeltaX und User.DeltaY definiert, die den Abstand von ParentShape verfolgen. Auf diese Weise kann das untergeordnete Shape verschoben werden, wenn das übergeordnete Shape verschoben wird, und die hierarchische Beziehung bleibt erhalten.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Wenn das untergeordnete Shape mithilfe der Benutzeroberfläche verschoben wird, werden die neuen PinX-und PinY-Werte als Parameter in der SETATREFEXPR-Funktion festgelegt. Die SETATREF-Funktion wertet die in SETATREFEVAL eingeschlossene Formel aus und ersetzt PinX und PinY durch ihre Ergebnisse, und dann wird die resultierende Formel den Benutzer Zellen zugewiesen, auf die in der SETATREF-Funktion – User. DeltaX und User. DeltaY verwiesen wird. Schließlich werden die von SETATREF zurückgegebenen Werte (User. DeltaX oder User. DeltaY) zur PIN-Position von ParentShape hinzugefügt, um die PIN-Position des untergeordneten Shapes zu berechnen.
  

