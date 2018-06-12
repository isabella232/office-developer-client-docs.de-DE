---
title: Benutzerdefinierte numerische Formate für die Formatfunktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 97efe972-d873-47d7-be81-8ae3461870c4
description: Hier erfahren Sie, wie Sie die Darstellung einer Zahl durch das Erstellen eines benutzerdefinierten Zahlenformats steuern.
ms.openlocfilehash: fac128ce13edf89105fbee7319533e1a3f346d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790224"
---
# <a name="custom-numeric-formats-for-the-format-function-access-custom-web-app"></a>Benutzerdefinierte numerische Formate für die Formatfunktion (benutzerdefinierte Access-Web-App)

Hier erfahren Sie, wie Sie die Darstellung einer Zahl durch das Erstellen eines benutzerdefinierten Zahlenformats steuern.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 

Sie können die Darstellung einer Zahl ändern, indem Sie ein benutzerdefiniertes Zahlenformat erstellen. Ein benutzerdefiniertes Zahlenformat kann über ein bis drei Teile, die durch ein Semikolon (;) getrennt sind, verfügen. Wenn das Formatargument der [Format-Funktion (Access benutzerdefinierte Web app)](format-function-access-custom-web-app.md)-Funktion eines der vordefinierten numerischen Formate enthält, ist nur ein Teil zulässig. 
  
## <a name="format-specifications"></a>Spezifikationen
<a name="bk_addresources"> </a>

In der folgenden Tabelle sind die Zeichen aufgeführt, die Sie zum Erstellen benutzerdefinierter Zahlenformate verwenden können.
  
|**Formatspezifikationen**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Zeigt die Zahl ohne Formatierung an.  <br/> |
|**0** (Null)  <br/> |Ziffernplatzhalter. Zeigt eine Ziffer oder eine Null an. Wenn im Ausdruck in der Formatzeichenfolge an der Position der Null eine Ziffer steht, wird die Ziffer angezeigt. Andernfalls wird an dieser Position eine Null angezeigt.  <br/> Wenn die Zahl im Formatausdruck weniger Ziffern als Nullen aufweist (auf einer von beiden Seiten des Dezimaltrennzeichens) werden voran- oder nachgestellte Nullen angezeigt. Weist die Zahl rechts neben dem Dezimaltrennzeichen mehr Ziffern als Nullen auf als rechts neben dem Dezimaltrennzeichen im Formatausdruck, wird die Zahl entsprechend der Anzahl an vorhandenen Nullen gerundet. Weist die Zahl links neben dem Dezimaltrennzeichen mehr Ziffern als Nullen auf als links neben dem Dezimaltrennzeichen im Formatausdruck, werden die zusätzlichen Ziffern unverändert angezeigt.  <br/> |
|#  <br/> |Ziffernplatzhalter. Zeigt eine Ziffer oder nichts an. Wenn im Ausdruck in der Formatzeichenfolge an der Position von „#" eine Ziffer steht, wird die Ziffer angezeigt. Andernfalls wird an dieser Position nichts angezeigt.  <br/> Dieses Symbol funktioniert so wie der Ziffernplatzhalter „0", nur dass keine voran- und nachgestellte Nullen angezeigt werden, wenn die Zahl auf einer von beiden Seiten des Dezimaltrennzeichens im Formatausdruck die gleiche oder eine geringere Anzahl an Ziffern als „#"-Zeichen aufweist.  <br/> |
|. (Punkt)  <br/> |Dezimalplatzhalter. Der Dezimalplatzhalter bestimmt, wie viele Ziffern rechts und links neben dem Dezimaltrennzeichen angezeigt werden. Sind im Formatausdruck nur #-Zeichen neben diesem Symbol enthalten, beginnen Zahlen unter 1 mit einem Dezimaltrennzeichen. Um eine vorangestellte Null mit Bruchzahlen anzuzeigen, wird die Null als erster Ziffernplatzhalter links neben dem Dezimaltrennzeichen verwendet. In manchen Gebietsschemas wird ein Komma als Dezimaltrennzeichen verwendet. Das tatsächliche in der formatierten Ausgabe als Dezimaltrennzeichen verwendete Zeichen hängt von dem vom System erkannten Zahlenformat ab. Daher sollten Sie auch dann den Punkt als Dezimaltrennzeichen in den Formaten verwenden, wenn Sie sich in einem Gebietsschema befinden, in dem ein Komma als Dezimaltrennzeichen verwendet wird. Die formatierte Zeichenfolge wird in dem für das Gebietsschema korrekten Format angezeigt.  <br/> |
|%  <br/> |Prozentplatzhalter. Der Ausdruck wird mit 100 multipliziert. Das Prozentzeichen (%) wird an der Position eingefügt, an der es in der Formatzeichenfolge steht.  <br/> |
|, (Komma)  <br/> |Tausendertrennzeichen. Das Tausendertrennzeichen trennt die Tausend von Hundert in einer Zahl, die vier oder mehr Stellen links neben dem Dezimaltrennzeichen aufweist. Der standardmäßige Gebrauch des Tausendertrennzeichens ist gegeben, wenn das Format ein Tausendertrennzeichen aufweist, das von Ziffernplatzhaltern umschlossen ist (0 oder #).  <br/> Ein Tausendertrennzeichen direkt links neben dem Dezimaltrennzeichen (falls eine Dezimalzahl angegeben ist) oder als Zeichen ganz rechts in der Zeichenfolge bedeutet, dass die Zahl durch 1000 dividiert und bei Bedarf entsprechend gerundet wird. Zahlen, die kleiner als 1000, jedoch größer oder gleich 500 sind, werden als 1 angezeigt, und Zahlen, die kleiner als 500 sind, werden als 0 angezeigt. Zwei aufeinanderfolgende Tausendertrennzeichen an dieser Stelle skalieren mit einem Faktor von 1 Million sowie einem weiteren Faktor von 1000 für jedes weitere Trennzeichen.  <br/> Mehrere Trennzeichen an anderer Position als direkt links neben dem Dezimaltrennzeichen oder ganz rechts in der Zeichenfolge werden so behandelt, als ob sie nur die Verwendung des Tausendertrennzeichens angeben würden. In einigen Gebietsschemas wird ein Punkt als Tausendertrennzeichen verwendet. Das tatsächliche in der formatierten Ausgabe als Tausendertrennzeichen verwendete Zeichen hängt von dem von Ihrem System erkannten Zahlenformat ab. Daher sollten auch dann das Komma als Tausendertrennzeichen in den Formaten verwenden, wenn Sie sich in einem Gebietsschema befinden, in dem ein Punkt als Tausendertrennzeichen verwendet wird. Die formatierte Zeichenfolge wird in dem für das Gebietsschema korrekten Format angezeigt.  <br/> Sehen Sie sich zum Beispiel die folgenden drei Formatierungszeichenfolgen an:  <br/> „#,0." verwendet das Tausendertrennzeichen, um die Zahl 100 Millionen als Zeichenfolge „100,000,000" zu formatieren.  <br/> „#0,." verwendet die Skalierung mit einem Faktor von Eintausend, um die Zahl 100 Millionen als Zeichenfolge „100000" zu formatieren.  <br/> „#,0,." verwendet das Tausendertrennzeichen und die Skalierung mit Eintausend, um die Zahl 100 Millionen als Zeichenfolge „100,000" zu formatieren.  <br/> |
|: (Doppelpunkt)  <br/> |Zeittrennzeichen. In manchen Gebietsschemas werden andere Zeichen als Zeittrennzeichen verwendet. Das Zeittrennzeichen trennt Stunden, Minuten und Sekunden bei der Formatierung von Zeitwerten. Das tatsächliche in der formatierten Ausgabe als Zeittrennzeichen verwendete Zeichen wird durch die Systemeinstellungen bestimmt.  <br/> |
|/ (Schrägstrich)  <br/> |Datumstrennzeichen. In manchen Gebietsschemas werden andere Zeichen als Datumstrennzeichen verwendet. Das Datumstrennzeichen trennt Tag, Monat und Jahr bei der Formatierung von Datumswerten. Das tatsächliche in der formatierten Ausgabe als Datumstrennzeichen verwendete Zeichen wird durch die Systemeinstellungen bestimmt.  <br/> |
|**E- , E+ , e- , e+** <br/> |Wissenschaftliches Format. Wenn der Formatausdruck mindestens einen Ziffernplatzhalter (0 oder #) rechts neben „E-", „E+", „e-" oder „e+" aufweist, wird die Zahl im wissenschaftlichen Format angezeigt und zwischen der Zahl und dem Exponenten „E" oder „e" eingefügt. Die Anzahl an Ziffernplatzhaltern auf der linken Seite bestimmt die Anzahl an Ziffern im Exponenten. „E-" oder „e-" fügt ein Minus-Zeichen neben negativen Exponenten ein. „E+" oder „e+" fügt ein Minus-Zeichen neben negativen und ein Plus-Zeichen neben positiven Exponenten ein. Zur richtigen Formatierung müssen Sie außerdem Ziffernplatzhalter rechts neben diesem Symbol einfügen.  <br/> |
|**- + $ ( )** <br/> |Literalzeichen. Diese Zeichen werden genau so angezeigt, wie sie in der Formatierungszeichenfolge eingegeben wurden. Um ein anderes Zeichen als die aufgeführten anzuzeigen, stellen Sie ihm einen umgekehrten Schrägstrich voran (\), oder schließen Sie das Zeichen in doppelte Anführungszeichen ein (" ").  <br/> |
|\ (umgekehrter Schrägstrich)  <br/> |Zeigt das nächste Zeichen in der Formatzeichenfolge an. Um ein Zeichen anzuzeigen, das als Literalzeichen eine besondere Bedeutung hat, wird diesem ein umgekehrter Schrägstrich vorangestellt (\). Der umgekehrte Schrägstrich wird nicht angezeigt. Die Verwendung eines umgekehrten Schrägstrichs entspricht dem Setzen eines Zeichens in doppelte Anführungszeichen. Wenn ein umgekehrter Schrägstrich angezeigt werden soll, muss diesem ein zweiter vorangestellt werden (\\).  <br/> Zeichen, die nicht als Literalzeichen angezeigt werden können, sind die datum- und uhrzeitformatierenden Zeichen (a, c, d, h, m, n, p, q, s, t, w, y, / und :), die zahlenformatierenden Zeichen (#, 0, %, E, e, Komma und Punkt) sowie die zeichenfolgenformatierenden Zeichen (@, &amp;, \<, \> und !).  <br/> |
|"ABC"  <br/> |Zeigt die Zeichenfolge zwischen den doppelten Anführungszeichen an (" "). Um eine Zeichenfolge im Formatargument innerhalb des Codes anzugeben, muss der Text mit Chr(34) umschlossen werden (34 ist der Zeichencode für ein Anführungszeichen (")).  <br/> |
   
Die folgende Tabelle enthält einige Beispiele für Zahlenformatausdrücke. (Bei diesen Beispielen wird davon ausgegangen, dass die Gebietsschemaeinstellung des Systems English-U.S. ist.) Die erste Spalte enthält die Formatierungszeichenfolgen für die Formatfunktion. Die anderen Spalten enthalten die resultierende Ausgabe, wenn die formatierten Daten den in der Spaltenüberschrift angegebenen Wert enthalten.
  
|**Format (Stil)**|**„5" formatiert als**|**„-5" formatiert als**|**„0.5" formatiert als**|**„0" formatiert als**|
|:-----|:-----|:-----|:-----|:-----|
|Zeichnfolge der Länge Null ("")  <br/> |5  <br/> |-5  <br/> |0.5  <br/> |0  <br/> |
|0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|0.00  <br/> |5.00  <br/> |-5.00  <br/> |0.50  <br/> |0.00  <br/> |
|#,##0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|$#,##0;($#,##0)  <br/> |$5  <br/> |($5)  <br/> |$1  <br/> |$0  <br/> |
|$#,##0.00;($#,##0.00)  <br/> |$5.00  <br/> |($5.00)  <br/> |$0.50  <br/> |$0.00  <br/> |
|0%  <br/> |500%  <br/> |-500%  <br/> |50%  <br/> |0%  <br/> |
|0.00%  <br/> |500.00%  <br/> |-500.00%  <br/> |50.00%  <br/> |0.00%  <br/> |
|0.00E+00  <br/> |5.00E+00  <br/> |-5.00E+00  <br/> |5.00E-01  <br/> |0.00E+00  <br/> |
|0.00E-00  <br/> |5.00E00  <br/> |-5.00E00  <br/> |5.00E-01  <br/> |0.00E00  <br/> |
|"$#,##0;;\Z\e\r\o"  <br/> |$5  <br/> |$-5  <br/> |$1  <br/> |Zero  <br/> |
   
## <a name="remarks"></a>Hinweise
<a name="bk_addresources"> </a>

Wenn Sie Semikolons ohne Werte dazwischen einfügen, wird der fehlende Abschnitt mit dem Format des positiven Werts angezeigt.
  
## <a name="see-also"></a>Siehe auch

- [Format-Funktion (Access benutzerdefinierte Web app)](format-function-access-custom-web-app.md) 
- [Benutzerdefinierte Datums- und Uhrzeitformate für die Format-Funktion (benutzerdefinierte Access-Web-App)](custom-date-and-time-formats-for-the-format-function-access-custom-web-app.md)
  

