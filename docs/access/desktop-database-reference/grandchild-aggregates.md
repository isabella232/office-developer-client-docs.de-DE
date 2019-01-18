---
title: Enkel-Aggregat
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722158"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="ea5eb-102">Enkel-Aggregat</span><span class="sxs-lookup"><span data-stu-id="ea5eb-102">Grandchild aggregates</span></span>


<span data-ttu-id="ea5eb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea5eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea5eb-p101">Die in einer Klausel eines Strukturierungsbefehls erstellte Kapitelspalte erhält möglicherweise einen Kapitelaliasnamen (üblicherweise mit dem Schlüsselwort AS). Sie können eine Spalte in einem beliebigen Kapitel des strukturierten Recordset-Objekts mit einem vollqualifizierten Namen bezeichnen, durch den das untergeordnete Recordset identifiziert wird, das die Spalte enthält. Wenn z. B. das übergeordnete Kapitel, Kapitel1, ein untergeordnetes Kapitel, Kapitel2 enthält, das eine Mengenspalte, Menge, enthält, würde der qualifizierte Name Kapitel1.Kapitel2.Menge lauten. Der qualifizierte Name kann dann als Argument in einer der Aggregatfunktionen (SUM, AVG, MAX, MIN, COUNT, STDEV oder ANY) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea5eb-p101">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword). You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

