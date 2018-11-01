---
title: Field.SourceTable Property (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1a11544808cfb897a359a5e170332ba23e25ceae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888041"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="d444d-102">Field.SourceTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d444d-102">Field.SourceTable Property (DAO)</span></span>


<span data-ttu-id="d444d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d444d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d444d-p101">Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein **Field**-Objekt handelt. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="d444d-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d444d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d444d-106">Syntax</span></span>

<span data-ttu-id="d444d-107">*Ausdruck* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="d444d-107">*expression* .SourceTable</span></span>

<span data-ttu-id="d444d-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d444d-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d444d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d444d-109">Remarks</span></span>

<span data-ttu-id="d444d-110">Bei einem **Field**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="d444d-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d444d-111">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="d444d-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="d444d-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d444d-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d444d-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="d444d-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d444d-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d444d-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d444d-115"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="d444d-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d444d-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d444d-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d444d-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d444d-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="d444d-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d444d-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d444d-119"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="d444d-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="d444d-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d444d-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d444d-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d444d-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d444d-122">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d444d-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d444d-p102">Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.</span><span class="sxs-lookup"><span data-stu-id="d444d-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d444d-125">Die SourceTable-Eigenschaft gibt keinen sinnvollen Tabellenamen zurück, wenn sie für ein Field-Objekt in der Fields-Auflistung eines Recordset-Objekts vom Typ Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d444d-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


