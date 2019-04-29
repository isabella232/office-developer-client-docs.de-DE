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
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="23c46-104">Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken</span><span class="sxs-lookup"><span data-stu-id="23c46-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="23c46-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="23c46-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="23c46-106">Eine der wichtigsten Features, die Excel über die C-API verfügbar macht, ist die Möglichkeit, beliebige Zeichenfolgen Formeln, die rechtlich in ein Arbeitsblatt eingegeben werden können, in einen Wert oder ein Array von Werten umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="23c46-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="23c46-107">Dies ist für XLL-Funktionen und Befehle unerlässlich, die beispielsweise den Inhalt definierter Namen lesen müssen.</span><span class="sxs-lookup"><span data-stu-id="23c46-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="23c46-108">Diese Fähigkeit wird über die [xlfEvaluate-Funktion](xlfevaluate.md)offen gelegt, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="23c46-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="23c46-109">Beachten Sie Folgendes: Wenn Sie einen Arbeitsblattnamen auswerten, entweder eigenständig oder in einer Formel, müssen Sie den Namen mindestens mit "!" voranstellen.</span><span class="sxs-lookup"><span data-stu-id="23c46-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="23c46-110">Andernfalls versucht Excel, den Namen in einem ausgeblendeten Namespace zu finden, der für DLLs reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="23c46-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="23c46-111">Sie können mit der [xlfSetName-Funktion](xlfsetname.md)versteckte DLL-Namen erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="23c46-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="23c46-112">Sie können die Definition eines definierten Namens abrufen, unabhängig davon, ob es sich um einen versteckten DLL-Namen oder einen Arbeitsblattnamen handelt, indem Sie die **xlfGetDef** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="23c46-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="23c46-113">Die vollständige Spezifikation für einen Arbeitsblattnamen hat das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="23c46-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="23c46-114">Beachten Sie, dass Excel 2007 eine Reihe neuer Dateierweiterungen eingeführt hat.</span><span class="sxs-lookup"><span data-stu-id="23c46-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="23c46-115">Sie können den Pfad, den Namen der Arbeitsmappe und den Namen des Blatts weglassen, wobei die geöffneten Arbeitsmappen in dieser Excel-Sitzung nicht eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="23c46-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="23c46-116">Im nächsten Beispiel wird die Formel `COUNT(A1:IV65536)` für das aktive Arbeitsblatt ausgewertet und das Ergebnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23c46-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="23c46-117">Beachten Sie, dass die Range-Adresse mit "!" vorangestellt werden muss, was mit der Range Reference Convention in XML-Makro Blättern konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="23c46-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="23c46-118">Die C-API XML folgt diesem Übereinkommen:</span><span class="sxs-lookup"><span data-stu-id="23c46-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="23c46-119">`=A1`Ein Verweis auf die Zelle a1 in der aktuellen Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="23c46-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="23c46-120">(Nicht für XLLs definiert).</span><span class="sxs-lookup"><span data-stu-id="23c46-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="23c46-121">`=!A1`Ein Verweis auf die Zelle a1 auf dem aktiven Blatt (Dies kann ein Arbeitsblatt oder ein Makroblatt sein)</span><span class="sxs-lookup"><span data-stu-id="23c46-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="23c46-122">`=Sheet1!A1`Ein Verweis auf die Zelle a1 auf dem angegebenen Blatt, Sheet1 in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="23c46-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="23c46-123">`=[Book1.xls]Sheet1!A1`Ein Verweis auf die Zelle a1 auf dem angegebenen Blatt in der angegebenen Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="23c46-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="23c46-124">In einer XLL kann ein Verweis ohne ein führendes Ausrufezeichen (**!**) nicht in einen Wert konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="23c46-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="23c46-125">Es hat keine Bedeutung, da es keine aktuelle Makrovorlage gibt.</span><span class="sxs-lookup"><span data-stu-id="23c46-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="23c46-126">Beachten Sie, dass ein führendes**=** Gleichheitszeichen () optional ist und im nächsten Beispiel ausgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="23c46-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="23c46-127">Sie können auch die **XLFEVALUATE** -Funktion verwenden, um die Registrierungs-ID einer XLL-Funktion aus dem registrierten Namen abzurufen, die dann zum Aufrufen dieser Funktion mithilfe der [xlUDF-Funktion](xludf.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="23c46-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="23c46-128">Der registrierte Name kann direkt an die **xlUDF** -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="23c46-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="23c46-129">Das heißt, Sie können verhindern, dass Sie den Namen auswerten, um die ID zu erhalten, bevor Sie **xlUDF**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="23c46-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="23c46-130">Wenn die Funktion jedoch mehrmals aufgerufen werden soll, wird Sie mit der Registrierungs-ID schneller ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23c46-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23c46-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23c46-131">See also</span></span>

- [<span data-ttu-id="23c46-132">Excel-Arbeitsblatt- und Ausdrucksauswertung</span><span class="sxs-lookup"><span data-stu-id="23c46-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="23c46-133">Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="23c46-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="23c46-134">Erste Schritte mit dem Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="23c46-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

