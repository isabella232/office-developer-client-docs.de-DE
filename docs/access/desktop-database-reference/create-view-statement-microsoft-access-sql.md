---
title: CREATE VIEW-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706625"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="e175a-102">CREATE VIEW-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e175a-102">CREATE VIEW statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="e175a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e175a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e175a-104">Erstellt eine neue Sicht.</span><span class="sxs-lookup"><span data-stu-id="e175a-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="e175a-105">[!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der CREATE VIEW-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen.</span><span class="sxs-lookup"><span data-stu-id="e175a-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="e175a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e175a-106">Syntax</span></span>

<span data-ttu-id="e175a-107">CREATE VIEW *Sicht* \[(*Feld1*\[, *Feld2*\[,... \] \])\] AS *SELECT-Anweisung*</span><span class="sxs-lookup"><span data-stu-id="e175a-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="e175a-108">Die CREATE VIEW-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="e175a-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e175a-109">Komponente</span><span class="sxs-lookup"><span data-stu-id="e175a-109">Part</span></span></p></th>
<th><p><span data-ttu-id="e175a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e175a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e175a-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="e175a-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="e175a-112">Der Name der zu erstellenden Sicht.</span><span class="sxs-lookup"><span data-stu-id="e175a-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e175a-113"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="e175a-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="e175a-114">Der Name des oder der Felder, die den Feldern aus der <em>Select-Anweisung</em> entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e175a-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e175a-115"><em>SelectAnweisung</em></span><span class="sxs-lookup"><span data-stu-id="e175a-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="e175a-116">Eine SQL SELECT-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="e175a-116">A SQL SELECT statement.</span></span> <span data-ttu-id="e175a-117">Weitere Informationen finden Sie in der <a href="select-statement-microsoft-access-sql.md">SELECT-Anweisung</a>.</span><span class="sxs-lookup"><span data-stu-id="e175a-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e175a-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e175a-118">Remarks</span></span>

<span data-ttu-id="e175a-119">Bei einer SELECT-Anweisung zur Definition einer Sicht kann es sich nicht um eine [SELECT INTO](select-into-statement-microsoft-access-sql.md)-Anweisung handeln.</span><span class="sxs-lookup"><span data-stu-id="e175a-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="e175a-120">Die SELECT-Anweisung zur Definition einer Sicht kann keine Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="e175a-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="e175a-121">Der Name der Sicht darf nicht mit dem Namen einer vorhandenen Tabelle identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e175a-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="e175a-122">Wenn die durch die SELECT-Anweisung definierte Abfrage aktualisiert werden kann, wird die Ansicht auch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e175a-122">If the query defined by the SELECT statement is updatable, the view is also updatable.</span></span> <span data-ttu-id="e175a-123">Andernfalls ist die Sicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e175a-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="e175a-124">Verfügen zwei Felder in der über die SELECT-Anweisung definierten Abfrage über den gleichen Namen, muss die Definition der Sicht eine Feldliste einschließen, die für jedes der Felder in der Abfrage einen eindeutigen Namen angibt.</span><span class="sxs-lookup"><span data-stu-id="e175a-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

