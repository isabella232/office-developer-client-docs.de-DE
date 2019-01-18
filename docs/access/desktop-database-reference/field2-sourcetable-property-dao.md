---
title: Field2.SourceTable-Eigenschaft (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a3ecf8b6655bb9f1dd2b25d264708112834e8a90
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717944"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="4b96c-102">Field2.SourceTable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b96c-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="4b96c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b96c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b96c-p101">Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein **Field2**-Objekt handelt. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4b96c-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b96c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b96c-106">Syntax</span></span>

<span data-ttu-id="4b96c-107">*Ausdruck* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="4b96c-107">*expression* .SourceTable</span></span>

<span data-ttu-id="4b96c-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b96c-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b96c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b96c-109">Remarks</span></span>

<span data-ttu-id="4b96c-110">Bei einem **Field2**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="4b96c-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b96c-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="4b96c-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4b96c-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="4b96c-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b96c-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="4b96c-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4b96c-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4b96c-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b96c-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4b96c-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4b96c-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b96c-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b96c-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4b96c-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4b96c-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b96c-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b96c-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="4b96c-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4b96c-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4b96c-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b96c-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4b96c-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4b96c-122">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b96c-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b96c-p102">Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field2**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.</span><span class="sxs-lookup"><span data-stu-id="4b96c-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="4b96c-125">Die SourceTable-Eigenschaft gibt keinen sinnvollen Tabellenamen zurück, wenn sie für ein Field2-Objekt in der Fields-Auflistung eines Recordset-Objekts vom Typ Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b96c-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


