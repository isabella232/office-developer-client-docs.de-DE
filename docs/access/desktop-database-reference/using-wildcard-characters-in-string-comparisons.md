---
title: Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305936"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="23647-102">Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen</span><span class="sxs-lookup"><span data-stu-id="23647-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="23647-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23647-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23647-p101">Der integrierte Mustervergleich ist ein vielseitiges Hilfsmittel, um Zeichenfolgenvergleiche anzustellen. In der folgenden Tabelle sind die Platzhalterzeichen aufgeführt, die Sie mit dem **Wie** -Operator verwenden können, sowie die Anzahl von übereinstimmenden Ziffern oder Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="23647-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23647-106">Zeichen in <em>Muster</em></span><span class="sxs-lookup"><span data-stu-id="23647-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="23647-107">Übereinstimmungen in <em>Ausdruck</em></span><span class="sxs-lookup"><span data-stu-id="23647-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23647-p102">? oder _ (Unterstrich)</span><span class="sxs-lookup"><span data-stu-id="23647-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="23647-110">Ein beliebiges Zeichen</span><span class="sxs-lookup"><span data-stu-id="23647-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23647-111">\*oder</span><span class="sxs-lookup"><span data-stu-id="23647-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="23647-112">Null oder mehr Zeichen</span><span class="sxs-lookup"><span data-stu-id="23647-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="23647-113">Jede einzelne Ziffer (0 - 9)</span><span class="sxs-lookup"><span data-stu-id="23647-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23647-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="23647-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="23647-115">Jedes einzelne unter <em>Zeichenliste</em> angegebene Zeichen</span><span class="sxs-lookup"><span data-stu-id="23647-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p><span data-ttu-id="23647-117">Jedes einzelne Zeichen, das nicht unter <em>Zeichenliste</em> angegeben ist</span><span class="sxs-lookup"><span data-stu-id="23647-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="23647-118">Sie können eine Gruppe von einem oder mehreren Zeichen (*charlist*), die in eckigen\[ \]Klammern () eingeschlossen sind, verwenden, um ein beliebiges einzelnes Zeichen in Expression abzugleichen *,* und *charlist* kann fast alle Zeichen im ANSI-Zeichensatz enthalten, einschließlich Ziffern.</span><span class="sxs-lookup"><span data-stu-id="23647-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="23647-119">Sie können die Sonderzeichen öffnende Klammer (\[ ), das Fragezeichen (?), das Nummern\#Zeichen () und das\*Sternchen () verwenden, um sich selbst direkt zuzuordnen, wenn Sie in eckigen Klammern eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="23647-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="23647-120">Sie können die schließende Klammer ( \]) nicht in einer Gruppe verwenden, um sich selbst abzugleichen, aber Sie kann Sie außerhalb einer Gruppe als einzelnes Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="23647-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="23647-121">Zusätzlich zu einer einfachen Liste mit Zeichen, die in eckigen \*\* Klammern eingeschlossen sind, kann charlist einen Zeichentyp angeben, indem Sie einen Bindestrich (-) verwenden, um die obere und untere Grenze des Bereichs zu trennen.</span><span class="sxs-lookup"><span data-stu-id="23647-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="23647-122">Wenn Sie beispielsweise \[A-Z\] in *Muster* verwenden, wird eine Übereinstimmung erzielt, wenn die entsprechende Zeichenposition in *Expression* einen der Großbuchstaben im Range A bis Z enthält. Sie können mehrere Bereiche in die eckigen Klammern einschließen, ohne die Bereiche zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="23647-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="23647-123">Beispielsweise stimmt \[a-Za-z0-9\] mit einem alphanumerischen Zeichen überein.</span><span class="sxs-lookup"><span data-stu-id="23647-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="23647-124">Beachten Sie, dass die ANSI SQL-Platzhalterzeichen (%) und (\_) sind nur verfügbar mit Microsoft Jet, Version 4. X, und dem Microsoft OLE DB-Anbieter für Jet.</span><span class="sxs-lookup"><span data-stu-id="23647-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="23647-125">Wenn sie in Microsoft Access oder DAO verwendet werden, werden sie als Literale behandelt.</span><span class="sxs-lookup"><span data-stu-id="23647-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="23647-126">Nachfolgend sind andere wichtige Regeln für den Mustervergleich aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="23647-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="23647-127">Ein Ausrufezeichen\!() am Anfang von *charlist* bedeutet, dass eine Übereinstimmung erzielt wird, wenn ein beliebiges Zeichen mit Ausnahme der Werte in *charlist* in *Expression*gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23647-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="23647-128">Bei Verwendung außerhalb der Klammern führt das Ausrufezeichen zu einer Übereinstimmung mit einem anderen Ausrufezeichen.</span><span class="sxs-lookup"><span data-stu-id="23647-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="23647-p107">Sie können den Trennstrich (-) entweder am Anfang (nach einem Ausrufezeichen, wenn eines verwendet wird) oder am Ende der *Zeichenliste* verwenden, damit ein anderer Trennstrich gefunden wird. An jeder anderen Position wird durch den Trennstrich ein Bereich von ANSI-Zeichen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="23647-p107">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself. In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="23647-131">Wenn Sie einen Bereich von Zeichen festlegen, müssen die Zeichen in aufsteigender Reihenfolge angegeben werden (A-Z oder 0-100).</span><span class="sxs-lookup"><span data-stu-id="23647-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="23647-132">\[A-Z\] ist ein gültiges Muster, \[aber Z-\] a nicht.</span><span class="sxs-lookup"><span data-stu-id="23647-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="23647-133">Die Zeichenfolge \[ \] wird ignoriert; Sie wird als Zeichenfolge der Länge NULL ("") betrachtet.</span><span class="sxs-lookup"><span data-stu-id="23647-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

