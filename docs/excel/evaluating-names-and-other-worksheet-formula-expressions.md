---
title: Auswerten von Namen und andere Formel Arbeitsblatt-Ausdrücke
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Auswertung von Ausdrücken [excel 2007], Arbeitsblätter [Excel 2007], Name zu Evaluierungszwecken Auswerten von Ausdrücken [Excel 2007], auswerten Arbeitsblattnamen [Excel 2007], Ausdrücke [Excel 2007], bewerten, Namen [Excel 2007], bewerten, nennen Sie Evaluierungshandbuch und exemplarische Vorgehensweisen [Excel 2007] , Zeichenfolgen [Excel 2007], konvertieren in Werte, XlfEvaluate-Funktion [Excel 2007], [Excel 2007-Arbeitsblättern, Auswertung von Ausdrücken
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790419"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Auswerten von Namen und andere Formel Arbeitsblatt-Ausdrücke

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Eines der wichtigsten Features, die über die C-API Excel verfügbar macht ist die Möglichkeit, eine beliebige Zeichenfolgenformel zu konvertieren, die an einen Wert oder ein Array von Werten in einem Arbeitsblatt gesetzlich eingegeben werden können. Dies ist entscheidend für XLL-Funktionen und Befehle, die den Inhalt der definierten Namen, beispielsweise gelesen werden müssen. Diese Fähigkeit wird durch die [XlfEvaluate-Funktion](xlfevaluate.md), verfügbar gemacht, wie im folgenden Beispiel dargestellt.
  
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

Beachten Sie, dass, wenn Sie einen Namen, eigenständig oder in einer Formel evaluieren müssen Sie den Namen mit Präfix "!", mindestens. Anderenfalls sucht Excel den Namen in einem ausgeblendeten Namespace reserviert für DLLs. Sie können erstellen und Löschen von ausgeblendeten DLL-Namen mithilfe der [XlfSetName-Funktion](xlfsetname.md). Sie können die Definition von einem beliebigen definierten Namen, abrufen, ob es sich um einen ausgeblendete DLL-Namen oder einen Arbeitsblattnamen ist mit der Funktion **XlfGetDef** . 
  
Die vollständige Spezifikation für einen Arbeitsblattnamen hat folgendes Format:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Beachten Sie, dass Excel 2007 eine Anzahl von neue Dateierweiterungen eingeführt. Kann ausgelassen werden, den Pfad, den Namen der Arbeitsmappe und der Name des Arbeitsblatts keine Mehrdeutigkeit zwischen geöffneten Arbeitsmappen in dieser Excel-Sitzung vorhanden ist. 
  
Im nächste Beispiel wertet die Formel `COUNT(A1:IV65536)` für das aktive Arbeitsblatt und das Ergebnis angezeigt. Beachten Sie die Notwendigkeit die Bereichsadresse mit Präfix für '!', die konsistent mit der Bereich Verweis Convention auf XLM-Makroblättern ist. Der C-API XLM folgt dieser Konvention: 
  
- `=A1`Ein Verweis auf die Zelle A1 in das aktuelle Makroblatt. (Nicht für XLLs definiert). 
  
- `=!A1`Einen Verweis auf die Zelle A1 auf dem aktiven Blatt (sich ein Arbeitsblatt oder eine Makrovorlage handeln) 
  
- `=Sheet1!A1`Ein Verweis auf die Zelle A1 auf dem angegebenen Blatt, "Sheet1" in diesem Fall. 
  
- `=[Book1.xls]Sheet1!A1`Ein Verweis auf die Zelle A1 auf dem angegebenen Blatt in der angegebenen Arbeitsmappe. 
  
In einer XLL kann nicht ohne eine führende Ausrufezeichen (**!**) ein Verweis auf einen anderen Wert konvertiert werden. Es hat keine Bedeutung, da es keine aktuelle Makroblatt ist. Beachten Sie, dass es sich bei ein führenden Anmelden ist gleich (**=**) ist optional und wird im nächsten Beispiel weggelassen.
  
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

Die **XlfEvaluate** -Funktion können auch die Registrierung-ID eine XLL-Funktion aus der registrierte Name, abzurufen, wodurch die aufzurufende Funktion mit der [Funktion XlUDF](xludf.md)verwendet werden können.
  
> [!NOTE]
> Der Name der registrierte kann direkt an die Funktion **XlUDF** übergeben werden. Dies bedeutet, dass Sie zum Auswerten der Name, der die ID abzurufen, bevor **XlUDF**vermeiden können. Jedoch ist die Funktion oft aufgerufen werden, das es mithilfe der Registrierung, die ID schneller ist aufrufen. 
  
## <a name="see-also"></a>Siehe auch

- [Excel-Arbeitsblatt und die Auswertung von Ausdrücken](excel-worksheet-and-expression-evaluation.md)
- [Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorg�nge](permitting-user-breaks-in-lengthy-operations.md)
- [Erste Schritte mit Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

