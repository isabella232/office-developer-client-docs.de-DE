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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716901"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="a400a-102">Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen</span><span class="sxs-lookup"><span data-stu-id="a400a-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="a400a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a400a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a400a-p101">Der integrierte Mustervergleich ist ein vielseitiges Hilfsmittel, um Zeichenfolgenvergleiche anzustellen. In der folgenden Tabelle sind die Platzhalterzeichen aufgeführt, die Sie mit dem **Wie** -Operator verwenden können, sowie die Anzahl von übereinstimmenden Ziffern oder Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="a400a-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a400a-106">Zeichen in <em>pattern</em></span><span class="sxs-lookup"><span data-stu-id="a400a-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="a400a-107">Übereinstimmungen in <em>Ausdruck</em></span><span class="sxs-lookup"><span data-stu-id="a400a-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a400a-p102">? oder _ (Unterstrich)</span><span class="sxs-lookup"><span data-stu-id="a400a-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="a400a-110">Jedes einzelne Zeichen</span><span class="sxs-lookup"><span data-stu-id="a400a-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a400a-111">\*oder %</span><span class="sxs-lookup"><span data-stu-id="a400a-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="a400a-112">Null oder mehr Zeichen</span><span class="sxs-lookup"><span data-stu-id="a400a-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="a400a-113">Jede einzelne Ziffer (0 - 9)</span><span class="sxs-lookup"><span data-stu-id="a400a-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a400a-114">[<em>Zeichenliste</em>]</span><span class="sxs-lookup"><span data-stu-id="a400a-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="a400a-115">Ein beliebiges einzelnes Zeichen in <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="a400a-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>Zeichenliste</em>]</p></td>
<td><p><span data-ttu-id="a400a-117">Ein beliebiges einzelnes Zeichen nicht in <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="a400a-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a400a-118">Sie können eine Gruppe von einem oder mehreren Zeichen (*Charlist*) in Klammern eingeschlossen (\[ \]) auf beliebiges einzelnes Zeichen in *Ausdruck,* und *Charlist* fast alle Zeichen enthalten in ANSI-Zeichen festgelegt, einschließlich Ziffern.</span><span class="sxs-lookup"><span data-stu-id="a400a-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="a400a-119">Können die Sonderzeichen Klammern (\[ ), Frage Mark (?), Nummernzeichen (\#), und ein Sternchen (\*) zu einer Übereinstimmung mit direkt nur, wenn in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a400a-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="a400a-120">Die schließende Klammer kann nicht verwendet werden ( \]) innerhalb einer Gruppe entsprechend selbst, aber Sie können es außerhalb einer Gruppe als ein einzelnes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a400a-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="a400a-121">Zusätzlich zu einer Liste von Zeichen in Klammern eingeschlossen können *Charlist* einen Bereich von Zeichen angeben, mit einem Bindestrich (-) zum Trennen der Ober- und Untergrenze des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a400a-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="a400a-122">Verwenden Sie beispielsweise \[A – Z\] in *Muster* ergibt eine Übereinstimmung, wenn die entsprechende Zeichenposition im *Ausdruck* Großbuchstaben im Bereich von A bis Z enthält. Sie können mehrere Bereiche innerhalb der Klammern einschließen, ohne zur Einschränkung die Bereiche.</span><span class="sxs-lookup"><span data-stu-id="a400a-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="a400a-123">Beispielsweise \[a-zA-Z0-9\] entspricht einem alphanumerisches Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a400a-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="a400a-124">Es ist wichtig zu beachten, dass die ANSI SQL-Platzhalter (%) und (\_) sind nur verfügbar, mit Microsoft Jet Version 4.X und den Microsoft OLE DB-Anbieter für Jet.</span><span class="sxs-lookup"><span data-stu-id="a400a-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="a400a-125">Wenn sie in Microsoft Access oder DAO verwendet werden, werden sie als Literale behandelt.</span><span class="sxs-lookup"><span data-stu-id="a400a-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="a400a-126">Nachfolgend sind andere wichtige Regeln für den Mustervergleich aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="a400a-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="a400a-127">Ausrufezeichen (\!) am Anfang von *Charlist* bedeutet, der eine Übereinstimmung, wenn ein beliebiges Zeichen außer denen in *Charlist* im *Ausdruck*gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a400a-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="a400a-128">Bei Verwendung außerhalb der Klammern führt das Ausrufezeichen zu einer Übereinstimmung mit einem anderen Ausrufezeichen.</span><span class="sxs-lookup"><span data-stu-id="a400a-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="a400a-129">Sie können Bindestrich (-) am Anfang (nach einem Ausrufezeichen, falls verwendet wird) oder am Ende des *Charlist* selbst abgleichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a400a-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="a400a-130">An jeder anderen Position wird durch den Trennstrich ein Bereich von ANSI-Zeichen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a400a-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="a400a-131">Wenn Sie einen Bereich von Zeichen festlegen, müssen die Zeichen in aufsteigender Reihenfolge angegeben werden (A-Z oder 0-100).</span><span class="sxs-lookup"><span data-stu-id="a400a-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="a400a-132">\[A – Z\] ist ein gültiges Muster, aber \[Z-A\] ist nicht.</span><span class="sxs-lookup"><span data-stu-id="a400a-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="a400a-133">Die Zeichenfolge \[ \] wird ignoriert. Es gilt eine Nullzeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="a400a-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

