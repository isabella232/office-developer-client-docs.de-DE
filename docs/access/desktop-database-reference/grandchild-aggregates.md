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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292146"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="be1ad-102">Enkel-Aggregat</span><span class="sxs-lookup"><span data-stu-id="be1ad-102">Grandchild aggregates</span></span>


<span data-ttu-id="be1ad-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be1ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be1ad-104">Die Chapter-Spalte, die in einer Klausel eines Shape-Befehls erstellt wurde, kann einen *Kapitel-Aliasnamen* erhalten (normalerweise mit dem As-Schlüsselwort).</span><span class="sxs-lookup"><span data-stu-id="be1ad-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="be1ad-105">Sie können jede Spalte in einem beliebigen Kapitel des geformten **Recordset-Objekts** mit einem vollqualifizierten Namen identifizieren, der das untergeordnete Element der Spalte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="be1ad-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="be1ad-106">Wenn beispielsweise das übergeordnete Chapter, chap1, ein untergeordnetes Chapter (chap2) enthält, das eine Betragsspalte "Amt" aufweist, lautet der qualifizierte Name chap1. chap2. Amt. Der qualifizierte Name kann dann als Argument für eine der Aggregatfunktionen verwendet werden (SUM, AVG, MAX, MIN, COUNT, STDEV oder ANY).</span><span class="sxs-lookup"><span data-stu-id="be1ad-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

