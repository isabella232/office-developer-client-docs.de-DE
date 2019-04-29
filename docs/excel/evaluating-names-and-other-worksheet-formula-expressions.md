---
title: Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Ausdrucksauswertung [Excel 2007], Arbeitsblätter [Excel 2007], Namensauswertung, Auswerten von Ausdrücken [Excel 2007], Auswerten von Arbeitsblattnamen [Excel 2007], Ausdrücke [Excel 2007], auswerten, Namen [Excel 2007], auswerten, Namensauswertung [Excel 2007] , Zeichenfolgen [Excel 2007], konvertieren in Werte, xlfEvaluate-Funktion [Excel 2007], Arbeitsblätter [Excel 2007], Ausdrucksauswertung
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406864"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Eine der wichtigsten Features, die Excel über die C-API verfügbar macht, ist die Möglichkeit, beliebige Zeichenfolgen Formeln, die rechtlich in ein Arbeitsblatt eingegeben werden können, in einen Wert oder ein Array von Werten umzuwandeln. Dies ist für XLL-Funktionen und Befehle unerlässlich, die beispielsweise den Inhalt definierter Namen lesen müssen. Diese Fähigkeit wird über die [xlfEvaluate-Funktion](xlfevaluate.md)offen gelegt, wie in diesem Beispiel gezeigt.
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

Beachten Sie Folgendes: Wenn Sie einen Arbeitsblattnamen auswerten, entweder eigenständig oder in einer Formel, müssen Sie den Namen mindestens mit "!" voranstellen. Andernfalls versucht Excel, den Namen in einem ausgeblendeten Namespace zu finden, der für DLLs reserviert ist. Sie können mit der [xlfSetName-Funktion](xlfsetname.md)versteckte DLL-Namen erstellen und löschen. Sie können die Definition eines definierten Namens abrufen, unabhängig davon, ob es sich um einen versteckten DLL-Namen oder einen Arbeitsblattnamen handelt, indem Sie die **xlfGetDef** -Funktion verwenden. 
  
Die vollständige Spezifikation für einen Arbeitsblattnamen hat das folgende Format:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Beachten Sie, dass Excel 2007 eine Reihe neuer Dateierweiterungen eingeführt hat. Sie können den Pfad, den Namen der Arbeitsmappe und den Namen des Blatts weglassen, wobei die geöffneten Arbeitsmappen in dieser Excel-Sitzung nicht eindeutig sind. 
  
Im nächsten Beispiel wird die Formel `COUNT(A1:IV65536)` für das aktive Arbeitsblatt ausgewertet und das Ergebnis angezeigt. Beachten Sie, dass die Range-Adresse mit "!" vorangestellt werden muss, was mit der Range Reference Convention in XML-Makro Blättern konsistent ist. Die C-API XML folgt diesem Übereinkommen: 
  
- `=A1`Ein Verweis auf die Zelle a1 in der aktuellen Makrovorlage. (Nicht für XLLs definiert). 
  
- `=!A1`Ein Verweis auf die Zelle a1 auf dem aktiven Blatt (Dies kann ein Arbeitsblatt oder ein Makroblatt sein) 
  
- `=Sheet1!A1`Ein Verweis auf die Zelle a1 auf dem angegebenen Blatt, Sheet1 in diesem Fall. 
  
- `=[Book1.xls]Sheet1!A1`Ein Verweis auf die Zelle a1 auf dem angegebenen Blatt in der angegebenen Arbeitsmappe. 
  
In einer XLL kann ein Verweis ohne ein führendes Ausrufezeichen (**!**) nicht in einen Wert konvertiert werden. Es hat keine Bedeutung, da es keine aktuelle Makrovorlage gibt. Beachten Sie, dass ein führendes**=** Gleichheitszeichen () optional ist und im nächsten Beispiel ausgelassen wird.
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

Sie können auch die **XLFEVALUATE** -Funktion verwenden, um die Registrierungs-ID einer XLL-Funktion aus dem registrierten Namen abzurufen, die dann zum Aufrufen dieser Funktion mithilfe der [xlUDF-Funktion](xludf.md)verwendet werden kann.
  
> [!NOTE]
> Der registrierte Name kann direkt an die **xlUDF** -Funktion übergeben werden. Das heißt, Sie können verhindern, dass Sie den Namen auswerten, um die ID zu erhalten, bevor Sie **xlUDF**aufrufen. Wenn die Funktion jedoch mehrmals aufgerufen werden soll, wird Sie mit der Registrierungs-ID schneller ausgeführt. 
  
## <a name="see-also"></a>Siehe auch

- [Excel-Arbeitsblatt- und Ausdrucksauswertung](excel-worksheet-and-expression-evaluation.md)
- [Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen](permitting-user-breaks-in-lengthy-operations.md)
- [Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

