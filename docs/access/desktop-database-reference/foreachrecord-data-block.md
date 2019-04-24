---
title: Fürjedendatensatz-Datenblock
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292328"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="3a3c4-102">Fürjedendatensatz-Datenblock</span><span class="sxs-lookup"><span data-stu-id="3a3c4-102">ForEachRecord data block</span></span>

<span data-ttu-id="3a3c4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a3c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a3c4-104">Ein **fürjedendatensatz** -Datenblock wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="3a3c4-105">Der **FürJedenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="3a3c4-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3a3c4-106">Setting</span></span>

<span data-ttu-id="3a3c4-107">Die **FürJedenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a3c4-108">Argument</span><span class="sxs-lookup"><span data-stu-id="3a3c4-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="3a3c4-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3a3c4-109">Required</span></span></p></th>
<th><p><span data-ttu-id="3a3c4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a3c4-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a3c4-111"><strong>In</strong></span><span class="sxs-lookup"><span data-stu-id="3a3c4-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="3a3c4-112">Ja</span><span class="sxs-lookup"><span data-stu-id="3a3c4-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="3a3c4-113">Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="3a3c4-114">Das Argument <em>in</em> kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="3a3c4-115"><strong>Hinweis</strong>: die angegebene Domäne kann Daten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind, nicht aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a3c4-116"><strong>Bedingung</strong></span><span class="sxs-lookup"><span data-stu-id="3a3c4-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="3a3c4-117">Nein</span><span class="sxs-lookup"><span data-stu-id="3a3c4-117">No</span></span></p></td>
<td><p><span data-ttu-id="3a3c4-118">Ein Zeichenfolgenausdruck, mit dem der Datenumfang eingeschränkt wird, auf dem der <strong>fürjedendatensatz</strong> -Datenblock ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="3a3c4-119">Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="3a3c4-120">Wenn criteria nicht angegeben wird, wird der <strong>fürjedendatensatz</strong> -Datenblock auf die gesamte Domäne angewendet, die durch das <em>in</em> -Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="3a3c4-121">Jedes Feld, das in Criteria enthalten ist, muss auch ein Feld in <em>in</em>sein.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a3c4-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="3a3c4-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="3a3c4-123">Nein</span><span class="sxs-lookup"><span data-stu-id="3a3c4-123">No</span></span></p></td>
<td><p><span data-ttu-id="3a3c4-124">Eine Zeichenfolge, die einen alternativen Namen für die durch das Argument <em>in</em> angegebene Domäne bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="3a3c4-125">Wird häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu kürzen, um mögliche mehrdeutige Verweise zu verhindern. Wenn <em>Alias</em> nicht angegeben wird, wird der Tabellen-oder Abfragename als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3a3c4-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a3c4-126">Remarks</span></span>

<span data-ttu-id="3a3c4-127">Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.</span><span class="sxs-lookup"><span data-stu-id="3a3c4-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

