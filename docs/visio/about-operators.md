---
title: Informationen zu Operatoren
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251824
ms.localizationpriority: medium
ms.assetid: 43128ea2-c0d9-c45f-31e6-768a80ae59b2
description: Sie können Operatoren in Formeln verwenden, um arithmetische Operationen (Addition, Subtraktion, Multiplikation usw.) oder logische Vergleiche (größer als, kleiner als, gleich usw.) auszuführen. Sie können darüber hinaus die Reihenfolge der Berechnungsschritte in einer Formel bestimmen, indem Sie Ausdrücke in Klammern einschließen. Verwenden Sie den &-Operator, um Zeichenfolgen zu kombinieren bzw. miteinander zu verketten.
ms.openlocfilehash: 81829e04445652ce45b3b1ff92339b2090c2fcb9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619176"
---
# <a name="about-operators"></a>Informationen zu Operatoren

Sie können Operatoren in Formeln verwenden, um arithmetische Operationen (Addition, Subtraktion, Multiplikation usw.) oder logische Vergleiche (größer als, kleiner als, gleich usw.) auszuführen. Sie können darüber hinaus die Reihenfolge der Berechnungsschritte in einer Formel bestimmen, indem Sie Ausdrücke in Klammern einschließen. Verwenden Sie den &-Operator, um Zeichenfolgen zu kombinieren bzw. miteinander zu verketten.
  
Microsoft Visio versucht automatisch, Datentypen umzuwandeln, wenn eine Operation oder Funktion einen spezifischen Datentyp erfordert. Der Multiplikationsoperator erfordert beispielsweise numerische Argumente, und der &-Operator (Zeichenfolgenverkettung) erfordert Zeichenfolgenargumente. Wenn das Argument nicht in den erforderlichen Datentyp konvertiert werden kann, wird ein Standardwert bereitgestellt. Der Standardwert ist das eingegebene Äquivalent von Nichts: Null für Zahlen, FALSE für Boolesche Werte, "" für Zeichenfolgen usw.
  
Die folgende Tabelle enthält Beispiele für Ausdrücke und deren Ergebnisse.
  
|**Ausdruck**|**Ergebnis**|**Beschreibung**|
|:-----|:-----|:-----|
| 2 \* 5 &amp; Cent  <br/> | "10 Cent"  <br/> | Der &amp; Operator (Zeichenfolgenverkettung) erfordert Zeichenfolgenargumente, sodass das numerische Ergebnis von \* 2 5 automatisch in die Zeichenfolge "10" konvertiert wird.  <br/> |
| 5 \* "2"  <br/> | 10  <br/> | Der \* Operator (Multiplikation) erfordert numerische Argumente, sodass die Zeichenfolge "2" automatisch in die entsprechende Zahl 2 konvertiert wird.  <br/> |
| 5 \* "vererzt"  <br/> | 0  <br/> | Für \* den Operator (Multiplikation) sind numerische Argumente erforderlich. Da die Zeichenfolge "Zierzeichen" nicht in eine Zahl konvertiert werden kann, wird null als numerische Entsprechung verwendet.  <br/> |
   
## <a name="arithmetic-operators"></a>Arithmetische Operatoren

Arithmetische Operatoren führen Vorgänge mit Zahlen aus. Der +-Operator (Plus) und der --Operator (Minus) können allein als unäre Operatoren verwendet werden, um das Vorzeichen einer Zahl anzugeben. Der %-Operator (Prozent) ist ebenfalls ein unärer Operator, der eine Zahl als Prozentsatz bestimmt.
  
|**Operator**|**Aktion**|**Beispiel**|**Ergebnis**|
|:-----|:-----|:-----|:-----|
| +  <br/> | Unärer Plus-Operator  <br/> | +37  <br/> | 37  <br/> |
| -  <br/> | Unärer Minus-Operator  <br/> | -37  <br/> | -37  <br/> |
| %  <br/> | Einstelliger Prozentsatz  <br/> | 37 %  <br/> | .37  <br/> |
| ^  <br/> | Potenzierung  <br/> | 5 ^ 2  <br/> | 25  <br/> |
| \*  <br/> | Multiplikation  <br/> | 5 \* 2  <br/> | 10  <br/> |
| /  <br/> | Division  <br/> | 5/2  <br/> | 2,5  <br/> |
| +  <br/> | Ergänzungen  <br/> | 5 +2  <br/> | 7   <br/> |
| -  <br/> | Subtraktion  <br/> | 5 -2  <br/> | 3  <br/> |
   
## <a name="comparison-operators"></a>Vergleichsoperatoren

Vergleichsoperatoren werden verwendet, um logische Ausdrücke zu erstellen. Ein logischer Ausdruck wird entweder als TRUE oder FALSE ausgewertet.
  
|**Operator**|**Alternative**|**Aktion**|**Beispiel**|**Ergebnis**|
|:-----|:-----|:-----|:-----|:-----|
| \>  <br/> | _GT_  <br/> | Größer als  <br/> | 5 \> 2  <br/> | TRUE  <br/> |
| \<  <br/> | _LT_  <br/> | Kleiner als  <br/> | 5 \< 2  <br/> | FALSE  <br/> |
| \>=  <br/> | _GE_  <br/> | Größer oder gleich  <br/> | 5 \> = 2  <br/> | TRUE  <br/> |
| \<=  <br/> | _LE_  <br/> | Kleiner als oder gleich  <br/> | 5 \<= 2  <br/> | FALSE  <br/> |
| =  <br/> | _EQ_  <br/> | Gleich  <br/> | 5 = 2  <br/> | FALSE  <br/> |
| \<\>  <br/> | _NE_  <br/> | Nicht gleich  <br/> | 5 \<\> 2  <br/> | TRUE  <br/> |
   
Die symbolischen \> Vergleichsoperatoren ( \< usw.) sind die beste Wahl für die meisten Vergleiche. Die alternativen Operatoren (_GT_, _LT_ usw.) führen einen genauen Vergleich mit den vollständigen 15 Genauigkeitsziffern durch, die Visio zum internen Speichern von Werten verwendet.
  
Wenn Sie gerundete oder berechnete Werte mithilfe der anderen Operatoren vergleichen, wird möglicherweise FALSE zurückgegeben, obwohl aus praktischen Gründen eigentlich TRUE zurückgegeben werden sollte.
  
Wenn Sie Vergleichsoperatoren zum Vergleichen von Textzeichenfolgen verwenden, werden die Zeichenfolgen zuerst in numerische Werte konvertiert. Textzeichenfolgen, die nicht konvertiert werden können, geben den Wert 0 zurück. Aus diesem Grund variieren Vergleiche und führen möglicherweise nicht zu den erwarteten Ergebnissen. Verwenden Sie die Funktion STRSAME oder STRSAMEEX, wenn Sie einen Standard-Zeichenfolgenvergleich durchführen möchten.
  
## <a name="order-of-evaluation"></a>Reihenfolge der Auswertung

Wenn eine Formel mehrere Ausdrücke enthält, werden die Ausdrücke in der Reihenfolge berechnet, die der derzeit ausgeführten Operation entspricht. In dieser Tabelle ist die Reihenfolge aufgeführt, in der die Operatoren in Visio berechnet werden.
  
|**Order**|**Aktion**|**Operator**|
|:-----|:-----|:-----|
|Erster  <br/> |Positive  <br/> |+ (einstellig)  <br/> |
||Negativ  <br/> |- (einstellig)  <br/> |
||Prozent  <br/> |% (einstellig)  <br/> |
|Zweiter  <br/> |Potenzierung  <br/> |^  <br/> |
|Dritter  <br/> |Multiplikation  <br/> |\*  <br/> |
||Division  <br/> |/  <br/> |
|Vier  <br/> |Ergänzungen  <br/> |+  <br/> |
||Subtraktion  <br/> |-  <br/> |
|Fünfte  <br/> |Zeichenfolgenverknüpfung  <br/> |&amp;  <br/> |
|Sechsten  <br/> |Größer als  <br/> |\> oder GT  <br/> |
||Größer oder gleich  <br/> |\>= oder GE  <br/> |
||Kleiner als  <br/> |\< or LT  <br/> |
||Kleiner als oder gleich  <br/> |\<= or LE  <br/> |
|Siebte  <br/> |Equal  <br/> |= oder EQ  <br/> |
||Nicht gleich  <br/> |\<\> oder NE  <br/> |
   
Sie können die Reihenfolge der Berechnung in einer Formel ändern, indem Sie Ausdrücke in Klammern einschließen. Visio berechnet Ausdrücke in Klammern zuerst, und zwar von links nach rechts. Beispiel:
  
4 + 5 \* 6 = 4 + 30 = 34
  
(4 + 5) \* 6 = 9 \* 6 = 54
  
Wenn Ausdrücke in Klammern geschachtelt sind, wird der Ausdruck im innersten Satz Klammern zuerst berechnet.
  
## <a name="ampersand-operator"></a>&-Operator

Der &-Operator gibt eine neue Zeichenfolge zurück. Mithilfe dieses Zeichens können Sie Komposita und Phrasen erstellen. Verwenden Sie die folgende Syntax:
  
"string1" &amp; "string2"
  
 **Beispiel**
  
"Dog" &amp; "house" gibt "doghouse" zurück
  

