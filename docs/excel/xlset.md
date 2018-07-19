---
title: gleich xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- gleich XlSet-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790624"
---
# <a name="xlset"></a><span data-ttu-id="fca2f-104">gleich xlSet</span><span class="sxs-lookup"><span data-stu-id="fca2f-104">xlSet</span></span>

<span data-ttu-id="fca2f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fca2f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fca2f-106">Konstantenwerte versetzt sehr schnell in Zellen oder Bereichen.</span><span class="sxs-lookup"><span data-stu-id="fca2f-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="fca2f-107">Weitere Informationen finden Sie unter "gleich XlSet und Arbeitsmappen mit Arrayformeln" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="fca2f-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="fca2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fca2f-108">Parameters</span></span>

<span data-ttu-id="fca2f-109">_pxReference_ (**XltypeRef** oder **XltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="fca2f-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="fca2f-110">Einen rechteckigen Verweis zur Beschreibung des Zielzelle oder Zellen.</span><span class="sxs-lookup"><span data-stu-id="fca2f-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="fca2f-111">Der Verweis muss also angrenzende Zellen beschreiben, die in einer **XltypeRef** `val.mref.lpmref->count` muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fca2f-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="fca2f-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="fca2f-112">_pxValue_</span></span>
  
<span data-ttu-id="fca2f-113">Der Wert oder die Werte in die Zelle oder die Zellen eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fca2f-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="fca2f-114">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="fca2f-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fca2f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fca2f-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="fca2f-116">PxValue-argument</span><span class="sxs-lookup"><span data-stu-id="fca2f-116">pxValue argument</span></span>

<span data-ttu-id="fca2f-117">_PxValue_ kann entweder ein Wert oder ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="fca2f-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="fca2f-118">Wenn sie ein Wert ist, wird mit diesem Wert der gesamten Zielbereich gefüllt.</span><span class="sxs-lookup"><span data-stu-id="fca2f-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="fca2f-119">Wenn es sich um ein Array (**XltypeMulti**) ist, werden die Elemente des Arrays in die entsprechenden Speicherorte im Rechteck eingefügt.</span><span class="sxs-lookup"><span data-stu-id="fca2f-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="fca2f-120">Wenn Sie ein horizontales Array für das zweite Argument verwenden, wird es nach unten dupliziert, um das gesamte Rechteck zu füllen.</span><span class="sxs-lookup"><span data-stu-id="fca2f-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="fca2f-121">Wenn Sie ein vertikales Array verwenden, wird er dupliziert rechts, um das gesamte Rechteck zu füllen.</span><span class="sxs-lookup"><span data-stu-id="fca2f-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="fca2f-122">Wenn Sie ein rechteckiges Array verwenden, und es ist zu klein für den rechteckigen Bereich, den Sie ihn in aufnehmen möchten, wird dieses Bereichs mit **#n/a**s aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="fca2f-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="fca2f-123">Wenn der Zielbereich kleiner als das Quell-Array ist, die Werte werden den Grenzen der Zielbereich kopiert und die zusätzlichen Daten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fca2f-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="fca2f-124">Ein Element des Zielrechtecks verwenden, um ein **XltypeNil** Typ Arrayelement im Quell-Array.</span><span class="sxs-lookup"><span data-stu-id="fca2f-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="fca2f-125">Deaktivieren Sie das gesamte Zielrechteck, ausgelassen werden Sie, das zweite Argument.</span><span class="sxs-lookup"><span data-stu-id="fca2f-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="fca2f-126">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fca2f-126">Restrictions</span></span>

<span data-ttu-id="fca2f-127">**gleich XlSet** kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="fca2f-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="fca2f-128">Darüber hinaus werden sie alle Rückgängig-Informationen, die vor dem verfügbaren möglicherweise wurden.</span><span class="sxs-lookup"><span data-stu-id="fca2f-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="fca2f-129">**gleich XlSet** können nur Konstanten, nicht Formeln in Zellen einfügen.</span><span class="sxs-lookup"><span data-stu-id="fca2f-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="fca2f-130">**gleich XlSet** verhält sich wie eine Klasse 3 Befehl äquivalente Funktion; d. h., steht er nur innerhalb einer DLL die DLL aufgerufen wird, ein Objekt, Makro, Menü, Symbolleiste, Tastenkombination oder die Schaltfläche **Ausführen** im Dialogfeld **Makro** (Zugriff über die Registerkarte **Ansicht** auf dem Menüband in Excel 2007 und den Tools **Starten **Menü in früheren Versionen).</span><span class="sxs-lookup"><span data-stu-id="fca2f-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="fca2f-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fca2f-131">Example</span></span>

<span data-ttu-id="fca2f-132">Im folgenden Beispiel wird die B205:B206 mit dem Wert, der aus einem Makro übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fca2f-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="fca2f-133">In diesem Befehlsbeispiel-Funktion erfordert ein Argument, und so funktioniert nur, wenn Sie aus einer XLM-Makrovorlage oder aus einem VBA-Modul die **entsprechende** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fca2f-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fca2f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fca2f-134">See also</span></span>

- [<span data-ttu-id="fca2f-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="fca2f-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="fca2f-136">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="fca2f-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

