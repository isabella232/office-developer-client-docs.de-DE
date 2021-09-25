---
title: Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
ms.localizationpriority: medium
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f2a9f1221acead606b71eedf6deb09133ad25a39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552255"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Eines der wichtigsten Features, die Excel über die C-API verfügbar machen, ist die Möglichkeit, beliebige Zeichenfolgenformeln, die gesetzlich in ein Arbeitsblatt eingegeben werden können, in einen Wert oder ein Array von Werten zu konvertieren. Dies ist wichtig für XLL-Funktionen und -Befehle, die beispielsweise den Inhalt definierter Namen lesen müssen. Diese Fähigkeit wird über die [xlfEvaluate-Funktion](xlfevaluate.md)verfügbar gemacht, wie in diesem Beispiel gezeigt.
  
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

Beachten Sie, dass Sie beim Auswerten eines Arbeitsblattnamens , entweder allein oder in einer Formel, dem Namen mindestens das Präfix "!" voran stellen müssen. Andernfalls versucht Excel, den Namen in einem ausgeblendeten Namespace zu finden, der für DLLs reserviert ist. Sie können ausgeblendete DLL-Namen mithilfe der [xlfSetName-Funktion](xlfsetname.md)erstellen und löschen. Mithilfe der **xlfGetDef-Funktion** können Sie die Definition eines beliebigen definierten Namens abrufen, unabhängig davon, ob es sich um einen ausgeblendeten DLL-Namen oder einen Arbeitsblattnamen handelt. 
  
Die vollständige Spezifikation für einen Arbeitsblattnamen hat folgendes Format:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Beachten Sie, dass Excel 2007 eine Reihe neuer Dateierweiterungen eingeführt hat. Sie können den Pfad, den Arbeitsmappennamen und den Blattnamen weglassen, wobei zwischen den geöffneten Arbeitsmappen in dieser Excel Sitzung keine Zweideutigkeit besteht. 
  
Im nächsten Beispiel wird die Formel für das aktive Arbeitsblatt ausgewertet  `COUNT(A1:IV65536)` und das Ergebnis angezeigt. Beachten Sie, dass der Bereichsadresse "!" vorangestellt werden muss, was mit der Bereichsreferenzkonvention für XLM-Makrovorlagen konsistent ist. Die C-API XLM folgt dieser Konvention: 
  
- `=A1` Ein Verweis auf Zelle A1 auf dem aktuellen Makroblatt. (Für XLLs nicht definiert). 
  
- `=!A1` Ein Verweis auf Zelle A1 im aktiven Blatt (die ein Arbeitsblatt oder Makroblatt sein kann) 
  
- `=Sheet1!A1` Ein Verweis auf Zelle A1 auf dem angegebenen Blatt, in diesem Fall Sheet1. 
  
- `=[Book1.xls]Sheet1!A1` Ein Verweis auf Zelle A1 auf dem angegebenen Blatt in der angegebenen Arbeitsmappe. 
  
In einer XLL kann ein Verweis ohne führendes Ausrufezeichen (**!**) nicht in einen Wert konvertiert werden. Sie hat keine Bedeutung, da kein aktuelles Makroblatt vorhanden ist. Beachten Sie, dass ein führendes Gleichheitszeichen ( **=** ) optional ist und im nächsten Beispiel weggelassen wird.
  
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

Sie können auch die **xlfEvaluate-Funktion** verwenden, um die Registrierungs-ID einer XLL-Funktion aus ihrem registrierten Namen abzurufen, die dann zum Aufrufen dieser Funktion mithilfe der [xlUDF-Funktion](xludf.md)verwendet werden kann.
  
> [!NOTE]
> Der registrierte Name kann direkt an die **xlUDF-Funktion** übergeben werden. Dies bedeutet, dass Sie vermeiden können, dass Sie den Namen auswerten müssen, um die ID abzurufen, bevor **Sie xlUDF** aufrufen. Wenn die Funktion jedoch mehrmals aufgerufen werden soll, ist der Aufruf mithilfe der Registrierungs-ID schneller. 
  
## <a name="see-also"></a>Siehe auch

- [Excel-Arbeitsblatt- und Ausdrucksauswertung](excel-worksheet-and-expression-evaluation.md)
- [Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen](permitting-user-breaks-in-lengthy-operations.md)
- [Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

