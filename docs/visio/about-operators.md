---
title: Informationen zu Operatoren
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251824
localization_priority: Normal
ms.assetid: 43128ea2-c0d9-c45f-31e6-768a80ae59b2
description: Sie können Operatoren in Formeln verwenden, um arithmetische Operationen (Addition, Subtraktion, Multiplikation usw.) oder logische Vergleiche (größer als, kleiner als, gleich usw.) auszuführen. Sie können darüber hinaus die Reihenfolge der Berechnungsschritte in einer Formel bestimmen, indem Sie Ausdrücke in Klammern einschließen. Verwenden Sie den &-Operator, um Zeichenfolgen zu kombinieren bzw. miteinander zu verketten.
ms.openlocfilehash: 3a14993ab317d19d0e4a8983e4714f587c235d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796362"
---
# <a name="about-operators"></a>Informationen zu Operatoren

Sie können Operatoren in Formeln verwenden, um arithmetische Operationen (Addition, Subtraktion, Multiplikation usw.) oder logische Vergleiche (größer als, kleiner als, gleich usw.) auszuführen. Sie können darüber hinaus die Reihenfolge der Berechnungsschritte in einer Formel bestimmen, indem Sie Ausdrücke in Klammern einschließen. Verwenden Sie den &-Operator, um Zeichenfolgen zu kombinieren bzw. miteinander zu verketten.
  
Microsoft Visio versucht automatisch, Datentypen umzuwandeln, wenn eine Operation oder Funktion einen spezifischen Datentyp erfordert. Der Multiplikationsoperator erfordert beispielsweise numerische Argumente, und der &-Operator (Zeichenfolgenverkettung) erfordert Zeichenfolgenargumente. Wenn das Argument nicht in den erforderlichen Datentyp konvertiert werden kann, wird ein Standardwert bereitgestellt. Der Standardwert ist das eingegebene Äquivalent von Nichts: Null für Zahlen, FALSE für Boolesche Werte, "" für Zeichenfolgen usw.
  
Die folgende Tabelle enthält Beispiele für Ausdrücke und deren Ergebnisse.
  
|**Expression**|**Ergebnis**|**Beschreibung**|
|:-----|:-----|:-----|
| 2 \* 5 &amp; "Cent"  <br/> | "10 Cent"  <br/> | Die &amp; -Operator (zeichenfolgenverkettung) erfordert Zeichenfolgenargumente, sodass das numerische Ergebnis von 2 \* 5 wird automatisch in die Zeichenfolge "10" konvertiert.  <br/> |
| 5 \* "2"  <br/> | 10  <br/> | Die \* -Operator (Multiplikation) erfordert numerische Argumente, daher wird die Zeichenfolge "2" automatisch in die äquivalente Zahl 2 konvertiert.  <br/> |
| 5 \* "Schafe"  <br/> | 0  <br/> | Die \* -Operator (Multiplikation) erfordert numerische Argumente, sodass 0 (null), da die Zeichenfolge "Schafe" in eine Zahl konvertiert werden kann, wie die numerische Entsprechung verwendet wird.  <br/> |
   
## <a name="arithmetic-operators"></a>Arithmetische Operatoren

Arithmetische Operatoren führen Vorgänge mit Zahlen aus. Der +-Operator (Plus) und der --Operator (Minus) können allein als unäre Operatoren verwendet werden, um das Vorzeichen einer Zahl anzugeben. Der %-Operator (Prozent) ist ebenfalls ein unärer Operator, der eine Zahl als Prozentsatz bestimmt.
  
|**Operator**|**Aktion**|**Beispiel**|**Ergebnis**|
|:-----|:-----|:-----|:-----|
| +  <br/> | Unärer Plus-Operator  <br/> | +37  <br/> | 37  <br/> |
| -  <br/> | Unärer Minus-Operator  <br/> | -37  <br/> | -37  <br/> |
| %  <br/> | Einstelliger Prozentsatz  <br/> | 37 %  <br/> | .37  <br/> |
| ^  <br/> | Potenzierung  <br/> | 5 ^ 2  <br/> | 25  <br/> |
| \*  <br/> | Multiplikation  <br/> | 5 \* 2  <br/> | 10  <br/> |
| /  <br/> | Division  <br/> | 5 / 2  <br/> | 2,5  <br/> |
| +  <br/> | Addition  <br/> | 5 +2  <br/> | 7  <br/> |
| -  <br/> | Subtraktion  <br/> | 5 - 2  <br/> | 3  <br/> |
   
## <a name="comparison-operators"></a>Vergleichsoperatoren

Vergleichsoperatoren werden verwendet, um logische Ausdrücke zu erstellen. Ein logischer Ausdruck wird entweder als TRUE oder FALSE ausgewertet.
  
|**Operator**|**Alternative**|**Aktion**|**Beispiel**|**Ergebnis**|
|:-----|:-----|:-----|:-----|:-----|
| \>  <br/> | _GT_  <br/> | Größer als  <br/> | 5 \> 2  <br/> | TRUE  <br/> |
| \<  <br/> | _LT_  <br/> | Kleiner als  <br/> | 5 \< 2  <br/> | FALSE  <br/> |
| \>=  <br/> | _GE_  <br/> | Größer als oder gleich  <br/> | 5 \>= 2  <br/> | TRUE  <br/> |
| \<=  <br/> | _LE_  <br/> | Kleiner als oder gleich  <br/> | 5 \<= 2  <br/> | FALSE  <br/> |
| =  <br/> | _EQ_  <br/> | Gleich  <br/> | 5 = 2  <br/> | FALSE  <br/> |
| \<\>  <br/> | _NE_  <br/> | Nicht gleich  <br/> | 5 \< \> 2  <br/> | TRUE  <br/> |
   
Symbolische Vergleichsoperatoren (\>, \<usw.) für die meisten Vergleiche am besten geeignet sind. Die anderen Operatoren (_GT_, _LT_usw.) führen Sie einen exakten Vergleich mit 15 Dezimalstellen Genauigkeitsverlust Visio verwendet, um Werte intern zu speichern.
  
Wenn Sie gerundete oder berechnete Werte mithilfe der anderen Operatoren vergleichen, wird möglicherweise FALSE zurückgegeben, obwohl aus praktischen Gründen eigentlich TRUE zurückgegeben werden sollte.
  
Wenn Sie Vergleichsoperatoren zum Vergleichen von Textzeichenfolgen verwenden, werden die Zeichenfolgen zuerst in numerische Werte konvertiert. Textzeichenfolgen, die nicht konvertiert werden können, geben den Wert 0 zurück. Aus diesem Grund variieren Vergleiche und führen möglicherweise nicht zu den erwarteten Ergebnissen. Verwenden Sie die Funktion STRSAME oder STRSAMEEX, wenn Sie einen Standard-Zeichenfolgenvergleich durchführen möchten.
  
## <a name="order-of-evaluation"></a>Reihenfolge der Auswertung

Wenn eine Formel mehrere Ausdrücke enthält, werden die Ausdrücke in der Reihenfolge berechnet, die der derzeit ausgeführten Operation entspricht. In dieser Tabelle ist die Reihenfolge aufgeführt, in der die Operatoren in Visio berechnet werden.
  
|**Order**|**Aktion**|**Operator**|
|:-----|:-----|:-----|
|Erster  <br/> |Positiv  <br/> |+ (einstellig)  <br/> |
||Negativ  <br/> |- (einstellig)  <br/> |
||Prozent  <br/> |% (einstellig)  <br/> |
|Zweiter  <br/> |Potenzierung  <br/> |^  <br/> |
|Dritter  <br/> |Multiplikation  <br/> |\*  <br/> |
||Abteilung  <br/> |/  <br/> |
|Vierter  <br/> |Ergänzungen  <br/> |+  <br/> |
||Subtraktion  <br/> |-  <br/> |
|Fünfter  <br/> |Zeichenfolgenverknüpfung  <br/> |&amp;  <br/> |
|Sechster  <br/> |Größer als  <br/> |\>oder GT  <br/> |
||Größer als oder gleich  <br/> |\>= oder GE  <br/> |
||Kleiner als  <br/> |\<oder LT  <br/> |
||Kleiner als oder gleich  <br/> |\<= oder LE  <br/> |
|Siebenter  <br/> |Gleich  <br/> |= oder EQ  <br/> |
||Nicht gleich  <br/> |\<\>oder NE  <br/> |
   
Sie können die Reihenfolge der Berechnung in einer Formel ändern, indem Sie Ausdrücke in Klammern einschließen. Visio berechnet Ausdrücke in Klammern zuerst, und zwar von links nach rechts. Beispiel:
  
4 + 5 \* 6 = 4 + 30 = 34
  
(4 + 5) \* 6 = 9 \* 6 = 54
  
Wenn Ausdrücke in Klammern geschachtelt sind, wird der Ausdruck im innersten Satz Klammern zuerst berechnet.
  
## <a name="ampersand-operator"></a>Kaufmännisches und-Zeichen

Der &-Operator gibt eine neue Zeichenfolge zurück. Mithilfe dieses Zeichens können Sie Komposita und Phrasen erstellen. Verwenden Sie die folgende Syntax:
  
"Zeichenfolge1" &amp; "Zeichenfolge2"
  
 **Beispiel**
  
"Dog" &amp; "Hütte" ergibt "Hundehütte"
  

