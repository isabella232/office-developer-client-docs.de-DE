---
title: FürJedenDatensatz-Datenblock
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706345"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="9b376-102">FürJedenDatensatz-Datenblock</span><span class="sxs-lookup"><span data-stu-id="9b376-102">ForEachRecord data block</span></span>

<span data-ttu-id="9b376-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b376-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b376-104">Mit einem **FürJedenDatensatz** -Datenblock wird eine Reihe von Anweisungen für jeden Datensatz in einer Domäne wiederholt.</span><span class="sxs-lookup"><span data-stu-id="9b376-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="9b376-105">[!HINWEIS] Der **FürJedenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b376-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="9b376-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="9b376-106">Setting</span></span>

<span data-ttu-id="9b376-107">Die **FürJedenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b376-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b376-108">Argument</span><span class="sxs-lookup"><span data-stu-id="9b376-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="9b376-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b376-109">Required</span></span></p></th>
<th><p><span data-ttu-id="9b376-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b376-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b376-111"><strong>In</strong></span><span class="sxs-lookup"><span data-stu-id="9b376-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="9b376-112">Ja</span><span class="sxs-lookup"><span data-stu-id="9b376-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="9b376-113">Eine Zeichenfolge zur Identifizierung von Datensätzen für den Betrieb die Domäne.</span><span class="sxs-lookup"><span data-stu-id="9b376-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="9b376-114">Das <em>im</em> Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b376-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="9b376-115"><strong>Hinweis</strong>: die angegebene Domäne darf keine enthalten Daten in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9b376-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b376-116"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="9b376-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="9b376-117">Nein</span><span class="sxs-lookup"><span data-stu-id="9b376-117">No</span></span></p></td>
<td><p><span data-ttu-id="9b376-118">Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des <strong>FürJedenDatensatz</strong> -Datenblocks wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b376-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="9b376-119">Häufig wird beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem.</span><span class="sxs-lookup"><span data-stu-id="9b376-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="9b376-120">Kriterien nicht angegeben, wirkt sich auf die gesamte Domäne angegeben, die durch das Argument <em>In</em> das <strong>FürJedenDatensatz</strong> -Datenblock.</span><span class="sxs-lookup"><span data-stu-id="9b376-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="9b376-121">Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in <em>In</em>sein.</span><span class="sxs-lookup"><span data-stu-id="9b376-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b376-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="9b376-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="9b376-123">Nein</span><span class="sxs-lookup"><span data-stu-id="9b376-123">No</span></span></p></td>
<td><p><span data-ttu-id="9b376-124">Eine Zeichenfolge, die einen alternativen Namen für die Domäne, die durch das Argument <em>im</em> angegebenen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9b376-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="9b376-125">Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen. Wenn <em>Alias</em> nicht angegeben ist, wird den Namen der Tabelle oder Abfrage als Alias verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b376-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b376-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b376-126">Remarks</span></span>

<span data-ttu-id="9b376-127">Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.</span><span class="sxs-lookup"><span data-stu-id="9b376-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

