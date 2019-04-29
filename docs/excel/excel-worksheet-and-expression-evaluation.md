---
title: Excel-Arbeitsblatt-und Ausdrucksauswertung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Ausdrucksauswertung [Excel 2007], Fehler in Arbeitsblättern [Excel 2007], lange Unicode-Zeichenfolgen [Excel 2007], Auswerten von Ausdrücken [Excel 2007], Auswerten von Arbeitsblättern [Excel 2007], Arbeitsblatt Bewertung [Excel 2007], Arbeitsblattfehler [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cf1e0539136435f7d7df6ef348fc92ec4380e132
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427766"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Excel-Arbeitsblatt-und Ausdrucksauswertung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel-Arbeitsblattzellen Inhalte werden in einen von vier grundlegenden Datentypen ausgewertet:
  
- **Zahlen**
    
- **Boolescher Wert true** oder **false**
    
- **Zeichenfolgen**
    
- **Fehler**
    
Gemischte Arrays dieser Typen können auch als Argumente für Funktionen oder als Werte, die mehr als eine Zelle in einer Arrayformel umfassen, in Formeln eingegeben werden.
  
Wenn ein Benutzer (oder ein Befehlsmakro) etwas in eine Zelle eingibt, versucht Excel, die Eingabe zu interpretieren, und zeigt eine Fehlermeldung an, wenn dies nicht der Fall ist. Wenn die Eingabe mit einem Zeichenfolgen Präfix beginnt (ein einfaches Anführungszeichen), platziert Excel alle Eingabezeichen in der Zelle, ohne dass eine Änderung vorgenommen wird. (Das Zeichenfolgen Präfix wird nicht angezeigt.) Wenn die Eingabe mit **=**, **+** oder **-** beginnt, versucht Excel, die Eingabe als Formel zu interpretieren. Wenn die Syntax falsch ist oder die Auswertung beendet wurde, wird ein Fehler angezeigt, und die Zelle wird in den Bearbeitungsmodus versetzt. Andernfalls versucht Excel, Operatoren und Funktionsnamen sowie deren Argumente zu identifizieren, zu konvertieren und zu bewerten. 
  
Operanden werden von links nach rechts ausgewertet, bevor der Operator angewendet wird. Funktionen werden beginnend mit den Operatoren mit der höchsten Rangfolge und innersten (am meisten geschachtelten) ausgewertet. Wenn Funktionsargumente oder Operanden nicht in die erwarteten Typen konvertiert werden können, schlägt die Auswertung fehl und führt zu einem **#VALUE!** zurück. Wenn ein Token (das kein Literalwert ist) nicht als Funktion oder als definierter Name oder Bezeichnung erkannt wird, schlägt die Auswertung fehl und führt zu einem **#NAME?** -Fehler. 
  
Wenn die Eingabe nicht mit einem dieser Elemente beginnt, prüft Excel anhand bekannter Eingabemuster wie Datumsangaben, Uhrzeiten, Währungsbeträge, Prozentsätzen oder Zahlen und interpretiert diese entsprechend. Dies erfolgt in einer gebietsschemaspezifischen Methode. Wenn keine dieser Interpretationen sinnvoll ist, wird Excel zur Berücksichtigung der Eingabe als Zeichenfolge zurückgesetzt und in der Zelle unverändert platziert.
  
Excel unterstützt andere Datentypen, von denen die sichtbarste eine Range-Referenz ist. Excel konvertiert Verweise auf die Werte der referenzierten Zellen beim Auswerten von Argumenten für Operatoren und Funktionen, die keine Verweisargumente enthalten, oder wenn der Ausdruck in einer Zellenformel zu einem Verweis reduziert wird.
  
Excel macht es möglich, eine beliebige gültige Zeichenfolge zu einem der vier einfachen Arbeitsblatt Datentypen mit der XML-Funktion **Evaluate** und der C-API-Entsprechung **xlfEvaluate**zu reduzieren. Diese Funktion bietet unter anderem eine einfache Möglichkeit zum Auswerten benannter Bereiche in DLL-Code. Diese Funktion unterscheidet sich von dem zuvor beschriebenen Verhalten nur dadurch, dass anstelle von Fehlermeldungen oder Aktivieren der Zellenbearbeitung ein #VALUE zurückgegeben wird **.** Fehler, wenn die Ausdrucksauswertung fehlschlägt. 
  
## <a name="numbers"></a>Zahlen

Alle Arbeitsblatt Zahlen in Excel werden intern als Gleitkommawert mit doppelter Genauigkeit von 8 Byte, einschließlich aller ganzen Zahlen, dargestellt. Die Implementierung dieser Zahlen in Excel ist jedoch nicht vollständig IEEE-kompatibel, wie in der folgenden Tabelle dargestellt.
  
|**Type**|**Maximum**|**Mindestens**|
|:-----|:-----|:-----|
|IEEE 8-Byte-Double  <br/> |1.7976931348623157 E + 308  <br/> |2.2250738585072014 E-308  <br/> |
|Arbeitsblatt (von Function-oder Paste-Wert zurückgegeben)  <br/> |1.7976931348623157 E + 308  <br/> |2.22507385850721 E-308  <br/> |
|Arbeitsblatt (manuelle Eingabe)  <br/> |9.99999999999999 E + 307  <br/> |2.22507385850721 E-308  <br/> |
   
IEEE-subnormal-Zahlen (Zahlen im 2.2250738585072009 E-308 bis 4.9406564584124654 E-324) werden in Excel-Arbeitsblättern nicht unterstützt, sondern von VBA-Doubles unterstützt.
  
Wenn eine DLL-Funktion IEEE +/-unendlich oder ein ungültiges Double zurückgibt, wandelt Excel Sie in **#NUM!**. Alle unter normalen Zahlen und Zahlen, die kleiner als die minimale positive normale in Excel sind, werden in positive NULL konvertiert. IEEE minus 0 wird unterstützt, das heißt, Sie kann von einer DLL-Funktion zurückgegeben werden und wird als **-0**angezeigt. (Der **\<** Operator prüft nicht auf negative Null, und so **= a1\<0** ergibt **true** , wenn a1 negative Null enthält). 
  
Beachten Sie, dass bestimmte Zahlenformate schmalere Grenzwerte aufweisen, beispielsweise Datums-und Uhrzeitangaben. Die Division "Integer" ist tatsächlich eine Gleitkommadivision und kann in extremen Fällen zu einem Ergebnis ohne Ganzzahl führen, bei dem das genaue Ergebnis eine ganze Zahl sein sollte.
  
## <a name="long-unicode-strings"></a>Lange Unicode-Zeichenfolgen

Alle Zeichenfolgen, die der Benutzer in Excel sieht, sind jetzt für viele Versionen intern als Unicode-Zeichenfolgen gespeichert. Unicode-Arbeitsblatt Zeichenfolgen können bis zu 32.767 (2<sup>15</sup> -1) Zeichen lang sein und ein beliebiges gültiges Unicode-Zeichen enthalten. 
  
Bei der ersten Einführung der C-API waren Arbeitsblatt Zeichenfolgen Byte Zeichenfolgen, die in der Länge auf 255 Zeichen begrenzt waren, und die C-API reflektierte diese Einschränkungen. Mit Excel 2007 wird die C-API für die Verarbeitung von Excel Long-Unicode-Zeichenfolgen aktualisiert. Dies führt dazu, dass DLL-Funktionen, die auf die richtige Weise registriert sind, Unicode-Argumente akzeptieren und Unicode-Zeichenfolgen zurückgeben können.
  
> [!NOTE]
> Byte Zeichenfolgen werden in der C-API zur Abwärtskompatibilität weiterhin vollständig unterstützt. Sie haben jedoch immer noch dieselbe Grenze von 255 Zeichen. 
  
## <a name="returning-errors"></a>Zurückgeben von Fehlern

Excel wertet Zellen in Fehler aus, wenn Funktions-oder Operator Argumente nicht in den richtigen Typ konvertiert werden können oder wenn Sie eine Funktion oder einen definierten Namen nicht erkennen. Beide Szenarien wurden zuvor beschrieben. Wenn die integrierten Arbeitsblattfunktionen und-Operatoren fehlschlagen, führen Sie auch zu Fehlern, die den Benutzer über den Typ des Fehlers informieren. Sie sollten über ihre eigenen Add-in-Funktionen Fehler zurückgeben, die mit dem Verhalten in Excel konsistent sind.
  
### <a name="null"></a>#NULL!

Die **#NULL!** Fehler wird von einigen XML-Informationsfunktionen zurückgegeben. Beispiel: Aufrufen von **Get. DOCUMENT (78)** oder die äquivalentE C-API-Funktion **xlfGetDocument** mit Argument 78, wenn keine Drucker installiert sind, wird dieser Fehler zurückgegeben. Sie kann auch von einigen Funktionen zurückgegeben werden, wenn Sie beispielsweise eine leere Zeichenfolge auswerten. 
  
Sie können diesen Fehler von ihrer Add-in-Funktion zurückgeben, wenn keiner der anderen Fehler angemessen erscheint.
  
### <a name="div0"></a>#DIV/0!

Der Excel-Divisionsoperator gibt die **#DIV/0 zurück.** Fehler, wenn der Nenner zu NULL ausgewertet wird oder eine Zahl zu klein ist, um von Excel als ungleich NULL dargestellt zu werden. Einige Funktionen, die per Definition eine Division enthalten, können auch diesen Fehler zurückgeben. Beispielsweise gibt **Average** diesen Fehler zurück, wenn keine der Eingaben in Zahlen konvertiert werden kann. 
  
Sie sollten diesen Fehler nur in der Add-in-Funktion zurückgeben, um anzugeben, dass eine Division durch Null erkannt wurde.
  
### <a name="value"></a>#VALUE!

Excel gibt die **#VALUE zurück.** Fehler, wenn ein Function-oder Operator-Argument nicht in den erforderlichen Typ konvertiert werden kann. Bei Funktionsargumenten, die nicht konvertiert werden können, ruft Excel `=LN("X")`beispielsweise nicht den Funktionscode auf. Dies ist ein wichtiger Punkt, um sich zu erinnern, wenn Sie Ihre eigenen Add-in-Funktionen schreiben und Debuggen. 
  
Einige Funktionen geben diesen Fehler zurück, wenn ein Argument nicht innerhalb des Funktionscodes konvertiert werden kann. Beispielsweise `DATEVALUE("30-Feb-2007")` schlägt mit diesem Fehler trotz des Arguments des richtigen Typs. In diesem Fall ist es die Funktion, die den Fehler innerhalb des Codes zurückgibt. Einige Funktionen geben diesen Fehler zurück, obwohl die Werttypen und-Bereiche zulässig sind, Beispiels `FIND("a","xyz")` Weise wird dieser Fehler zurückgegeben. 
  
Sie sollten diesen Fehler von der Add-in-Funktion zurückgeben, um anzugeben, dass die Argumente vom falschen Typ sind, nicht in den richtigen Typ konvertiert werden können oder außerhalb des gültigen Gültigkeitsbereichs liegen, obwohl Sie **#NUM** zurückgeben sollten! für numerische Argumente außerhalb des gültigen Gültigkeitsbereichs. Sie sollten diesen Fehler auch dann zurückgeben, wenn Range-oder Array-Argumente die falsche Form oder Größe aufweisen. 
  
### <a name="ref"></a>#REF!

Excel generiert die **#REF!** Fehler innerhalb eines Ausdrucks, wenn er an einen Speicherort kopiert wird, an dem der resultierende relative Verweis außerhalb der Grenzen liegt. Wenn die Zelle B2 beispielsweise die Formel `=A1`enthält, führt das Kopieren dieses in Zelle B1 zu einer formel **= #REF!**. Dieser Fehler wird auch in Formeln generiert, die einen Verweis enthalten, der in einem Cut-and-Paste-Vorgang überschrieben wird oder in einer Zeile, Spalte oder Arbeitsblatt Löschung gelöscht wird. Einige Funktionen, die Verweise zurückgeben können, können diesen Fehler zurückgeben `OFFSET(A1,-1,-1)`, beispielsweise. Arbeitsblattnamen, deren Definitionen ungültige Verweise enthalten, werden auf diesen Fehler ausgewertet.
  
Wenn die Add-in-Funktion Verweisargumente verwendet, sollten Sie diesen Fehler zurückgeben, wenn die Verweise ungültig sind oder wenn Sie einen Verweisfehler übergeben werden. Im Abschnitt zu XLOPER/XLOPER12s in [Memory Management in Excel](memory-management-in-excel.md) wird beschrieben, wie Sie Funktionen erstellen, die Verweisargumente akzeptieren und zurückgeben können. 
  
### <a name="name"></a>#NAME?

Excel generiert den **#NAME?** -Fehler, wenn ein Ausdruck ein Token enthält, das nicht als Funktion oder definierter Name erkannt wird. Wenn Ihre Add-in-Funktion versucht, auf einen definierten Namen zuzugreifen, und Sie nicht definiert ist, sollten Sie diesen Fehler zurückgeben. 
  
### <a name="num"></a>#NUM!

Viele der integrierten numerischen und mathematischen Funktionen in Excel geben den #NUM zurück **.** Fehler, wenn eine numerische Eingabe außerhalb des zulässigen Zeitraums ist, beispielsweise `LN(0)`. Sie sollten diesen Fehler von der Add-in-Funktion zurückgeben, um anzugeben, dass eine numerische Eingabe ungültig oder außerhalb des gültigen Gültigkeitsbereichs liegt.
  
### <a name="na"></a>#N/A

Der **#N/a** -Fehler wird häufig zurückgegeben, damit ein erfolgreiches oder aussagekräftiges Ergebnis nicht verfügbar ist. Beispiel: Übereinstimmung mit dem dritten Argument NULL gibt diesen Fehler zurück, wenn eine exakte Übereinstimmung nicht gefunden werden kann. Dieser Fehler kann auch mit der Funktion **na** generiert werden und speziell mit der Funktion **ISTNV**erkannt werden. Es ist daher ein häufig verwendeter Fehler in Arbeitsblättern, um eine Reihe von anwendungsspezifischen Bedingungen anzugeben.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

