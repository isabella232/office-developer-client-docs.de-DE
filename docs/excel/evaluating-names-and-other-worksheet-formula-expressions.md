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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790419"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="82f33-104">Auswerten von Namen und andere Formel Arbeitsblatt-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="82f33-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="82f33-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82f33-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="82f33-106">Eines der wichtigsten Features, die über die C-API Excel verfügbar macht ist die Möglichkeit, eine beliebige Zeichenfolgenformel zu konvertieren, die an einen Wert oder ein Array von Werten in einem Arbeitsblatt gesetzlich eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="82f33-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="82f33-107">Dies ist entscheidend für XLL-Funktionen und Befehle, die den Inhalt der definierten Namen, beispielsweise gelesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="82f33-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="82f33-108">Diese Fähigkeit wird durch die [XlfEvaluate-Funktion](xlfevaluate.md), verfügbar gemacht, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82f33-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="82f33-109">Beachten Sie, dass, wenn Sie einen Namen, eigenständig oder in einer Formel evaluieren müssen Sie den Namen mit Präfix "!", mindestens.</span><span class="sxs-lookup"><span data-stu-id="82f33-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="82f33-110">Anderenfalls sucht Excel den Namen in einem ausgeblendeten Namespace reserviert für DLLs.</span><span class="sxs-lookup"><span data-stu-id="82f33-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="82f33-111">Sie können erstellen und Löschen von ausgeblendeten DLL-Namen mithilfe der [XlfSetName-Funktion](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="82f33-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="82f33-112">Sie können die Definition von einem beliebigen definierten Namen, abrufen, ob es sich um einen ausgeblendete DLL-Namen oder einen Arbeitsblattnamen ist mit der Funktion **XlfGetDef** .</span><span class="sxs-lookup"><span data-stu-id="82f33-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="82f33-113">Die vollständige Spezifikation für einen Arbeitsblattnamen hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="82f33-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="82f33-114">Beachten Sie, dass Excel 2007 eine Anzahl von neue Dateierweiterungen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="82f33-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="82f33-115">Kann ausgelassen werden, den Pfad, den Namen der Arbeitsmappe und der Name des Arbeitsblatts keine Mehrdeutigkeit zwischen geöffneten Arbeitsmappen in dieser Excel-Sitzung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82f33-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="82f33-116">Im nächste Beispiel wertet die Formel `COUNT(A1:IV65536)` für das aktive Arbeitsblatt und das Ergebnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82f33-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="82f33-117">Beachten Sie die Notwendigkeit die Bereichsadresse mit Präfix für '!', die konsistent mit der Bereich Verweis Convention auf XLM-Makroblättern ist.</span><span class="sxs-lookup"><span data-stu-id="82f33-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="82f33-118">Der C-API XLM folgt dieser Konvention:</span><span class="sxs-lookup"><span data-stu-id="82f33-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="82f33-119">`=A1`Ein Verweis auf die Zelle A1 in das aktuelle Makroblatt.</span><span class="sxs-lookup"><span data-stu-id="82f33-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="82f33-120">(Nicht für XLLs definiert).</span><span class="sxs-lookup"><span data-stu-id="82f33-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="82f33-121">`=!A1`Einen Verweis auf die Zelle A1 auf dem aktiven Blatt (sich ein Arbeitsblatt oder eine Makrovorlage handeln)</span><span class="sxs-lookup"><span data-stu-id="82f33-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="82f33-122">`=Sheet1!A1`Ein Verweis auf die Zelle A1 auf dem angegebenen Blatt, "Sheet1" in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="82f33-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="82f33-123">`=[Book1.xls]Sheet1!A1`Ein Verweis auf die Zelle A1 auf dem angegebenen Blatt in der angegebenen Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="82f33-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="82f33-124">In einer XLL kann nicht ohne eine führende Ausrufezeichen (**!**) ein Verweis auf einen anderen Wert konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="82f33-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="82f33-125">Es hat keine Bedeutung, da es keine aktuelle Makroblatt ist.</span><span class="sxs-lookup"><span data-stu-id="82f33-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="82f33-126">Beachten Sie, dass es sich bei ein führenden Anmelden ist gleich (**=**) ist optional und wird im nächsten Beispiel weggelassen.</span><span class="sxs-lookup"><span data-stu-id="82f33-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="82f33-127">Die **XlfEvaluate** -Funktion können auch die Registrierung-ID eine XLL-Funktion aus der registrierte Name, abzurufen, wodurch die aufzurufende Funktion mit der [Funktion XlUDF](xludf.md)verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="82f33-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="82f33-128">Der Name der registrierte kann direkt an die Funktion **XlUDF** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="82f33-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="82f33-129">Dies bedeutet, dass Sie zum Auswerten der Name, der die ID abzurufen, bevor **XlUDF**vermeiden können.</span><span class="sxs-lookup"><span data-stu-id="82f33-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="82f33-130">Jedoch ist die Funktion oft aufgerufen werden, das es mithilfe der Registrierung, die ID schneller ist aufrufen.</span><span class="sxs-lookup"><span data-stu-id="82f33-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82f33-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82f33-131">See also</span></span>

- [<span data-ttu-id="82f33-132">Excel-Arbeitsblatt und die Auswertung von Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="82f33-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="82f33-133">Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorgänge</span><span class="sxs-lookup"><span data-stu-id="82f33-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="82f33-134">Erste Schritte mit Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="82f33-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

