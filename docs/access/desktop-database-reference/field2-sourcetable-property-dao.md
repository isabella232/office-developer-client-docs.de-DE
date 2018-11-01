---
title: Field2.SourceTable Property (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb0c7b57b8ad5c0a1c202197e14fdaefd9a1103f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881020"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="a71f3-102">Field2.SourceTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a71f3-102">Field2.SourceTable Property (DAO)</span></span>


<span data-ttu-id="a71f3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a71f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a71f3-p101">Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein **Field2**-Objekt handelt. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="a71f3-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71f3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a71f3-106">Syntax</span></span>

<span data-ttu-id="a71f3-107">*Ausdruck* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="a71f3-107">*expression* .SourceTable</span></span>

<span data-ttu-id="a71f3-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a71f3-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a71f3-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a71f3-109">Remarks</span></span>

<span data-ttu-id="a71f3-110">Bei einem **Field2**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="a71f3-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a71f3-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="a71f3-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="a71f3-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="a71f3-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a71f3-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a71f3-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a71f3-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a71f3-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a71f3-115"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="a71f3-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a71f3-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a71f3-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a71f3-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a71f3-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="a71f3-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a71f3-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a71f3-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="a71f3-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="a71f3-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a71f3-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a71f3-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a71f3-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a71f3-122">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a71f3-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a71f3-p102">Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field2**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.</span><span class="sxs-lookup"><span data-stu-id="a71f3-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a71f3-125">Die SourceTable-Eigenschaft gibt keinen sinnvollen Tabellenamen zurück, wenn sie für ein Field2-Objekt in der Fields-Auflistung eines Recordset-Objekts vom Typ Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a71f3-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field2</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


