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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295366"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="23e23-102">CREATE VIEW-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="23e23-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="23e23-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23e23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23e23-104">Erstellt eine neue Sicht.</span><span class="sxs-lookup"><span data-stu-id="23e23-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="23e23-105">Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung von CREATE VIEW oder einer der DDL-Anweisungen für Datenbanken, die nicht mit dem Microsoft Access-Datenbankmodul erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="23e23-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e23-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e23-106">Syntax</span></span>

<span data-ttu-id="23e23-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="23e23-107">CREATE VIEW *view [(field1* \[[, *field2*[, …]])] AS *selectstatement*</span></span>

<span data-ttu-id="23e23-108">Die CREATE VIEW-Anweisung setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="23e23-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23e23-109">Part</span><span class="sxs-lookup"><span data-stu-id="23e23-109">Part</span></span></p></th>
<th><p><span data-ttu-id="23e23-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23e23-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23e23-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="23e23-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="23e23-112">Der Name der zu erstellenden Sicht.</span><span class="sxs-lookup"><span data-stu-id="23e23-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23e23-113"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="23e23-113"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="23e23-114">Die Namen der Felder für die entsprechenden in der <em>SELECT-Anweisung</em> angegebenen Felder.</span><span class="sxs-lookup"><span data-stu-id="23e23-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23e23-115"><em>SELECT-Anweisung</em></span><span class="sxs-lookup"><span data-stu-id="23e23-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="23e23-116">Eine SQL SELECT-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="23e23-116">A SQL SELECT statement.</span></span> <span data-ttu-id="23e23-117">Weitere Informationen finden Sie unter <a href="select-statement-microsoft-access-sql.md">SELECT-Anweisung</a>.</span><span class="sxs-lookup"><span data-stu-id="23e23-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="23e23-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e23-118">Remarks</span></span>

<span data-ttu-id="23e23-119">Bei einer SELECT-Anweisung zur Definition einer Sicht kann es sich nicht um eine [SELECT INTO](select-into-statement-microsoft-access-sql.md)-Anweisung handeln.</span><span class="sxs-lookup"><span data-stu-id="23e23-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="23e23-120">Die SELECT-Anweisung, die die Sicht definiert, darf keine Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="23e23-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="23e23-121">Der Name der Sicht darf nicht mit dem Namen einer vorhandenen Tabelle übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="23e23-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="23e23-122">Handelt es sich bei der über die SELECT-Anweisung definierten Abfrage um eine Abfrage, die aktualisiert werden kann, ist die Aktualisierung der Sicht ebenfalls möglich.</span><span class="sxs-lookup"><span data-stu-id="23e23-122">If the query defined by the SELECT statement is updatable, then the view is also updatable.</span></span> <span data-ttu-id="23e23-123">Andernfalls ist die Sicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="23e23-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="23e23-124">Wenn zwei beliebige Felder in der durch die SELECT-Anweisung definierten Abfrage denselben Namen haben, muss die Sichtdefinition eine Feldliste mit eindeutigen Namen für jedes Feld in der Abfrage enthalten.</span><span class="sxs-lookup"><span data-stu-id="23e23-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

