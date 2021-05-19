---
title: Excel Arbeitsblatt- und Ausdrucksauswertung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Ausdrucksauswertung [excel 2007],Fehler in Arbeitsblättern [Excel 2007],lange Unicode-Zeichenfolgen [Excel 2007],Auswerten von Ausdrücken [Excel 2007],Auswerten von Arbeitsblättern [Excel 2007],Arbeitsblattauswertung [Excel 2007],Arbeitsblattfehler [Excel 2007]
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
# <a name="excel-worksheet-and-expression-evaluation"></a>Excel Arbeitsblatt- und Ausdrucksauswertung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel Inhalt von Arbeitsblattzellen werden in einen von vier grundlegenden Datentypen ausgewertet:
  
- **Zahlen**
    
- **Boolean TRUE** oder **FALSE**
    
- **Zeichenfolgen**
    
- **Fehler**
    
Gemischte Arrays dieser Typen können auch in Formeln als Argumente für Funktionen oder als Werte eingegeben werden, die sich über mehrere Zellen in einer Arrayformel erstreckt.
  
Wenn ein Benutzer (oder ein Befehlsmakro) etwas in eine Zelle eintritt, versucht Excel, die Eingabe zu interpretieren, und zeigt eine Fehlermeldung an, wenn dies nicht möglich ist. Wenn die Eingabe mit einem Zeichenfolgenpräfix (ein einfaches Anführungszeichen) beginnt, werden Excel alle Eingabezeichen in der Zelle platziert, wie angegeben, ohne Änderung. (Das Zeichenfolgenpräfix wird nicht angezeigt.) Wenn die Eingabe mit **=** , **+** oder beginnt, Excel versucht, die Eingabe **-** als Formel zu interpretieren. Wenn die Syntax falsch ist oder die Auswertung beendet wird, wird ein Fehler angezeigt, und die Zelle wird in den Bearbeitungsmodus versetzt. Andernfalls Excel versucht, Operatoren und Funktionsnamen sowie deren Argumente zu identifizieren, zu konvertieren und auszuwerten. 
  
Operanden werden von links nach rechts ausgewertet, bevor der Operator angewendet wird. Funktionen werden beginnend mit den Operatoren mit der höchsten Rangfolge und dem innersten (am häufigsten geschachtelten) ausgewertet. Wenn Funktionsargumente oder Operanden nicht in die erwarteten Typen konvertiert werden können, schlägt die Auswertung fehl und führt zu **#VALUE!** zurück. Wenn ein Token (das kein Literalwert ist) nicht als Funktion oder definierter Name oder Bezeichnung erkannt wird, schlägt die Auswertung fehl und führt zu einem **#NAME?** Fehler. 
  
Wenn die Eingabe mit keinem dieser Dinge beginnt, überprüft Excel bekannte Eingabemuster wie Datumsangaben, Zeiten, Währungsbeträge, Prozentsätze oder Zahlen und interpretiert entsprechend. Dies erfolgt auf eine locale-spezifische Weise. Wenn keine dieser Interpretationen sinnvoll ist, wird Excel die Eingabe als Zeichenfolge betrachtet und unverändert in der Zelle platziert.
  
Excel unterstützt andere Datentypen, von denen der sichtbarste ein Bereichsverweis ist. Excel konvertiert Verweise auf die Werte der auf Zellen verwiesenen Zellen, wenn Argumente für Operatoren und Funktionen ausgewertet werden, die keine Referenzargumente verwenden, oder wenn der Ausdruck in einer Zellformel auf einen Verweis reduziert wird.
  
Excel die Möglichkeit, alle gültigen Zeichenzeichenfolgen auf einen der grundlegenden vier Arbeitsblattdatentypen zu reduzieren, mit der XLM-Funktion **EVALUATE** und ihrer C-API-Entsprechung **xlfEvaluate**. Diese Funktion bietet unter anderem eine einfache Möglichkeit, benannte Bereiche im DLL-Code auszuwerten. Diese Funktion unterscheidet sich vom zuvor beschriebenen Verhalten nur dadurch, dass sie anstelle von Fehlermeldungen oder aktivieren der Zellbearbeitung ein **#VALUE!** fehler, wenn die Ausdrucksauswertung fehlschlägt. 
  
## <a name="numbers"></a>Zahlen

Alle Arbeitsblattnummern in Excel intern als Gleitkomma mit doppelter Genauigkeit mit 8 Byte dargestellt, einschließlich aller ganzzahligen Zahlen. Die Implementierung dieser Nummern in Excel ist jedoch nicht vollständig IEEE-kompatibel, wie in der folgenden Tabelle dargestellt.
  
|**Typ**|**Maximum**|**Minimum**|
|:-----|:-----|:-----|
|IEEE 8-Byte-Double  <br/> |1.7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|Arbeitsblatt (zurückgegeben durch Funktion oder Einfügewert)  <br/> |1.7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|Arbeitsblatt (manuelle Eingabe)  <br/> |9.9999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
IEEE subnormale Zahlen (d. h. Zahlen im Bereich 2.2250738585072009E-308 bis 4.9406564584124654E-324) werden in Excel-Arbeitsblättern nicht unterstützt, aber von VBA Doubles unterstützt.
  
Wenn eine DLL-Funktion IEEE +/- infinity oder ein ungültiges Double zurückgibt, konvertiert Excel in **#NUM!**. Alle subnormalen Zahlen und Zahlen, die kleiner als die minimale positive Normalität in Excel werden in positive Null konvertiert. IEEE negative Null wird unterstützt, d. h. sie kann von einer DLL-Funktion zurückgegeben werden und wird als **-0 angezeigt.** (Der **\<** Operator überprüft nicht auf negative Null, und daher wird **=A1 \< 0** auf **TRUE** ausgewertet, wenn A1 negative Null enthält). 
  
Beachten Sie, dass bestimmte Zahlenformate engere Grenzwerte als diese haben, z. B. Datums- und Zeitangaben. Die ganzzahlige Division ist in der Tat eine Gleitkommateilung und kann im Extremfall zu einem Ergebnis führen, das nicht ganzzahlig ist, bei dem das genaue Ergebnis eine ganze Zahl sein sollte.
  
## <a name="long-unicode-strings"></a>Lange Unicode-Zeichenfolgen

Alle Zeichenfolgen, die dem Benutzer in Excel werden nun für viele Versionen intern als Unicode-Zeichenfolgen gespeichert. Unicode-Arbeitsblattzeichenfolgen können bis zu 32.767 (2<sup>15</sup> - 1) Zeichen lang sein und ein beliebiges gültiges Unicode-Zeichen enthalten. 
  
Bei der ersten Einführung der C-API waren Arbeitsblattzeichenfolgen Bytezeichenfolgen, die auf 255 Zeichen beschränkt waren, und die C-API spiegelte diese Einschränkungen wider. Mit Excel 2007 wird die C-API so aktualisiert, dass sie Excel #A0 verarbeiten kann. Dies bedeutet, dass dll-Funktionen, die auf die richtige Weise registriert wurden, Unicode-Argumente akzeptieren und Unicode-Zeichenfolgen zurückgeben können.
  
> [!NOTE]
> Bytezeichenfolgen werden zur Abwärtskompatibilität weiterhin vollständig in der C-API unterstützt. Sie haben jedoch weiterhin denselben Grenzwert von 255 Zeichen. 
  
## <a name="returning-errors"></a>Zurückgeben von Fehlern

Excel wertet Zellen zu Fehlern aus, bei denen Funktions- oder Operatorargumente nicht in den richtigen Typ konvertiert werden können oder wenn eine Funktion oder ein definierter Name nicht erkannt wird. Beide Szenarien wurden bereits beschrieben. Wenn die integrierten Arbeitsblattfunktionen und -operatoren fehlschlagen, führen sie auch zu Fehlern, die den Benutzer über den Fehlertyp informieren. Ihre eigenen Add-In-Funktionen sollten Fehler zurückgeben, die mit dem Verhalten in der Excel.
  
### <a name="null"></a>#NULL!

Die **#NULL!** fehler wird von einigen XLM-Informationsfunktionen zurückgegeben. Wenn sie z. **B.GET.DOCUMENT(78)** oder die entsprechende C-API-Funktion **xlfGetDocument** mit argument 78 aufrufen, wenn keine Drucker installiert sind, wird dieser Fehler zurückgegeben. Sie kann auch von einigen Funktionen zurückgegeben werden, wenn sie beispielsweise eine leere Zeichenfolge auswerten. 
  
Möglicherweise möchten Sie diesen Fehler von Ihrer Add-In-Funktion zurückgeben, wenn keiner der anderen Fehler geeignet erscheint.
  
### <a name="div0"></a>#DIV/0!

Der Excel -Abteilungsoperator gibt die **#DIV/0 zurück!** Fehler, wenn der Nenner zu Null ausgewertet wird oder eine Zahl zu klein ist, um von der Excel. Einige Funktionen, die definitionsgemäß eine Abteilung umfassen, können diesen Fehler ebenfalls zurückgeben. Beispielsweise gibt **AVERAGE** diesen Fehler zurück, wenn keine der Eingaben in Zahlen konvertiert werden kann. 
  
Sie sollten diesen Fehler nur von Ihrer Add-In-Funktion zurückgeben, um anzugeben, dass eine Division mit Null erkannt wurde.
  
### <a name="value"></a>#VALUE!

Excel gibt die **#VALUE!** fehler, wenn ein Funktions- oder Operatorargument nicht in den erforderlichen Typ konvertiert werden kann. Bei Funktionsargumenten, die nicht konvertiert werden können, z. `=LN("X")` B. wird Excel Funktionscode nicht aufruft. Dies ist ein wichtiger Punkt, den Sie beim Schreiben und Debuggen Ihrer eigenen Add-In-Funktionen beachten sollten. 
  
Einige Funktionen geben diesen Fehler zurück, wenn ein Argument nicht innerhalb des Funktionscodes konvertiert werden kann. Beispielsweise tritt  `DATEVALUE("30-Feb-2007")` bei diesem Fehler ein Fehler auf, obwohl das Argument den richtigen Typ hat. In diesem Fall ist es die Funktion, die den Fehler innerhalb des Codes zurücksent. Einige Funktionen geben diesen Fehler zurück, obwohl die Werttypen und -bereiche zulässig sind, z. B.  `FIND("a","xyz")` gibt diesen Fehler zurück. 
  
Sie sollten diesen Fehler von Ihrer Add-In-Funktion zurückgeben, um anzugeben, dass die Argumente den falschen Typ haben, nicht in den richtigen Typ konvertiert werden konnten oder sich nicht im Bereich befinden, obwohl Sie die Rückgabe von **#NUM!** für numerische Argumente, die nicht im Bereich liegen. Sie sollten diesen Fehler auch zurückgeben, wenn Bereichs- oder Arrayargumente die falsche Form oder Größe sind. 
  
### <a name="ref"></a>#REF!

Excel generiert die **#REF!** fehler innerhalb eines Ausdrucks, wenn er an einen Speicherort kopiert wird, an dem der resultierende relative Verweis nicht mehr in Grenzen liegt. Wenn die Zelle B2 beispielsweise die Formel enthält, führt das Kopieren in Zelle B1 zu einer Formel  `=A1` **=#REF!**. Dieser Fehler wird auch in Formeln generiert, die einen Verweis enthalten, der in einem Ausschneiden und Einfügen überschrieben oder in einer Zeile, Spalte oder einem Arbeitsblatt gelöscht wird. Einige Funktionen, die Verweise zurückgeben können, können diesen Fehler zurückgeben, z. B.  `OFFSET(A1,-1,-1)` . Arbeitsblattnamen, deren Definitionen ungültige Verweise enthalten, werden auf diesen Fehler ausgewertet.
  
Wenn Ihre Add-In-Funktion Referenzargumente verwendet, sollten Sie diesen Fehler zurückgeben, wenn die Verweise ungültig sind oder ein Verweisfehler übergeben wurde. Im Abschnitt xlOPER/XLOPER12s in [Memory Management in Excel](memory-management-in-excel.md) wird beschrieben, wie Sie Funktionen erstellen, die Referenzargumente akzeptieren und zurückgeben können. 
  
### <a name="name"></a>#NAME?

Excel generiert den **#NAME?-Fehler,** wenn ein Ausdruck ein Token enthält, das nicht als Funktion oder definierter Name erkannt wird. Wenn Ihre Add-In-Funktion versucht, auf einen definierten Namen zu zugreifen und sie nicht definiert ist, sollten Sie diesen Fehler zurückgeben. 
  
### <a name="num"></a>#NUM!

Viele der integrierten numerischen und mathematischen Funktionen in Excel geben die **#NUM!** fehler, wenn eine numerische Eingabe nicht im zulässigen Bereich liegt, z. B.  `LN(0)` . Sie sollten diesen Fehler von Ihrer Add-In-Funktion zurückgeben, um anzugeben, dass eine numerische Eingabe ungültig oder nicht gültig war.
  
### <a name="na"></a>#N/A

Der **#N/A-Fehler** wird häufig zurückgegeben, um zu signalisieren, dass ein erfolgreiches oder aussagekräftiges Ergebnis nicht verfügbar ist. Beispiel: MATCH mit dem dritten Argument Null gibt diesen Fehler zurück, wenn keine genaue Übereinstimmung gefunden werden kann. Dieser Fehler kann auch mithilfe der Funktion **NA** generiert und speziell mit der Funktion **ISNA erkannt werden.** Daher ist es ein häufig verwendeter Fehler in Arbeitsblättern, um einen Bereich anwendungsspezifischer Bedingungen anzugeben.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

