---
title: Excel-Arbeitsblatt und die Auswertung von Ausdrücken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Auswertung von Ausdrücken [excel 2007], Fehler in Arbeitsblättern [Excel 2007], lange Unicode-Zeichenfolgen [Excel 2007], Auswerten von Ausdrücken [Excel 2007], Auswerten von Arbeitsblättern [Excel 2007], Arbeitsblatt Evaluierungshandbuch und exemplarische Vorgehensweisen [Excel 2007], Arbeitsblattfehler [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 543ff7fcbc88253dafd7fc6e7000bf9657d8c258
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790477"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Excel-Arbeitsblatt und die Auswertung von Ausdrücken

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel-Arbeitsblatt Zelleninhalt werden in eine der vier grundlegenden Datentypen ausgewertet:
  
- **Zahlen**
    
- **Boolescher Wert TRUE** oder **FALSE**
    
- **Zeichenfolgen**
    
- **Fehler**
    
Gemischte Typ Arrays dieser Typen können auch in Formeln als Argumente für Funktionen oder als Werte übergreifende mehr als eine Zelle in einer Arrayformel eingegeben.
  
Wenn ein Benutzer (oder ein Makro mit Befehlen) etwas in eine Zelle eingibt, Excel versucht, die Eingabe zu interpretieren und zeigt eine Fehlermeldung an, falls es nicht möglich ist. Wenn die Eingabe mit einer Zeichenfolge Präfix (ein einfaches Anführungszeichen) beginnt platziert Excel alle Eingabezeichen in der Zelle, sofern nicht geändert werden. (Das Präfix Zeichenfolge wird nicht angezeigt.) Wenn Sie mit die Eingabe beginnt **=**, **+**, oder **-**, Excel versucht, die Eingabe als Formel interpretiert werden. Wenn die Syntax falsch ist oder Evaluation wird angehalten, ein Fehler angezeigt wird und die Zelle im hört Bearbeitungsmodus. Anderenfalls versucht Excel zu identifizieren und konvertieren Operatoren und Funktionsnamen und deren Argumente ausgewertet. 
  
Operanden werden von links nach rechts ausgewertet, bevor der Operator angewendet wird. Funktionen werden beginnend mit der höchsten Priorität Operatoren und innersten (am besten geschachtelt) ausgewertet. Wenn Funktionsargumente oder Operanden erwartet Typen konvertiert werden können, schlägt fehl und führt zu einer **#VALUE!** Fehler. Wenn ein Token (, das keinem Literalwert ist) als eine Funktion oder definierten Namen oder die Bezeichnung nicht erkannt wird, Evaluation schlägt fehl und führt zu einer **#NAME?** Fehler. 
  
Wenn die Eingabe mit einer dieser Aktionen nicht gestartet wird, Excel mit den bekannten Mustern der Eingabe wie Datumsangaben, Zeitangaben, Beträge, Prozentsätze oder Zahlen überprüft und entsprechend interpretiert. Dies ist eine Möglichkeit gebietsschemaspezifischen durchgeführt. Wenn keines dieser Interpretationen sinnvoll ist, wird von Excel kehrt er zum Berücksichtigung der Eingabe als Zeichenfolge und platziert es in der Zelle bleibt unverändert.
  
Excel unterstützt anderen Datentypen, von denen die offensichtlichsten ein Bereichsbezug ist. Excel konvertiert Verweise auf die Werte von Zellen verwiesen, beim Auswerten von Argumenten für Operatoren und Funktionen, die Verweisargumente nicht berücksichtigt, oder wenn reduziert der Ausdruck in die Formel einer Zelle auf einen Verweis.
  
Excel macht die Möglichkeit, eine beliebige gültige Zeichenfolge eines der grundlegenden vier Arbeitsblatt-Datentypen mit XLM-Funktion **EVALUATE** und die entsprechenden C-API- **XlfEvaluate**zu verringern. Diese Funktion stellt eine einfache Möglichkeit zum Bewerten der benannten Bereiche in DLL-Code unter anderem bereit. Diese Funktion unterscheidet sich vom Verhalten beschriebenen nur innerhalb der anstelle von Fehlermeldungen anzeigen oder Bearbeiten der Zelle aktivieren, es gibt eine **#VALUE!** Fehler, wenn der Ausdruck ausgewertet fällt aus. 
  
## <a name="numbers"></a>Zahlen

Alle Arbeitsblatt Zahlen in Excel werden intern als 8-Byte-Double Gleitkommazahl mit doppelter Genauigkeit, einschließlich aller ganzen Zahlen dargestellt. Jedoch ist die Implementierung dieser Zahlen in Excel nicht vollständig IEEE kompatible, wie in der folgenden Tabelle dargestellt.
  
|**Typ**|**Maximum**|**Minimum**|
|:-----|:-----|:-----|
|Double IEEE-8-Byte-Wert  <br/> |1.7976931348623157E + 308  <br/> |2.2250738585072014E-308  <br/> |
|Arbeitsblatt (zurückgegebene Wert Funktion oder einfügen)  <br/> |1.7976931348623157E + 308  <br/> |2, 22507385850721E-308  <br/> |
|Arbeitsblatt (manuelle Eingabe)  <br/> |9.99999999999999E + 307  <br/> |2, 22507385850721E-308  <br/> |
   
IEEE subnormal Zahlen (d. h., Zahlen im Bereich 2.2250738585072009E-308 4.9406564584124654E-324) werden nicht in Excel-Arbeitsblättern unterstützt, aber von VBA Double-Werte unterstützt werden.
  
Wenn eine DLL-Funktion IEEE +/-unendlich oder ein ungültiges Double-Wert zurückgibt, Excel konvertiert, um **#NUM!**. Alle subnormal-Nummern und Nummern kleiner als die minimale positive Normal in Excel werden positive 0 (null) konvertiert. IEEE negative Null unterstützt wird, d. h., sie können eine DLL-Funktion zurückgegebene und wird angezeigt als **-0**. (Die **\<** Operator prüft nicht für negative Null und **= A1\<0** auf **TRUE** ausgewertet wird, wenn A1 negative Null enthält). 
  
Beachten Sie, dass bestimmte Zahlenformate schmaler als die genannten, beispielsweise Datums- und Zeitangaben eingeschränkt. Ganzzahldivision Punkt Division ist, können Sie sogar nicht verankert und kann in extreme Fällen ein Ergebnis nicht-Integer, in dem das exakte Ergebnis werden sollte, eine ganze Zahl.
  
## <a name="long-unicode-strings"></a>Lange Unicode-Zeichenfolgen

Alle Zeichenfolgen, die der Benutzer in Excel erhält wurden für viele Versionen jetzt intern als Unicode-Zeichenfolgen gespeichert. Unicode-Arbeitsblatt Zeichenfolgen kann bis zu 32.767 (2<sup>15</sup> : 1) Zeichen und kann eine beliebige gültige Unicode-Zeichen enthalten. 
  
Wenn der C-API wurde eingeführt, Arbeitsblatt Zeichenfolgen wurden Byte-Zeichenfolgen auf eine Länge von 255 Zeichen begrenzt, und der C-API reflektiert diese Einschränkungen. Mit Excel 2007 wird der C-API aktualisiert, sodass um Excel lange Unicode-Zeichenfolgen zu behandeln. Dies bedeutet, dass die DLL-Funktionen in bequeme Weise registrierte Unicode-Argumente akzeptieren und Unicode-Zeichenfolgen zurückgeben können.
  
> [!NOTE]
> Byte-Zeichenfolgen werden in der C-API für die Abwärtskompatibilität noch vollständig unterstützt. Sie haben jedoch immer noch den gleichen Grenzwert 255 Zeichen. 
  
## <a name="returning-errors"></a>Gibt Fehler zurück

Excel wertet Zellen auf Fehler, Funktion oder einen Operator Argumente nicht in den korrekten Typ konvertiert werden können, oder wenn eine Funktion oder ein definierter Name nicht erkannt wird. Beide Szenarien wurden weiter oben beschrieben. Wenn die integrierten Arbeitsblattfunktionen und Operatoren ausfallen, führen sie auch Fehler, die den Benutzer über den Typ des Fehlers informieren. Sie sollten Ihre eigenen Fehler zurückgegeben, die dem Verhalten in Excel-add-ins Funktionen verfügen.
  
### <a name="null"></a>#NULL!

Die **#NULL!** Fehler wird durch einige XLM-Informationsfunktionen zurückgegeben. Beispielsweise Aufrufen **GET. Document(78)**, oder die entsprechende C-API funktionsfähig **XlfGetDocument** mit Argument 78, wenn es sind keine installierten Drucker Ergebnisse in dieser Fehler zurückgegeben wird. Es kann auch einige Funktionen, die zurückgegeben werden, wenn beispielsweise sie eine leere Zeichenfolge ausgewertet. 
  
Möglicherweise möchten die Add-in-Funktion dieser Fehler zurückgeben, wenn keines der anderen Fehlern angemessen.
  
### <a name="div0"></a>#DIV/0!

Gibt der Divisionsoperator Excel die **#DIV/0!** Fehler bei die Nenner 0 (null) oder eine Zahl ergibt ist zu klein wie ungleich NULL durch Excel dargestellt werden. Einige Funktionen, die per Definition eine Division beinhalten können auch dieser Fehler zurückgeben. Beispielsweise **durchschnittliche** gibt diesen Fehler zurück, wenn keine der Eingaben in Nummern konvertiert werden kann. 
  
Sie sollten nur zurückgeben dieser Fehler aus Ihrer Funktion-add-in, um anzugeben, dass eine Division durch Null erkannt wurde.
  
### <a name="value"></a>#VALUE!

Excel-gibt die **#VALUE!** Fehler, wenn ein Argument-Funktion oder -Operator in den erforderlichen Typ konvertiert werden kann. Im Fall von Funktionsargumente, beispielsweise konvertiert werden können, die `=LN("X")`, Excel nicht den Funktionscode aufgerufen. Dies ist ein wichtiger Punkt, beachten beim Schreiben und Debuggen von eigene Add-in-Funktionen. 
  
Einige Funktionen, die zurück dieser Fehler, wenn ein Argument in der Funktionscode konvertiert werden kann. Beispielsweise `DATEVALUE("30-Feb-2007")` schlägt fehl, obwohl das Argument vom richtigen Typ dieser Fehler. In diesem Fall ist es die Funktion den Fehler aus, dessen-Codes zurück. Einige Funktionen, die dieser Fehler zurückgegeben, obwohl die Werttypen und Bereiche beispielsweise zulässig sind `FIND("a","xyz")` gibt diesen Fehler zurück. 
  
Sie sollten zurückgeben dieser Fehler aus Ihrer Funktion-add-in, um anzugeben, dass die Argumente vom falschen Typ, sind nicht in den richtigen Typ konvertiert werden konnte oder liegen außerhalb des Bereichs, obwohl Sie zurückgeben berücksichtigen sollten **#NUM!** für numerische Argumente außerhalb des Bereichs. Sie sollten auch diesen Fehler zurückgibt, wenn Bereich oder Array Argumente die falsche Form oder Größe sind. 
  
### <a name="ref"></a>#REF!

Excel generiert die **#REF!** Fehler in einem Ausdruck, die an einen Speicherort kopiert werden, in dem der resultierende relative Bezug Grenzen überschreitet. Wenn die Zelle B2 die Formel enthält beispielsweise `=A1`, kopieren dies in Zelle B1 führt zu einer Formel **= #REF!**. Dieser Fehler wird auch in Formeln generiert, die einen Verweis enthalten, der in Ausschneiden und Einfügen überschrieben wird, oder in einem Zeilen-, Spalten- oder Arbeitsblatt löschen gelöscht wird. Einige Funktionen, die Verweise zurückgeben dieser Fehler beispielsweise zurückgeben können `OFFSET(A1,-1,-1)`. Für diesen Fehler werden Arbeitsblattnamen, deren Definitionen Verweise enthalten, die ungültig, ausgewertet.
  
Wenn Ihr Add-in-Funktion Verweisargumente akzeptiert, sollten Sie diesen Fehler zurückgibt, wenn die Verweise ungültig sind, oder wenn Sie einen Verweisfehler übergeben werden. Abschnitt zu XLOPER/XLOPER12s in [Speicherverwaltung in Excel](memory-management-in-excel.md) wird beschrieben, wie Funktionen erstellen, die akzeptiert und Verweisargumente zurückgeben kann. 
  
### <a name="name"></a>#NAME?

Excel generiert die **#NAME?** Fehler, wenn ein Ausdruck ein Token enthält, die nicht als Funktion erkannt wird oder definierter Name. Wenn Ihr Add-in-Funktion versucht, auf einen definierten Namen zuzugreifen und ist nicht definiert, sollten Sie diesen Fehler zurückgibt. 
  
### <a name="num"></a>#NUM!

Viele der integrierten numerischen und mathematischen Funktionen in Excel zurückgeben der **#NUM!** Fehler beim ist einer numerischen Eingabe außerhalb des zulässigen Bereichs, z. B. `LN(0)`. Sie sollten diese Fehler von Ihrer Funktion-add-in, um anzugeben, dass eine numerische Eingabe ungültig oder außerhalb des gültigen Bereichs wurde zurückgegeben.
  
### <a name="na"></a>#N/A

Häufig wird der Fehler **#n/a** zurückgegeben, um anzugeben, dass ein Ergebnis erfolgreich oder aussagekräftigen nicht verfügbar ist. Übereinstimmung mit dem dritten Argument NULL gibt beispielsweise diesen Fehler zurück, wenn eine genaue Übereinstimmung gefunden werden kann. Dieser Fehler kann auch generiert werden, mithilfe der Funktion **NA** und insbesondere mit der Funktion **ISNA**erkannt. Aus diesem Grund ist eine häufig verwendete Fehler Arbeitsblätter, um einen Bereich der anwendungsspezifischen Bedingungen anzugeben.
  
## <a name="see-also"></a>Siehe auch



[Excel-Programmierkonzepte](excel-programming-concepts.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Auswerten von Namen und andere Arbeitsblatt Formula-Ausdr�cke](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL-SDK-API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

