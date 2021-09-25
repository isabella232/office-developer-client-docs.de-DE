---
title: Excel Arbeitsblatt- und Ausdrucksauswertung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e3f7887d15b5cdb783647f0bbd5b9778354f054e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601373"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Excel Arbeitsblatt- und Ausdrucksauswertung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel Inhalt der Arbeitsblattzelle werden in einen von vier grundlegenden Datentypen ausgewertet:
  
- **Zahlen**
    
- **Boolean TRUE** oder **FALSE**
    
- **Zeichenfolgen**
    
- **Fehler**
    
Arrays mit gemischten Typen dieser Typen können auch in Formeln als Argumente für Funktionen oder als Werte eingegeben werden, die mehr als eine Zelle in einer Arrayformel umfassen.
  
Wenn ein Benutzer (oder ein Befehlsmakro) etwas in eine Zelle eingibt, versucht Excel, die Eingabe zu interpretieren, und zeigt eine Fehlermeldung an, falls dies nicht möglich ist. Wenn die Eingabe mit einem Zeichenfolgenpräfix (einem einfachen Anführungszeichen) beginnt, Excel alle Eingabezeichen ohne Änderung in der Zelle platziert. (Das Zeichenfolgenpräfix wird nicht angezeigt.) Wenn die Eingabe mit **=** , oder , Excel **+** **-** versucht, die Eingabe als Formel zu interpretieren. Wenn die Syntax falsch ist oder die Auswertung beendet wird, wird ein Fehler angezeigt, und die Zelle wird in den Bearbeitungsmodus versetzt. Andernfalls versucht Excel, Operatoren und Funktionsnamen und deren Argumente zu identifizieren, zu konvertieren und auszuwerten. 
  
Operanden werden von links nach rechts ausgewertet, bevor der Operator angewendet wird. Funktionen werden beginnend mit den Operatoren mit der höchsten Rangfolge und den innersten (am häufigsten geschachtelten) Operatoren ausgewertet. Wenn Funktionsargumente oder Operanden nicht in die erwarteten Typen konvertiert werden können, schlägt die Auswertung fehl und führt zu einem **#VALUE!** zurück. Wenn ein Token (das kein Literalwert ist) nicht als Funktion oder definierter Name oder Bezeichnung erkannt wird, schlägt die Auswertung fehl und führt zu einem **#NAME?-Fehler.** 
  
Wenn die Eingabe nicht mit diesen Elementen beginnt, überprüft Excel bekannte Eingabemuster wie Datumsangaben, Uhrzeiten, Währungsbeträge, Prozentsätze oder Zahlen und interpretiert sie entsprechend. Dies erfolgt gebietsschemaspezifisch. Wenn keine dieser Interpretationen sinnvoll ist, wird Excel die Eingabe als Zeichenfolge betrachten und unverändert in der Zelle platziert.
  
Excel unterstützt andere Datentypen, deren sichtbarste Datentyp ein Bereichsverweis ist. Excel konvertiert Beim Auswerten von Argumenten für Operatoren und Funktionen, die keine Verweisargumente verwenden, oder wenn der Ausdruck in einer Zellformel auf einen Verweis reduziert wird, werden Verweise auf die Werte der zellenverweisten Zellen konvertiert.
  
Excel bietet die Möglichkeit, eine beliebige gültige Zeichenzeichenfolge auf einen der vier grundlegenden Arbeitsblatt-Datentypen mit der XLM-Funktion **EVALUATE** und dem entsprechenden C-API-Äquivalent **xlfEvaluate** zu reduzieren. Diese Funktion bietet unter anderem eine einfache Möglichkeit, benannte Bereiche im DLL-Code auszuwerten. Diese Funktion unterscheidet sich nur dadurch vom zuvor beschriebenen Verhalten, dass anstelle von Fehlermeldungen oder der Aktivierung der Zellbearbeitung ein #VALUE zurückgegeben **wird.** fehler, wenn die Auswertung des Ausdrucks fehlschlägt. 
  
## <a name="numbers"></a>Zahlen

Alle Arbeitsblattnummern in Excel werden intern als Gleitkommazahl mit doppelter Genauigkeit von 8 Byte dargestellt, einschließlich aller ganzen Zahlen. Die Implementierung dieser Nummern in Excel ist jedoch nicht vollständig IEEE-kompatibel, wie in der folgenden Tabelle dargestellt.
  
|**Typ**|**Maximum**|**Minimum**|
|:-----|:-----|:-----|
|IEEE 8-Byte-Double  <br/> |1,7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|Arbeitsblatt (zurückgegeben von Funktion oder Einfügewert)  <br/> |1,7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|Arbeitsblatt (manuelle Eingabe)  <br/> |9,99999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
Unternormale IEEE-Nummern (d. h. Zahlen im Bereich von 2,2250738585072009E-308 bis 4,9406564584124654E-324) werden in Excel Arbeitsblättern nicht unterstützt, werden jedoch von VBA Doubles unterstützt.
  
Wenn eine DLL-Funktion IEEE +/- infinity oder einen ungültigen Double zurückgibt, konvertiert Excel sie in **#NUM!**. Alle subnormalen Zahlen und Zahlen, die kleiner als die minimale positive Normalzahl in Excel sind, werden in positive Null konvertiert. IEEE negative Null wird unterstützt, d. h., sie kann von einer DLL-Funktion zurückgegeben werden und wird als **-0** angezeigt. (Der **\<** Operator überprüft nicht auf negative Null, und daher wird **=A1 \< 0** zu **TRUE** ausgewertet, wenn A1 negative Null enthält). 
  
Beachten Sie, dass bestimmte Zahlenformate schmaler sind als diese, z. B. Datums- und Uhrzeitangaben. Bei der Ganzzahlteilung handelt es sich tatsächlich um eine Gleitkommateilung und kann in Extremfällen zu einem Ergebnis führen, bei dem das genaue Ergebnis eine ganze Zahl sein sollte.
  
## <a name="long-unicode-strings"></a>Lange Unicode-Zeichenfolgen

Alle Zeichenfolgen, die dem Benutzer in Excel für viele Versionen angezeigt werden, wurden jetzt intern als Unicode-Zeichenfolgen gespeichert. Unicode-Arbeitsblattzeichenfolgen können bis zu 32.767 (2<sup>15</sup> - 1) Zeichen lang sein und ein beliebiges gültiges Unicode-Zeichen enthalten. 
  
Bei der ersten Einführung der C-API waren Arbeitsblattzeichenfolgen Bytezeichenfolgen, die auf 255 Zeichen beschränkt waren, und die C-API spiegelte diese Einschränkungen wider. Mit Excel 2007 wird die C-API aktualisiert, um Excel lange Unicode-Zeichenfolgen zu verarbeiten. Dies bedeutet, dass auf die richtige Weise registrierte DLL-Funktionen Unicode-Argumente akzeptieren und Unicode-Zeichenfolgen zurückgeben können.
  
> [!NOTE]
> Bytezeichenfolgen werden in der C-API aus Gründen der Abwärtskompatibilität weiterhin vollständig unterstützt. Sie haben jedoch immer noch den gleichen Grenzwert von 255 Zeichen. 
  
## <a name="returning-errors"></a>Zurückgeben von Fehlern

Excel wertet Zellen zu Fehlern aus, bei denen Funktions- oder Operatorargumente nicht in den richtigen Typ konvertiert werden können oder wenn eine Funktion oder ein definierter Name nicht erkannt wird. Beide Szenarien wurden zuvor beschrieben. Wenn die integrierten Arbeitsblattfunktionen und -operatoren fehlschlagen, führen sie auch zu Fehlern, die den Benutzer über den Typ des Fehlers informieren. Ihre eigenen Add-In-Funktionen sollten Fehler zurückgeben, die mit dem Verhalten in Excel übereinstimmen.
  
### <a name="null"></a>#NULL!

Die **#NULL!** wird von einigen XLM-Informationsfunktionen zurückgegeben. Rufen Sie z. **B. GET auf. DOCUMENT(78)** oder die entsprechende C-API-Funktion **xlfGetDocument** mit Argument 78, wenn keine Drucker installiert sind, wird dieser Fehler zurückgegeben. Sie kann auch von einigen Funktionen zurückgegeben werden, wenn sie z. B. eine leere Zeichenfolge auswerten. 
  
Sie können diesen Fehler von Ihrer Add-In-Funktion zurückgeben, wenn keiner der anderen Fehler geeignet erscheint.
  
### <a name="div0"></a>#DIV/0!

Der Excel Division-Operator gibt den **#DIV/0!** wenn der Nenner als Null ausgewertet wird oder eine Zahl zu klein ist, um durch Excel als Nicht-Null dargestellt zu werden. Einige Funktionen, die definitionsgemäß eine Division umfassen, können diesen Fehler auch zurückgeben. Beispielsweise gibt **AVERAGE** diesen Fehler zurück, wenn keine der Eingaben in Zahlen konvertiert werden kann. 
  
Sie sollten diesen Fehler nur aus Ihrer Add-In-Funktion zurückgeben, um anzugeben, dass eine Division durch Null erkannt wurde.
  
### <a name="value"></a>#VALUE!

Excel gibt die **#VALUE zurück!** fehler, wenn eine Funktion oder ein Operatorargument nicht in den erforderlichen Typ konvertiert werden kann. Bei Funktionsargumenten, die beispielsweise nicht konvertiert werden `=LN("X")` können, ruft Excel den Funktionscode nicht auf. Dies ist ein wichtiger Punkt, den Sie beim Schreiben und Debuggen Ihrer eigenen Add-In-Funktionen beachten sollten. 
  
Einige Funktionen geben diesen Fehler zurück, wenn ein Argument nicht innerhalb des Funktionscodes konvertiert werden kann. Schlägt beispielsweise  `DATEVALUE("30-Feb-2007")` mit diesem Fehler fehl, obwohl das Argument den richtigen Typ aufweist. In diesem Fall gibt die Funktion den Fehler innerhalb des Codes zurück. Einige Funktionen geben diesen Fehler zurück, obwohl die Werttypen und -bereiche zulässig sind,  `FIND("a","xyz")` z. B. wird dieser Fehler zurückgegeben. 
  
Sie sollten diesen Fehler von Ihrer Add-In-Funktion zurückgeben, um anzugeben, dass die Argumente den falschen Typ aufweisen, nicht in den richtigen Typ konvertiert werden konnten oder außerhalb des Gültigen liegen, obwohl Sie erwägen sollten, **#NUM zurückzugeben!** für numerische Argumente außerhalb des Bereichs. Sie sollten diesen Fehler auch zurückgeben, wenn Bereichs- oder Arrayargumente die falsche Form oder Größe sind. 
  
### <a name="ref"></a>#REF!

Excel generiert die **#REF!** fehler in einem Ausdruck, wenn er an eine Stelle kopiert wird, an der der resultierende relative Bezug außerhalb der Grenzen liegt. Wenn die Zelle B2 beispielsweise die Formel enthält, führt das  `=A1` Kopieren in Zelle B1 zu einer Formel **=#REF!**. Dieser Fehler wird auch in Formeln generiert, die einen Verweis enthalten, der in einem Ausschneide- und Einfügevorgang überschrieben oder in einer Zeile, Spalte oder Arbeitsblattlöschung gelöscht wird. Einige Funktionen, die Verweise zurückgeben können, können diesen Fehler zurückgeben,  `OFFSET(A1,-1,-1)` z. B. . Arbeitsblattnamen, deren Definitionen ungültige Verweise enthalten, werden für diesen Fehler ausgewertet.
  
Wenn Ihre Add-In-Funktion Verweisargumente verwendet, sollten Sie diesen Fehler zurückgeben, wenn die Verweise ungültig sind oder wenn Sie einen Verweisfehler erhalten. Im Abschnitt zu XLOPER/XLOPER12s in [memory management in Excel](memory-management-in-excel.md) wird beschrieben, wie Sie Funktionen erstellen, die Verweisargumente akzeptieren und zurückgeben können. 
  
### <a name="name"></a>#NAME?

Excel generiert den **#NAME?-Fehler,** wenn ein Ausdruck ein Token enthält, das nicht als Funktion oder definierter Name erkannt wird. Wenn Ihre Add-In-Funktion versucht, auf einen definierten Namen zuzugreifen, und dieser nicht definiert ist, sollten Sie diesen Fehler zurückgeben. 
  
### <a name="num"></a>#NUM!

Viele der integrierten numerischen und mathematischen Funktionen in Excel die **#NUM zurückgeben!** fehler, wenn eine numerische Eingabe außerhalb des zulässigen Bereichs liegt, z.  `LN(0)` B. . Sie sollten diesen Fehler aus Ihrer Add-In-Funktion zurückgeben, um anzugeben, dass eine numerische Eingabe ungültig oder außerhalb des Gültigen bereichs war.
  
### <a name="na"></a>#N/A

Der **#N/A-Fehler** wird häufig zurückgegeben, um anzuzeigen, dass ein erfolgreiches oder aussagekräftiges Ergebnis nicht verfügbar ist. Beispielsweise gibt MATCH mit dem dritten Argument Null diesen Fehler zurück, wenn keine genaue Übereinstimmung gefunden werden kann. Dieser Fehler kann auch mithilfe der Funktion **NA** generiert und speziell mit der **Funktion ISNA** erkannt werden. Es ist daher ein häufig verwendeter Fehler in Arbeitsblättern, um einen Bereich von anwendungsspezifischen Bedingungen anzugeben.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

